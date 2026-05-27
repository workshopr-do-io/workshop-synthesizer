# Positioning

## What this is

Workshop Synthesis is an **open, platform-neutral Claude Code plugin** that runs the recipes from Bill Bulman's book *The Synthesis Playbook* (Workshopr facilitation series, Book 6). The reference distribution is a suite of 8 skills, 7 slash commands, and 26 prompts that assist facilitators through the workshop-aftermath workflow — turning interview transcripts, stickies, decision logs, and pulse surveys into defensible client-facing artifacts.

It is licensed under [MIT](LICENSE). The prompts and recipes are designed to be copied, adapted, and improved. If you build a version that works better than the reference, send it back — see [CONTRIBUTING.md](CONTRIBUTING.md).

## What this is not

Workshop Synthesis is **not an autonomous synthesis writer**. It is not a replacement for the facilitator's judgment. It does not claim authorship, and its outputs are not client-ready without human review at the named human-authorship checkpoints.

The plugin is also **not a substitute for the book**. *The Synthesis Playbook* teaches the framework — the four moves, the synthesis stack, the Stakes × Politics matrix, the "human-authored, machine-assisted" principle. The plugin runs the framework. They are designed to be used together.

## Allowed uses

- **Synthesis assistance** for facilitators running consumer discovery, strategic offsites, design sprints, ideation/roadmap workshops, retros/post-mortems, and training debriefs
- **Teaching** facilitation craft: demonstrating the four-moves framework, the anti-flattening discipline, the audience-tier discipline
- **Method training**: using the pipeline agents to scaffold a junior facilitator's first solo synthesis
- **Collaborative use within a firm or team**: prompt library sharing, recipe versioning, cross-collaborator workflows
- **Commercial consulting work**: the MIT license permits commercial use. If the synthesis output goes to a paying client, disclose AI use per the book's Chapter 12 disclosure prescription

## Discouraged uses

- **Submitting AI-generated synthesis as solely human-authored work** without the disclosure framework from the book's Chapter 12
- **Skipping the human-authorship checkpoints** ([INTERPRET], [PRIORITIZE], the call slide, the personalized paragraph). The pipeline agents will refuse to advance past these — but a determined user could bypass them. Don't.
- **Treating AI-generated client artifacts as ready to ship** without the aloud test, the retelling test, and the credibility test from Chapter 12
- **Using the recipes in privacy-constrained settings** (GDPR / HIPAA / FERPA / etc.) without first running the four-question consent-and-data check in [`synthesis-framework/references/consent-and-data.md`](synthesis-framework/references/consent-and-data.md)

## Conflict of interest disclosure

Bill Bulman runs [Workshopr.io](https://workshopr.io), which sells a hosted version of the same recipes alongside the prompt library, the synthesis-ready file template, and the Coach that knows the moves. He has a commercial interest in your trying it.

He also published the book and this plugin as the open, platform-neutral version of the same kit. The book is complete without Workshopr.io. This plugin is too. Both of those statements are true at the same time.

See [NOTICE.md](NOTICE.md) for the full COI disclosure, mirroring the book's Introduction disclosure.

## Relationship to the book

- The book is the **source of truth.** If a prompt in the plugin drifts from the book's appendix, the book wins.
- The plugin is the **executable companion.** It runs the recipes the book teaches.
- See [docs/relationship-to-book.md](docs/relationship-to-book.md) for the full chapter-to-skill map.

## Relationship to Workshopr.io

- Workshopr.io sells a **hosted version** of the same recipes plus a Coach UI, persistent workspace, and team collaboration features.
- This plugin is **platform-neutral by design** (per Chapter 11 of the book) — it does not call Workshopr.io APIs or require a Workshopr.io account.
- You can use the book, the plugin, and Workshopr.io independently. They compound when used together.

## Compared to other plugins

| Plugin | Domain | Pattern |
|---|---|---|
| [academic-research-skills](https://github.com/Imbad0202/academic-research-skills) | Academic research / paper writing | Multi-skill plugin with mode registry, pipeline orchestrator, integrity gates. **Workshop Synthesis is modeled after this pattern.** |
| Workshop Synthesis (this plugin) | Workshop facilitation / synthesis | 8 skills, 7 commands, 6 pipeline agents. Recipes per workshop type. Framework + prompt library as foundational skills. |

If you've used academic-research-skills, the structure here will feel familiar.

## Versioning policy

- **Patch releases (0.1.x)** — prompt improvements, doc fixes, minor reference content. Backward compatible.
- **Minor releases (0.x.0)** — new recipes, new variants, new pipeline agents. Backward compatible within the major.
- **Major releases (x.0.0)** — structural changes that break existing workflows. Migration guide in CHANGELOG.

See [CHANGELOG.md](CHANGELOG.md) for what's shipped.

## Reporting issues

Bugs, prompt failures, voice drift: open a GitHub issue at https://github.com/bbulman/workshop-synthesizer/issues

Security concerns: see [SECURITY.md](SECURITY.md). Email directly; don't open public issues for security reports.

## Source

This document is original to the plugin. The "platform-neutral by design" framing is lifted from Chapter 11 of *The Synthesis Playbook*.
