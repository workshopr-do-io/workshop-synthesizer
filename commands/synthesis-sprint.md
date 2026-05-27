---
description: Run the Design Sprint synthesis recipe — turns a Decide vote + 5 user tests into a Monday-morning recommendation (ship / iterate / abandon / third option). Use after GV-style sprints, mini-sprints, or prototype validations.
---

Invoke the `synthesis-sprint` skill. Use the recipe to walk the user through synthesizing a design sprint, mini-sprint, or prototype validation into a single Monday-morning recommendation.

## The recipe (Move mix: 15% [CLUSTER] · 25% [INTERPRET] · 35% [PRIORITIZE] · 25% [NARRATE])

Eight steps:

1. Structure the test notes ([CLUSTER, light]) — Prompt #8
2. Map evidence against hypothesis ([CLUSTER → INTERPRET]) — Supports / Complicates / Breaks
3. Stress-test your read ([INTERPRET]) — Prompt #9
4. **Draft the Monday recommendation ([PRIORITIZE → NARRATE])** — *human-authored sentence*
5. **Surface what changed our mind ([NARRATE])** — *human-authored, political work*
6. Risks list ([NARRATE]) — 3–5 risks, severity, mitigation
7. Draft the readout ([NARRATE]) — one-pager + 6–8 slide deck
8. **Send Sunday night**, not Monday morning

## The four possible recommendations

The Step 4 sentence is one of exactly four:

1. **Ship the winner** — testing supports the hypothesis with minor caveats (rare)
2. **Iterate before shipping** — testing complicates; specific changes would close the gap (most common)
3. **Abandon the winner** — testing breaks the hypothesis structurally (rarer)
4. **Explore a third option** — the room voted on the wrong question entirely (rarest, most valuable when correct)

## Variants

- **Mini-sprint (1 week)** — same recipe, compressed; Decide vote sometimes skipped
- **Prototype validation outside sprint** — same recipe, less political weight; risks list tighter

## How to invoke

Ask for: the 5 user-test notes (raw is fine), the Decide-vote breakdown, the winning sketch description, the sprint hypothesis, the team's pre-existing positions on the call (CEO, product lead, eng lead each may have horses in this race).

Invoke the pipeline agent in `skills/synthesis-sprint/agents/sprint_pipeline_agent.md`.

## Where AI is closed

- Step 4 (recommendation sentence) — write yourself, by hand
- Step 5 (what changed our mind) — political work; from scratch

## Source

`skills/synthesis-sprint/SKILL.md` — full skill description and references.

Book chapter: *The Synthesis Playbook* Chapter 6, "Design sprint synthesis."
