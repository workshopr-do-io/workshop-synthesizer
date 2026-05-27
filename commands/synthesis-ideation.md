---
description: Run the Ideation & Roadmap synthesis recipe — turns 200 stickies into a ranked shortlist (8–15 ideas), a kill list, and a next-step plan. Use after half-day ideation workshops, brainstorms, or roadmap sessions.
---

Invoke the `synthesis-ideation` skill. Use the recipe to walk the user through synthesizing a half-day ideation session, brainstorm, or roadmap workshop into a ranked shortlist with rationale.

## The recipe (Move mix: 20% [CLUSTER] · 15% [INTERPRET] · 50% [PRIORITIZE] · 15% [NARRATE])

Seven steps:

1. Dedupe and tighten ([CLUSTER]) — Prompt #10 — three passes
2. Apply criteria explicitly ([PRIORITIZE]) — Prompt #11 — ignore dot-vote
3. Dots-vs-criteria tension surfacer ([PRIORITIZE]) — Prompt #12
4. **Pick the shortlist ([PRIORITIZE])** — *human-authored cut to 8–15*
5. The kill list ([PRIORITIZE → NARRATE]) — Prompt #13 — categorized
6. Next-step recommendations ([NARRATE]) — prototype / research / commit / monitor
7. Draft the readout ([NARRATE]) — one-pager + longer doc

For **roadmap workshops**, add Step 4.5: sequencing critic ([PRIORITIZE]) — Prompt #14.

## The shortlist rules

When you reach Step 4:

- **Top three are non-negotiable** — score top on criteria + executable
- **Include at least one cool-but-strong** — the unsung idea
- **Include at most one hot-but-weak** — political signal honored
- **Include at least one weird outlier** — the idea the team would never have generated alone
- **Stop at 15** — past 15 it stops being a shortlist

## Variants

- **Roadmap workshop** — sequencing as a fifth criterion; the sequencing critic catches the "Now bucket fills with top-rated items regardless of whether they can start" failure
- **Internal facilitator** — run the criteria applicator with 2–3 teammates in the room; the hot-but-weak cut is politically hard internally

## How to invoke

Ask for: the sticky export (CSV with sticky text, HMW prompt, room-grouped cluster, dot count), the HMW prompts the session was structured around, the agreed evaluation criteria, dot-vote tally, a note on which voices were loudest and which quietest.

Invoke the pipeline agent in `skills/synthesis-ideation/agents/ideation_pipeline_agent.md`.

## Where AI is closed

- Step 4 (final shortlist pick) — committing is yours
- Weird-outlier inclusion judgment — the model won't recommend keeping a low-scoring idea
- Politically-hard kill category — the model guesses politics; you read the room

## Source

`skills/synthesis-ideation/SKILL.md` — full skill description and references.

Book chapter: *The Synthesis Playbook* Chapter 7, "Ideation & roadmap synthesis."
