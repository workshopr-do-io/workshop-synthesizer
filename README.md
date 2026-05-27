# Workshop Synthesis for Claude Code

[![Version](https://img.shields.io/badge/version-v0.1.0-blue)](https://github.com/workshopr-do-io/workshop-synthesizer/releases/tag/v0.1.0)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Companion to the book](https://img.shields.io/badge/companion-The%20Synthesis%20Playbook-orange)](https://workshopr.io)

A Claude Code plugin that runs the recipes from Bill Bulman's book *The Synthesis Playbook* (Workshopr facilitation series, Book 6) — for turning workshop outputs into defensible client decisions.

**Install in 30 seconds** (Claude Code CLI / VS Code / JetBrains):

```text
/plugin marketplace add workshopr-do-io/workshop-synthesizer
/plugin install workshop-synthesizer
```

Then try `/ws-help` to see the decision tree, or jump straight to `/ws-discovery` if you just ran customer interviews.

> **The recipe runs the recipe. You author the call.** This plugin doesn't write your synthesis for you. It handles the mechanical work — clustering, anti-flattening, draft transitions, audience-tiered framing — so you can focus on the parts that need your judgment: the interpretation, the priority call, the political read, the sentence at the top of the deck.

### Why human-in-the-loop, not full automation?

Every pipeline agent in this plugin **pauses at named human-authorship checkpoints** — the `[INTERPRET]` move, the `[PRIORITIZE]` move, the call slide, the personalized paragraph. It refuses to advance past those steps with model assistance. That's by design.

The book's Chapter 11 ("A gentle on-ramp to agents") describes the pattern. The agent is good at the recipe; the agent is not good at the engagement. An agent that runs the discovery recipe end-to-end produces output that's **80% of what you'd produce manually**. The remaining 20% — the unexpected interpretation that requires you to remember interview nineteen, the political read on which opportunity area the CPO can stomach, the call slide phrased exactly right — does not fit inside an agent.

The plugin's job is to remove the paste-and-wait labor so the human's time goes to the parts that need a human.

---

## What's in the box

### 8 skills

| Skill | What it does | Book chapter |
|---|---|---|
| `synthesis-framework` | The four moves, the synthesis stack, the Stakes × Politics matrix, "human-authored, machine-assisted" | Chs 1–3 |
| `synthesis-discovery` | Customer discovery synthesis (14+ interviews → opportunity areas) | Ch 4 |
| `synthesis-offsite` | Strategic offsite synthesis (CEO memo + board deck + confidential appendix) | Ch 5 |
| `synthesis-sprint` | Design sprint synthesis (Decide vote + 5 user tests → Monday recommendation) | Ch 6 |
| `synthesis-ideation` | Ideation/roadmap synthesis (200 stickies → ranked shortlist + kill list) | Ch 7 |
| `synthesis-retro` | Retro/post-mortem synthesis (dissent preservation, blame-vs-cause) | Ch 8 |
| `synthesis-training` | Training debrief (3 audiences: participants, program owner, budget-holder) | Ch 9 |
| `synthesis-prompt-library` | Twelve workhorses + four-part prompt grammar + aloud test | Ch 10 |

### 7 slash commands

```
/ws-help                Index + decision tree — start here
/ws-discovery           Run the Discovery recipe
/ws-offsite             Run the Strategic Offsite recipe
/ws-sprint              Run the Design Sprint recipe
/ws-ideation            Run the Ideation/Roadmap recipe
/ws-retro               Run the Retro/Post-mortem recipe
/ws-training            Run the Training Debrief recipe
```

See [`MODE_REGISTRY.md`](MODE_REGISTRY.md) for all recipes, modes, and variants.

### 26 prompts

Every prompt from the book's appendix in copy-paste form, organized by recipe in [`prompts/`](prompts/):

- [`prompts/workhorses/`](prompts/workhorses) — the 10 most-reused prompts + 2 disciplines (aloud test, audience-tiered narrator)
- [`prompts/discovery/`](prompts/discovery) — 7 prompts (#1–4, #24–26)
- [`prompts/offsite/`](prompts/offsite) — 3 prompts (#5–7)
- [`prompts/sprint/`](prompts/sprint) — 2 prompts (#8–9)
- [`prompts/ideation/`](prompts/ideation) — 5 prompts (#10–14)
- [`prompts/retro/`](prompts/retro) — 5 prompts (#15–19)
- [`prompts/training/`](prompts/training) — 4 prompts (#20–23)

Each prompt file is verbatim from the book's appendix with `[bracket]` variables marked. **They work in any long-context LLM** — copy-paste into ChatGPT or Claude.ai if you don't run Claude Code.

### 6 pipeline agents

One per recipe (under `<skill>/agents/`). Each implements the Chapter 11 agentic-pipeline pattern: automated steps with human-authorship pauses at the `[INTERPRET]` and `[PRIORITIZE]` checkpoints (and at the personalized-paragraph step in training, and the confidential-appendix step in offsite).

---

## Architecture & pipeline

**👉 [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md)** — the full plugin view: file tree, how a slash command flows through the plugin, how skills reference each other, how pipeline agents pause at human-authored steps.

## Quick decision tree

```
You just walked out of a workshop. Which recipe?

Customer discovery, user interviews, CAB, persona work       → /ws-discovery
Executive offsite, board strategy day, founder/board         → /ws-offsite
GV-style design sprint, prototype validation                 → /ws-sprint
Half-day ideation, brainstorm, roadmap workshop              → /ws-ideation
Team retro, sprint retro, blameless post-mortem              → /ws-retro
Multi-day training, cohort program, cross-functional         → /ws-training

Don't know which fits?                                       → /ws-help
```

---

## Quick install

**Prerequisites:**

- [Claude Code](https://docs.claude.com/en/docs/claude-code/setup) (latest)
- An Anthropic API key, OpenAI key, or model provider configured in Claude Code
- *Optional:* a synthesis-ready file template stored somewhere stable (see `synthesis-framework/references/synthesis-ready-file.md`)

**Plugin install (recommended):**

```text
/plugin marketplace add workshopr-do-io/workshop-synthesizer
/plugin install workshop-synthesizer
```

**Verify it works:** run `/ws-help` — you should see a decision tree pointing at the six recipes.

For direct-clone install or installing without Claude Code, see [`QUICKSTART.md`](QUICKSTART.md).

---

## Use without the plugin

Every prompt in [`prompts/`](prompts/) works in any long-context LLM. The plugin is the convenient runner; the prompts are the product.

See [`docs/using-without-claude-code.md`](docs/using-without-claude-code.md) for the copy-paste path.

---

## Use with the book

The book and the plugin are designed to be used together. The book teaches the moves and the rationale. The plugin runs the workflow. If you find a recipe in the book that the plugin handles oddly, **the book is the source of truth** — read the chapter again, then file an issue.

Book: [*The Synthesis Playbook*](https://workshopr.io) by Bill Bulman, available on Amazon KDP, Apple Books, and the Workshopr.io site.

See [`docs/relationship-to-book.md`](docs/relationship-to-book.md) for the full chapter-to-skill map.

---

## Conflict of interest

The author runs [Workshopr.io](https://workshopr.io), which sells a hosted version of these recipes. This plugin is the open, platform-neutral version. Both can be true at the same time.

See [NOTICE.md](NOTICE.md) for the full COI disclosure and [POSITIONING.md](POSITIONING.md) for what the plugin is (and isn't).

---

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md). Prompt improvements welcome via PR. New workshop-type recipes — open an issue first so we can scope it. The book's discipline is to keep "where AI helps" and "where AI hurts" in balance; PRs that only document failure modes will be asked to balance the framing.

## License

[MIT](LICENSE). The prompts and recipes are yours to copy, adapt, and steal. If you build a version that works better than mine, I want to see it. Send it. I'll print it out and steal it back.

---

## Patterned after

This plugin's structure follows the [`academic-research-skills`](https://github.com/Imbad0202/academic-research-skills) pattern by Cheng-I Wu — multi-skill plugin with mode registry, pipeline agents, and platform-neutral prompt library. Thanks for the template.

---

*The Synthesis Playbook plugin — v0.1.0, May 2026. By [Bill Bulman](https://workshopr.io). Pick up the pan.*
