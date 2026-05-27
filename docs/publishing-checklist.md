# Publishing Checklist

For shipping a new version of the Synthesis Playbook plugin.

## Before any release

### Content checks

- [ ] All prompt files in `prompts/` match the verbatim text in the book's appendix (no drift)
- [ ] SKILL.md frontmatter for each sub-skill has accurate `name` and `description`
- [ ] Slash command frontmatter has accurate `description`
- [ ] No broken internal links in any markdown file (`SKILL.md` → `references/` → `prompts/`)
- [ ] No banned vocabulary in newly-written content: *leverage, comprehensive, robust, key, critical, streamline, empower, elevate, transformative, strategic* (when used as generic praise)

### Voice checks

- [ ] Read the new content aloud (the aloud test applies to plugin content too)
- [ ] No "in today's fast-paced world" / "at the end of the day" / "ultimately" / "to summarize" / "in conclusion"
- [ ] First-person where it earns its place; no anonymous LinkedIn voice
- [ ] No model-flavored generic prose in any newly-written reference or doc

### Manifest checks

- [ ] `plugin.json` `version` bumped appropriately (semver)
- [ ] `CHANGELOG.md` has a new entry with date and changes
- [ ] `plugin.json` `keywords` are accurate
- [ ] Repository URL in `plugin.json` matches the actual GitHub URL

### Repository hygiene

- [ ] `LICENSE` is present and accurate (MIT for v0.1.x)
- [ ] `CONTRIBUTING.md` is up to date with current contribution patterns
- [ ] `SECURITY.md` has current contact info
- [ ] `.gitignore` covers common cruft
- [ ] No accidental private files committed (check `git status` carefully)

### Functional checks (local install)

- [ ] Clone the repo to a clean machine or fresh `~/.claude/plugins/cache/` location
- [ ] Restart Claude Code
- [ ] Verify all 7 slash commands appear (`/synthesis-help`, `/synthesis-discovery`, `/synthesis-offsite`, `/synthesis-sprint`, `/synthesis-ideation`, `/synthesis-retro`, `/synthesis-training`)
- [ ] Invoke `/synthesis-help` and verify the decision tree works
- [ ] Run `/synthesis-discovery` against a test synthesis-ready file (see test fixtures, if shipped)
- [ ] Verify the pipeline agent pauses correctly at human-authored steps

### Discovery recipe end-to-end test

1. Create a fake synthesis-ready file with 3 short interview transcripts + 1 hypothesis line at `/tmp/test-engagement.md`
2. Run `/synthesis-discovery` pointing at `/tmp/test-engagement.md`
3. Confirm agent runs steps 1–3 (prep, cluster, anti-flatten)
4. Confirm agent pauses at step 4 (INTERPRET) and asks for human authorship
5. Provide interpretations
6. Confirm agent resumes, runs 5–6, pauses at 7 (PRIORITIZE)
7. Provide shortlist
8. Confirm agent runs step 8 (NARRATE), drafts deck + brief

If any step fails, **do not ship.** Open an issue and fix.

## For minor releases (0.x.0)

Additional checks:

- [ ] If new recipes added, all variant files referenced in their SKILL.md exist
- [ ] If new pipeline agents added, they follow the Discovery agent's pattern (pauses at human-authored steps, refuses to advance when model-closed)
- [ ] If new prompts added, they follow the four-part grammar (role/stakes, input/constraints, process, anti-patterns)
- [ ] If new slash commands added, they're listed in `README.md` and `plugin.json`

## For major releases (x.0.0)

Additional checks:

- [ ] Migration guide in `CHANGELOG.md` for users on the prior major version
- [ ] Any deprecated skills or commands explicitly flagged in `CHANGELOG.md`
- [ ] Backward-compatibility breakage documented in README

## Pushing to GitHub

```bash
# From the plugin directory
git status                                    # confirm clean working tree (except staged changes)
git add .
git commit -m "Release v0.x.y: <one-line summary>"
git tag v0.x.y
git push origin main
git push origin v0.x.y
```

For the very first release (v0.1.0):

```bash
git init
git add .
git commit -m "Initial commit: v0.1.0"
git branch -M main
git remote add origin https://github.com/bbulman/synthesis-playbook.git
git push -u origin main
git tag v0.1.0
git push origin v0.1.0
```

## Submitting to the Claude Code plugin marketplace

After pushing to GitHub:

1. Visit the Claude Code plugin marketplace submission page
2. Submit the repo URL: `https://github.com/bbulman/synthesis-playbook`
3. Plugin marketplace reviewers will check:
   - `.claude-plugin/plugin.json` is valid
   - At least one `SKILL.md` exists
   - README is present
   - LICENSE is present
4. After approval, users can install via `/plugin marketplace add bbulman/synthesis-playbook`

## After publishing

- [ ] Update the book's Chapter 11 to reference the plugin (if not done already)
- [ ] Update Workshopr.io to link to the plugin repo
- [ ] Substack announcement post (using the substack-writer skill)
- [ ] Social-media announcement (LinkedIn, X)

## Disclosure reminder

Every public mention of the plugin should include the Workshopr.io COI disclosure that's already in README:

> *I run Workshopr.io, which sells a hosted version of these recipes. This plugin is the open, platform-neutral version.*

Per the book's own discipline.

## Source

This document is original to the plugin. The release checklist patterns are adapted from common open-source publishing practice.
