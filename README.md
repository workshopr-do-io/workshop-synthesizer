# The Synthesis Playbook — Claude Code Plugin

**AI-assisted recipes for turning workshop outputs into decisions.**

Companion plugin to the book *[The Synthesis Playbook](https://workshopr.io)* (Workshopr facilitation series, Book 6).

The book teaches a four-move synthesis framework — **cluster, interpret, prioritize, narrate** — with six workshop-type recipes and 26 reusable prompts. This plugin packages all of it into Claude Code so you don't have to paste prompts by hand on a Sunday afternoon.

It is platform-neutral by design. The prompts in [`prompts/`](./prompts) work in any LLM — copy-paste them into ChatGPT or Claude.ai if you don't run Claude Code.

---

## A word on what this is, and what it isn't

I (Bill Bulman) run [Workshopr.io](https://workshopr.io), which sells a hosted version of these recipes alongside the prompt library, a synthesis-ready file template, and the Coach that knows the moves. I have a commercial interest in your trying it. I also published the book and this plugin as the open, platform-neutral version of the same kit. The book is complete without Workshopr.io. This plugin is too. Both of those statements are true at the same time.

The plugin runs in Claude Code; the platform runs in your browser; the prompts run anywhere. Pick the surface that matches the volume you do.

---

## Install

### Via Claude Code plugin marketplace (recommended)

```
/plugin marketplace add bbulman/synthesis-playbook
/plugin install synthesis-playbook
```

### Via direct clone

```bash
git clone https://github.com/bbulman/synthesis-playbook ~/.claude/plugins/cache/synthesis-playbook
```

Then restart Claude Code.

### Without Claude Code (any LLM)

Browse [`prompts/`](./prompts) and copy whichever prompt fits your workshop. The four-part prompt grammar at the bottom of [`prompts/README.md`](./prompts/README.md) explains how to adapt them.

---

## What's in the box

### Eight skills

| Skill | Covers | Book chapter |
|---|---|---|
| `synthesis-framework` | The four moves, the synthesis stack, the Stakes × Politics matrix, "human-authored, machine-assisted" | Chs 1–3 |
| `synthesis-discovery` | Customer discovery synthesis: 14+ interviews → opportunity areas + insight statements | Ch 4 |
| `synthesis-offsite` | Strategic offsite synthesis: 5 executives → CEO memo + board deck + confidential appendix | Ch 5 |
| `synthesis-sprint` | Design sprint synthesis: Decide vote + 5 user tests → Monday recommendation | Ch 6 |
| `synthesis-ideation` | Ideation/roadmap synthesis: 200 stickies → ranked shortlist + kill list | Ch 7 |
| `synthesis-retro` | Retro/post-mortem synthesis: dissent preservation, blame-vs-cause | Ch 8 |
| `synthesis-training` | Training debrief synthesis: 3 audiences (participants, program owner, budget-holder) | Ch 9 |
| `synthesis-prompt-library` | The twelve workhorses, the four-part prompt grammar, the aloud test | Ch 10 |

### Seven slash commands

```
/synthesis-help              Index + decision tree — start here
/synthesis-discovery         Run the Discovery recipe
/synthesis-offsite           Run the Strategic Offsite recipe
/synthesis-sprint            Run the Design Sprint recipe
/synthesis-ideation          Run the Ideation/Roadmap recipe
/synthesis-retro             Run the Retro/Post-mortem recipe
/synthesis-training          Run the Training Debrief recipe
```

### 26 prompts

Every prompt from the book's appendix, organized by recipe in [`prompts/`](./prompts):

- [`prompts/workhorses/`](./prompts/workhorses) — the 10 most-reused prompts plus two disciplines (audience-tiered narrator, the aloud test)
- [`prompts/discovery/`](./prompts/discovery) — 7 prompts (#1–4, #24–26)
- [`prompts/offsite/`](./prompts/offsite) — 3 prompts (#5–7)
- [`prompts/sprint/`](./prompts/sprint) — 2 prompts (#8–9)
- [`prompts/ideation/`](./prompts/ideation) — 5 prompts (#10–14)
- [`prompts/retro/`](./prompts/retro) — 5 prompts (#15–19)
- [`prompts/training/`](./prompts/training) — 4 prompts (#20–23)

Each prompt file is verbatim from the book's appendix with the `[bracket]` variables marked clearly.

---

## A quick decision tree

```
You just walked out of a workshop. Which recipe?

Discovery sprint, customer research, persona work       → /synthesis-discovery
Executive offsite, board strategy day, founder/board    → /synthesis-offsite
GV-style design sprint, prototype test, mini-sprint     → /synthesis-sprint
Half-day ideation, brainstorm, roadmap workshop         → /synthesis-ideation
Quarterly retro, sprint retro, blameless post-mortem    → /synthesis-retro
Multi-day training, cohort program, cross-functional    → /synthesis-training

Don't know which fits?                                  → /synthesis-help
```

---

## How each recipe runs

Each slash command walks you through the recipe's workflow with the four moves tagged inline: **[CLUSTER]**, **[INTERPRET]**, **[PRIORITIZE]**, **[NARRATE]**. At the [INTERPRET] and [PRIORITIZE] steps the agent pauses — those are the human-authored moves. You write the interpretation, you make the prioritization call, then the agent picks up and runs the rest.

This isn't an "agent that does the whole synthesis." That output is slop and the client will smell it. This is the agent doing the paste-and-wait labor so you can do the parts that need you in the room.

---

## Use without the plugin

Every prompt in [`prompts/`](./prompts) works in vanilla ChatGPT, Claude.ai, or any long-context model. Browse the folder, copy the prompt, replace the `[brackets]`. The plugin is the convenient runner. The recipes are yours.

---

## Use with the book

The book and the plugin are designed to be used together. The book teaches the moves and the rationale. The plugin runs the workflow. If you find a recipe in the book that the plugin handles oddly, the book is the source of truth — read the chapter again, then file an issue and tell me what's drifting.

Book: [`The Synthesis Playbook`](https://workshopr.io) — also available on Amazon KDP, Apple Books, and the Workshopr.io site.

---

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md). Short version: prompt improvements welcome via PR. New workshop-type recipes — open an issue first so we can scope it. Don't add a new "where AI hurts" section without a "where AI helps" pair; the book's discipline is to keep them in balance.

## License

MIT. See [`LICENSE`](./LICENSE). The prompts and recipes are yours to copy, adapt, and steal. If you build a version that works better than mine, I want to see it. Send it. I'll print it out and steal it back.

## Where this work continues

The recipes in this plugin all run in vanilla Claude Code. They don't require any specific tooling beyond what you already have.

If you do this work professionally and find yourself reaching for the recipes often, there's a hosted version inside [Workshopr.io](https://workshopr.io) — same recipes, less setup, your library and your workshops in one place. You don't need it. The plugin is complete on its own.

---

*The Synthesis Playbook plugin — v0.1.0, May 2026. By [Bill Bulman](https://workshopr.io). Pick up the pan.*
