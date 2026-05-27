---
name: synthesis-training
description: >
  Synthesize a multi-day training program, cohort-based leadership program,
  certification workshop, sales-team training, customer-facing training,
  or cross-functional alignment session into three audience-tiered
  artifacts — a participant write-up (with personalized paragraphs), a
  cohort-level analysis for the program owner, and a budget-defending
  one-pager. The room was the deliverable; the synthesis is the receipt.
  Use when the user has just finished a multi-day program and needs to
  ship for three different readers at once. Triggers on: "synthesize
  training", "training debrief", "cohort report", "participant write-up",
  "L&D readout", "leadership program synthesis", "cross-functional
  alignment synthesis".
---

# Training & Workshop Debrief Synthesis Recipe

> **Move mix:** 15% [CLUSTER] · 35% [INTERPRET] · 20% [PRIORITIZE] · 30% [NARRATE]
> **Dominant moves:** [INTERPRET] + [NARRATE]

Training debriefs sit at an unusual intersection: the deliverable has to land with three audiences at once. Participants want a receipt for what they got. The program owner wants a diagnostic. The budget-holder wants outcomes per dollar. Same source material, three altitudes.

The other thing that makes training different: the room was the deliverable. The training itself produced the transformation. The synthesis isn't reporting on a decision — it's reporting on a change.

## When to use this recipe

- Multi-day training programs (2–5 days)
- Cohort-based leadership development programs
- Certification workshops
- Sales-team training (Sales/Customer variant)
- Customer-facing training (Sales/Customer variant)
- Cross-functional alignment workshops (Cross-Functional variant)

## When NOT to use this recipe

- One-off teaching sessions without a cohort (use `synthesis-discovery` for the feedback round)
- Training-the-trainer sessions (use `synthesis-retro` for the meta-debrief)
- Pure team retros after training (use `synthesis-retro`)

## The workflow at a glance

1. **Build the baseline-to-close pair** — [INTERPRET prep] For each participant: what they said walking in, what they said at close, your read of distance traveled. ~4 hours for 16 participants.
2. **Identify the cohort's pattern** — [CLUSTER → INTERPRET] Sub-cohorts, strongest-movement competency, weakest, participants whose growth direction surprised the design.
3. **Identify program-design signals** — [INTERPRET] Session-by-session: strength signal / friction signal / demonstration vs. discussion.
4. **Participant write-up** — [NARRATE] Six sections including a personalized paragraph for each participant by name. ~4–8 hours.
5. **Cohort-level analysis** — [NARRATE] 6–10 pages. Includes a flags section naming below-average participants.
6. **Budget-holder one-pager** — [NARRATE] One page. Two named stories. One recommended next investment. Names what didn't work.
7. **Aloud test, three times** — [NARRATE check] Read each artifact aloud as if you were its audience.

For cross-functional alignment: **swap Steps 2 and 3 for the position-mapper across functions.** See [`references/cross-functional-variant.md`](references/cross-functional-variant.md).

Full step-by-step: [`references/workflow.md`](references/workflow.md).

## The prompts (4)

| # | Prompt | Used at |
|---|---|---|
| 20 | Cohort-pattern surfacer | Step 2 [CLUSTER → INTERPRET] |
| 21 | Program-design signal extractor | Step 3 [INTERPRET] |
| 22 | Position-mapper across functions | Cross-functional variant only |
| 23 | Real-disagreement surfacer | Cross-functional variant only |

The participant paragraphs, the flags section, and the named stories all come out of your head. The model does not draft these.

Verbatim text: [`references/prompts.md`](references/prompts.md). Copy-paste: [`../../prompts/training/`](../../prompts/training/).

## Reference files

| File | Load when... |
|---|---|
| [`references/workflow.md`](references/workflow.md) | Running the recipe end-to-end |
| [`references/prompts.md`](references/prompts.md) | Need the 4 prompts in one place |
| [`references/pitfalls.md`](references/pitfalls.md) | Personalized paragraphs reading generic; everyone-moved comfort cluster; budget one-pager all flattery |
| [`references/worked-example.md`](references/worked-example.md) | Want to see what a 3-audience synthesis looks like (first-time-manager cohort composite) |
| [`references/personalized-paragraph-template.md`](references/personalized-paragraph-template.md) | Writing the per-participant paragraph that earns its keep |
| [`references/cross-functional-variant.md`](references/cross-functional-variant.md) | Cross-functional alignment workshop instead of training |
| [`references/sales-customer-variant.md`](references/sales-customer-variant.md) | Sales-team or customer-facing training |

## Pipeline agent

[`agents/training_pipeline_agent.md`](agents/training_pipeline_agent.md) implements the 7-step workflow. Pauses at Steps 4, 5, and 6 — the personalized paragraphs and the named stories and the flags section all require your authorship.

## Where AI hurts

- **The personalized paragraph for each participant.** Single most authorship-heavy moment in any recipe. Model produces competent generic versions every time. Participant will know.
- **The flags section.** Below-average participants named with framings of why. Model softens too much or sharpens the wrong way.
- **The named stories in the one-pager.** Anonymized-but-specific stories require human calibration of detail vs. identifiability.
- **The cross-functional position map (variant).** Model can structure from notes. Model cannot tell whether stated disagreement is real disagreement.

## The bottom line

Three audiences, three altitudes, three documents. The participant write-up's personalized paragraph is the receipt the participant keeps. The cohort analysis's flags section is the program owner's tool. The one-pager's named stories are what get re-told in meetings where you won't be in the room.

The baseline-to-close pair is the spine. Spend the time on it. Without it, the synthesis reports on outputs instead of outcomes.

## Source

*The Synthesis Playbook*, Chapter 9 "Training & workshop debrief synthesis." Worked example (first-time-manager cohort, 16 participants, 600-person product company) is a composite.
