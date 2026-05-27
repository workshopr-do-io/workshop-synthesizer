# Changelog

All notable changes to the Synthesis Playbook plugin.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). This plugin uses semantic versioning.

## [Unreleased]

### Planned for 0.2.0
- Worked-example fixtures for each recipe (sanitized test data you can run the plugin against)
- A `/synthesis-portable` command that exports a current synthesis as the book's Notion-brief shape
- Cross-recipe handoff support (one synthesis informing the next)

---

## [0.1.0] — 2026-05-27

Initial release. Companion to *The Synthesis Playbook* (Workshopr facilitation series, Book 6).

### Added

- **8 sub-skills:**
  - `synthesis-framework` — the four moves, synthesis stack, Stakes × Politics matrix, "human-authored, machine-assisted" principle, consent and data guidance
  - `synthesis-discovery` — Discovery & qualitative synthesis recipe (Ch 4)
  - `synthesis-offsite` — Strategic offsite & stakeholder politics recipe (Ch 5)
  - `synthesis-sprint` — Design sprint synthesis recipe (Ch 6)
  - `synthesis-ideation` — Ideation & roadmap synthesis recipe (Ch 7)
  - `synthesis-retro` — Retro & post-mortem synthesis recipe (Ch 8)
  - `synthesis-training` — Training debrief synthesis recipe (Ch 9)
  - `synthesis-prompt-library` — The twelve workhorses + four-part grammar + aloud test (Ch 10)

- **7 slash commands:**
  - `/ws-help` (index + decision tree)
  - `/ws-discovery`
  - `/ws-offsite`
  - `/ws-sprint`
  - `/ws-ideation`
  - `/ws-retro`
  - `/ws-training`

- **26 prompts** (verbatim from the book's appendix), organized by recipe folder in `prompts/`. Workhorses cross-listed in `prompts/workhorses/`.

- **One pipeline agent** (`synthesis-discovery/agents/discovery_pipeline_agent.md`) implementing the Ch 11 agentic pipeline for the Discovery recipe — 8 steps with human pauses at [INTERPRET] and [PRIORITIZE]. Pipeline agents for the other 5 recipes follow the same pattern; see each recipe's `agents/` folder.

- **Documentation:**
  - `README.md` — install, quick start, decision tree
  - `CONTRIBUTING.md` — how to add prompts and recipes
  - `SECURITY.md` — consent/data discipline, vulnerability reporting
  - `docs/ARCHITECTURE.md` — how the plugin is wired
  - `docs/using-without-claude-code.md` — copy-paste path for any LLM
  - `docs/publishing-checklist.md` — release process
  - `docs/relationship-to-book.md` — chapter → skill map

### Known limitations

- Plugin tested against Claude Code as of May 2026 with Claude 4.x and ChatGPT-5-class models. Prompt behavior across other models is unverified at release.
- Pipeline agents read from local files via the standard Read tool. Cloud-source ingestion (Granola, Fireflies, Notion) is not in v0.1.
- Worked examples in the book's appendix are composites; the plugin does not ship fixture data. That's coming in v0.2.

### Disclosure

- The model assisted with this plugin's scaffolding (directory layout, frontmatter conventions, prompt-extraction from the manuscript). The 26 prompts themselves are verbatim from the book and human-authored. The SKILL.md content, pipeline agent logic, and documentation prose are model-drafted and human-edited.
- I (Bill Bulman) have a commercial interest in [Workshopr.io](https://workshopr.io), which sells a hosted version of these recipes. This plugin is the open, platform-neutral version. See README for full COI disclosure.

[Unreleased]: https://github.com/bbulman/synthesis-playbook/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/bbulman/synthesis-playbook/releases/tag/v0.1.0
