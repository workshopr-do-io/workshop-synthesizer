---
description: Run the Strategic Offsite & Stakeholder Politics recipe — turns an exec offsite into three tiered artifacts (CEO memo, board deck, confidential appendix). The hardest recipe; AI does about 15% of the work.
---

Invoke the `synthesis-offsite` skill. Use the recipe to walk the user through synthesizing an executive offsite, founder/board strategy day, or sensitive cross-leadership decision session into three tiered artifacts.

## The recipe (Move mix: 10% [CLUSTER] · 30% [INTERPRET] · 30% [PRIORITIZE] · 30% [NARRATE])

Eight steps:

1. Structure the decision log ([PREP]) — Prompt #5
2. **Political read ([INTERPRET, model off])** — *model closed; you write by hand*
3. Prioritize decisions across artifacts ([PRIORITIZE]) — Prompt #6 for sanity check
4. Draft the CEO memo ([NARRATE, with model assist]) — Prompt #7
5. Draft the board deck ([NARRATE, with model assist])
6. **Draft the confidential appendix ([NARRATE, model off])** — *model closed; written by hand*
7. Political read pass ([INTERPRET, model off]) — read all 3 artifacts back-to-back
8. In-person handoff ([SOCIAL]) — printed copies, no laptop

## Critical pre-work

Before invoking the recipe, confirm the user wrote a **Day-One Read brief** before sleeping on the first night of the offsite. If they didn't, the synthesis will struggle to recover the political reads from notes that don't carry tone. See `skills/synthesis-offsite/references/day-one-read-brief.md`.

## Variants

- **Founder/board strategy day** — sharper political reads; appendix often longer than memo
- **Internal facilitator** — confidential appendix only after explicit verbal request; in-person handoff non-negotiable

## How to invoke

Ask for: the structured decision log (or raw notes if not structured yet), whiteboard photos, vote results, the user's Day-One Read brief, the deliverable spec (who reads each artifact, by when).

Invoke the pipeline agent in `skills/synthesis-offsite/agents/offsite_pipeline_agent.md`.

## Where AI is closed (do not run the model)

- Step 2 (political read)
- Step 6 (confidential appendix)
- Step 7 (political read pass — final check)

The pipeline agent will refuse to advance these steps with model assistance. That's by design.

## Source

`skills/synthesis-offsite/SKILL.md` — full skill description and references.

Book chapter: *The Synthesis Playbook* Chapter 5, "Strategic offsite & stakeholder politics."
