---
description: Run the Discovery & Qualitative Synthesis recipe — turns interview transcripts and stakeholder stickies into opportunity areas, insight statements, and recommended next steps. Use after a customer discovery sprint, research round, CAB, or persona/JTBD work.
---

Invoke the `synthesis-discovery` skill. Use the recipe to walk the user through synthesizing a customer discovery sprint, research round, Customer Advisory Board session, or persona/JTBD work into a defensible readout.

## The recipe (Move mix: 30% [CLUSTER] · 40% [INTERPRET] · 10% [PRIORITIZE] · 20% [NARRATE])

Eight steps:

1. Prepare transcripts ([CLUSTER prep])
2. First-pass cluster ([CLUSTER]) — Prompt #1
3. **Anti-flattening pass ([CLUSTER critic])** — Prompt #2 — do not skip
4. **Interpretation ([INTERPRET])** — Prompt #3 — *human-authored pause*
5. Opportunity framing ([INTERPRET → NARRATE]) — Prompt #4
6. Prioritization ([PRIORITIZE]) — model closed
7. Narrative ([NARRATE]) — draft the readout deck + brief
8. Aloud test

## Variants

- **Customer Advisory Board** — add cross-session deduper (Prompt #24) before Step 4
- **Persona / JTBD** — replace Step 2 with the archetype clusterer (Prompt #25), add archetype tension finder (Prompt #26)
- **Internal facilitator** — see the IF YOU'RE INTERNAL guidance in `skills/synthesis-discovery/references/workflow.md`

## Human pauses

The pipeline pauses at Step 4 (you write the interpretations by hand) and Step 6 (you pick the shortlist by hand). The model is your assistant, not your author. Your name is on the deck.

## How to invoke

If the user has a synthesis-ready file ready (interview transcripts, sticky exports, hypothesis): ask for the file path, invoke the pipeline agent in `skills/synthesis-discovery/agents/discovery_pipeline_agent.md`, and run end-to-end.

If they don't have a file ready yet: walk them through the synthesis-ready file template from `synthesis-framework` first.

## Source

`skills/synthesis-discovery/SKILL.md` — full skill description and references.

Book chapter: *The Synthesis Playbook* Chapter 4, "Discovery & qualitative synthesis."
