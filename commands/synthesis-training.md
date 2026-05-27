---
description: Run the Training & Workshop Debrief synthesis recipe — turns a multi-day cohort program into three audience-tiered artifacts (participant write-up with personalized paragraphs, cohort analysis, budget one-pager). Use after leadership programs, cohort-based training, or cross-functional alignment workshops.
---

Invoke the `synthesis-training` skill. Use the recipe to walk the user through synthesizing a multi-day training, cohort program, or cross-functional alignment workshop for three audiences at once.

## The recipe (Move mix: 15% [CLUSTER] · 35% [INTERPRET] · 20% [PRIORITIZE] · 30% [NARRATE])

Seven steps:

1. **Build the baseline-to-close pair ([INTERPRET prep])** — *human-authored, one per participant*
2. Identify the cohort's pattern ([CLUSTER → INTERPRET]) — Prompt #20
3. Identify program-design signals ([INTERPRET]) — Prompt #21
4. **Participant write-up ([NARRATE])** — *human-authored personalized paragraph per participant*
5. **Cohort-level analysis ([NARRATE])** — *human-authored flags section*
6. **Budget-holder one-pager ([NARRATE])** — *human-authored named stories*
7. Aloud test, three times — one per audience

For **cross-functional alignment workshops**, swap Steps 2 and 3 for:

- Position-mapper across functions — Prompt #22
- Real-disagreement surfacer — Prompt #23

## The audiences

Three artifacts, three altitudes:

1. **Participants** — receive the write-up with their named personalized paragraph
2. **Program owner** (L&D leader) — receives the cohort analysis with flags
3. **Budget-holder** (VP, customer exec) — receives the one-pager with named stories

The temptation is to write the long document first and trim. **Resist.** Trim approach produces three watered-down versions of the same artifact. Write each for its audience.

## The personalized paragraph (Step 4)

The single most authorship-heavy moment in any recipe in this book. Three to five sentences per participant, citing one specific moment from the program. The participant will know if it's generic. The participant will keep the paragraph if it isn't.

Template in `skills/synthesis-training/references/personalized-paragraph-template.md`.

## Variants

- **Sales-team or customer-facing training** — participant write-up gets shorter (1 page); cohort analysis more numbers-heavy
- **Cross-functional alignment workshop** — different audiences (functions, not participants); position-mapper replaces cohort-pattern surfacer
- **Internal facilitator** — personalized paragraphs land politically; flags section may affect colleagues' careers

## How to invoke

Ask for: all facilitation notes, each participant's 30-60-90 plan, pulse survey responses, co-facilitator observation notes, closing-circle recording, pre-program baseline (what each participant said walking in), program design, cohort roster with role/tenure.

The crucial item is the **baseline-to-close pair** — what each participant said at the start vs. at the end. Without it, the synthesis reports on outputs (artifacts produced) instead of outcomes (people changed).

Invoke the pipeline agent in `skills/synthesis-training/agents/training_pipeline_agent.md`.

## Where AI is closed

- Step 1 (baseline-to-close pairs) — your read of distance traveled
- Step 4 (personalized paragraph per participant) — single most authorship-heavy moment
- Step 5 (flags section) — names of below-average participants
- Step 6 (named stories in one-pager) — calibration of detail vs. identifiability

## Source

`skills/synthesis-training/SKILL.md` — full skill description and references.

Book chapter: *The Synthesis Playbook* Chapter 9, "Training & workshop debrief synthesis."
