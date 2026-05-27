# Relationship to The Synthesis Playbook (the book)

This plugin is the executable companion to Bill Bulman's book *The Synthesis Playbook* (Workshopr facilitation series, Book 6).

## The chapter-to-skill map

| Book chapter | Plugin location | What lives there |
|---|---|---|
| Front matter — How to use this book | `README.md` decision tree | The "which recipe do I use" lookup |
| Front matter — A note on numbers | (preserved by design discipline) | The plugin doesn't ship numbers; the reference files do, with composite tags where applicable |
| Front matter — How this book was made | `CHANGELOG.md` disclosure section | The plugin discloses its own AI use the same way the book does |
| Front matter — Consent and data | `synthesis-framework/references/consent-and-data.md` | Verbatim — read before pasting client material |
| Intro — The Sunday you stop dreading | — | The narrative intro doesn't ship in the plugin; read the book for it |
| Ch 1 — Synthesis is a craft, not a summary | Woven into `synthesis-framework/SKILL.md` intro | Foundation |
| Ch 2 — The four moves | `synthesis-framework/references/four-moves.md` | The taxonomy |
| Ch 3 — Your synthesis stack | `synthesis-framework/references/synthesis-ready-file.md`, `stakes-politics-matrix.md`, `human-authored-machine-assisted.md` | The stack + matrix + principle |
| Ch 4 — Discovery & qualitative synthesis | `synthesis-discovery/` + `prompts/discovery/` | The discovery recipe + 7 prompts + Mid-Co composite |
| Ch 5 — Strategic offsite & stakeholder politics | `synthesis-offsite/` + `prompts/offsite/` | The offsite recipe + 3 prompts + Reset-Co composite |
| Ch 6 — Design sprint synthesis | `synthesis-sprint/` + `prompts/sprint/` | The sprint recipe + 2 prompts + swipe-or-not composite |
| Ch 7 — Ideation & roadmap synthesis | `synthesis-ideation/` + `prompts/ideation/` | The ideation recipe + 5 prompts + 200-to-12 composite |
| Ch 8 — Retro & post-mortem synthesis | `synthesis-retro/` + `prompts/retro/` | The retro recipe + 5 prompts + trust-sticky composite |
| Ch 9 — Training & workshop debrief synthesis | `synthesis-training/` + `prompts/training/` | The training recipe + 4 prompts + first-time-manager-cohort composite |
| Ch 10 — Your reusable prompt library | `synthesis-prompt-library/` + `prompts/workhorses/` | The twelve workhorses + four-part grammar + versioning + extending pattern |
| Ch 11 — A gentle on-ramp to agents | The 6 pipeline agents in `skills/<recipe>/agents/` | The agentic pipeline pattern instantiated for each recipe |
| Ch 12 — Client-facing artifacts | `prompts/workhorses/audience-tiered-narrator.md` + `prompts/workhorses/aloud-test.md` | The artifact altitude discipline + the two tests |
| Back matter — Recipe index | `commands/ws-help.md` | The decision tree as a slash command |
| Back matter — Prompt appendix | `prompts/` (all 26 prompts) | The prompts themselves |
| Back matter — About the author | (preserved by reference) | Read the book |

## When the book and the plugin disagree

The book is the source of truth. If a prompt in the plugin drifts from the book's appendix, the book wins — open an issue and the plugin will be brought back into alignment.

The exception: when a model behavior changes (sycophancy, hedging, refusal patterns) the prompts in the plugin may evolve faster than the book can. In those cases the plugin's prompts represent the current-best version; the book's appendix represents the canonical version. The plugin's CHANGELOG will document any deliberate drift.

## What the plugin adds that the book doesn't

- **Pipeline agents.** The book describes the agentic pattern in Chapter 11 but stays platform-neutral. The plugin provides the agents.
- **Slash commands.** Quick invocation of any recipe.
- **Cross-recipe lookup.** The `synthesis-help` command's decision tree.
- **Versioned prompts.** The plugin can update prompts in response to model changes; the book is static after publication.

## What the book has that the plugin doesn't

- **The narrative.** The book is a narrative work, not a reference. Chapters open with kitchen metaphors, walk through the practitioner's experience, and close with kinetic-verb imperatives. The plugin extracts the operational content but loses the prose voice that makes the book a book.
- **The reasoning behind the recipes.** Each chapter explains *why* each step exists. The plugin's reference files summarize this, but the depth lives in the book.
- **The "where AI hurts" sidebars.** These are present in the plugin as recipe-specific references, but the book's longer treatment carries more weight for the harder workshop types (especially the offsite chapter).
- **The author's voice.** The plugin's documentation tries to match it. The book is the source.

## How the two are designed to work together

The reading flow:

1. **Read the book** (or the chapters relevant to your work). 4–10 hours.
2. **Install the plugin** when you have a real engagement to synthesize.
3. **Invoke the recipe via slash command.** The plugin runs the workflow.
4. **Return to the book** when something in the recipe doesn't fit your specific situation. The book covers the variants and the reasoning.

You don't need the book to use the plugin. You don't need the plugin to use the book. They compound when used together.

## When to use one without the other

- **Plugin without book** — you've read another synthesis book (Hall's *Just Enough Research*, Knapp et al.'s *Sprint*, Kerth's *Project Retrospectives*) and want a tactical toolkit. The plugin works.
- **Book without plugin** — you don't use Claude Code, or your engagements are too low-volume to justify the plugin overhead. The book works.

## Disclosure (also in README)

I (Bill Bulman) run [Workshopr.io](https://workshopr.io), which sells a hosted version of these recipes. The book and the plugin are both designed to be useful without Workshopr.io. The platform exists as a third option for practitioners who want the recipes hosted alongside their workshops.

Three surfaces. Same recipes. No lock-in to any one.

## Source

This document is original to the plugin.
