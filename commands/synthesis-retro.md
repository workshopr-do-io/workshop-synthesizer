---
description: Run the Retro & Post-mortem synthesis recipe — turns a team retro or blameless post-mortem into a public write-up that preserves dissent and surfaces patterns without becoming a blame document. Use after team retros, sprint retros, project retros, or incident post-mortems.
---

Invoke the `synthesis-retro` skill. Use the recipe to walk the user through synthesizing a team retro or post-mortem with one rule above all others: **preserve dissent.** The minority view is the data, not the noise.

## The recipe (Move mix: 40% [CLUSTER] · 30% [INTERPRET] · 10% [PRIORITIZE] · 20% [NARRATE])

Seven steps:

1. Structure and cluster ([CLUSTER]) — Prompt #15 — three passes including minority-view extraction
2. Distinguish noise from real dissent ([CLUSTER critic]) — Prompt #16
3. **Interpret linked themes ([INTERPRET])** — *human-authored, one paragraph per theme*
4. **Action items ([PRIORITIZE])** — *human-authored, 3–7 max*
5. Public write-up ([NARRATE]) — Prompt #17 — 6 sections
6. One-page summary ([NARRATE, optional]) — for sharing up
7. **Pre-send check ([SOCIAL])** — to one quiet voice + one loud voice

For **post-mortems**, add Steps 1.5 and 3.5:

- **1.5 — Post-mortem timeline structurer** — Prompt #18 — does NOT impose retrospective clarity
- **3.5 — Cause-vs-blame check** — Prompt #19 — names the system, not the person

## The rule

Word count is a tell. If the most-discussed theme has five times more words than the dissent in your draft write-up, the synthesis has flattened. Aim for proportional weight, not proportional to room time.

## Variants

- **Post-mortem** — incident or failed project; adds timeline + cause-vs-blame; never name the person at the center of the cause
- **Project retro** — adds "what we would have done differently" section without claiming the team should have known better in real time
- **Internal facilitator** — pre-send check is non-optional; flags section requires extra care because participants are colleagues

## How to invoke

Ask for: the sticky export (CSV: sticky text, column, who wrote it if known, dot count), the discussion transcript or recording, vote tally, the feelings-temperature read (if you ran one), pre-existing context (what the team committed to at start of quarter).

Invoke the pipeline agent in `skills/synthesis-retro/agents/retro_pipeline_agent.md`.

## Where AI is closed

- Step 3 (final language on minority views) — model softens too politely
- Step 4 (action item ownership) — model doesn't know who has capacity
- Step 7 (pre-send check) — send to a real person, not the model

## Source

`skills/synthesis-retro/SKILL.md` — full skill description and references.

Book chapter: *The Synthesis Playbook* Chapter 8, "Retro & post-mortem synthesis."
