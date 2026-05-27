---
name: synthesis-sprint
description: >
  Synthesize a GV-style design sprint, one-week mini-sprint, or prototype
  validation into a Monday-morning recommendation — ship / iterate /
  abandon / third option. The room hands you a Decide vote and five user
  tests; the synthesis lives in the gap between "enough to call" and
  "enough to know." Use when the user has just finished a Friday user-
  test round and needs a recommendation for the team's Monday standup.
  Triggers on: "synthesize sprint", "design sprint readout", "ship or
  iterate", "Friday user tests", "Monday recommendation", "Decide vote",
  "prototype validation".
---

# Design Sprint Synthesis Recipe

> **Move mix:** 15% [CLUSTER] · 25% [INTERPRET] · 35% [PRIORITIZE] · 25% [NARRATE]
> **Dominant moves:** [PRIORITIZE] + [NARRATE]

The room already did most of the synthesis work — Decide vote, five user tests, decision-stage map. Your job is not to surface themes. Your job is to back the room's vote or call it wrong. Sometimes both at once.

Five user tests is enough to make the call. Five user tests is not enough to feel certain. The synthesis carries that tension.

## When to use this recipe

- GV-style design sprints (4–5 days, ending with Decide + Friday user tests)
- One-week mini-sprints
- Prototype validations outside a sprint container
- Any session ending with a Decide vote and a small-N user test

## When NOT to use this recipe

- Pre-sprint discovery work (use `synthesis-discovery`)
- Ideation sessions without prototype testing (use `synthesis-ideation`)
- Post-launch retros (use `synthesis-retro`)

## The workflow at a glance

1. **Structure the test notes** — [CLUSTER, light] Each tester gets three rows: what worked / what broke / what surprised. Behavioral only, no affective.
2. **Map evidence against hypothesis** — [CLUSTER → INTERPRET bridge] For each tester: Supports / Complicates / Breaks the hypothesis. Tally.
3. **Stress-test your read** — [INTERPRET] The model argues the strongest case that you've overstated the testing evidence.
4. **Draft the Monday recommendation** — [PRIORITIZE → NARRATE] One of four sentences: ship the winner / iterate before shipping / abandon the winner / explore a third option.
5. **Surface what changed your mind** — [NARRATE] The section most sprint syntheses skip. Honors the room's vote even when the testing complicates it.
6. **Risks list** — [NARRATE] Three to five risks, ordered by severity, each with a mitigation.
7. **Draft the readout** — [NARRATE] One-pager plus six-to-eight-slide deck.
8. **Send Sunday night** — [SOCIAL] Not Monday morning. Give the team eight hours to read before they meet.

Full step-by-step: [`references/workflow.md`](references/workflow.md).

## The prompts (2)

| # | Prompt | Used at |
|---|---|---|
| 8 | User-test notes structurer | Step 1 [CLUSTER, light] |
| 9 | Sprint evidence stress-test | Step 3 [INTERPRET] |

Two prompts. That's it. Sprint synthesis is mostly judgment work; the model does light lifting.

Verbatim text: [`references/prompts.md`](references/prompts.md). Copy-paste: [`../../prompts/sprint/`](../../prompts/sprint/).

## Reference files

| File | Load when... |
|---|---|
| [`references/workflow.md`](references/workflow.md) | Running the recipe end-to-end |
| [`references/prompts.md`](references/prompts.md) | Need the 2 prompts in one place |
| [`references/pitfalls.md`](references/pitfalls.md) | About to ship a confirmation-biased recommendation or bury an inconvenient tester |
| [`references/worked-example.md`](references/worked-example.md) | Want to see what a finished recommendation looks like (swipe-or-not composite) |
| [`references/four-recommendations.md`](references/four-recommendations.md) | Choosing between ship / iterate / abandon / third option |

## Pipeline agent

[`agents/sprint_pipeline_agent.md`](agents/sprint_pipeline_agent.md) implements the 8-step workflow. Pauses at Step 4 (you write the recommendation sentence) and Step 5 (you write the "what changed our mind" section). Both are authorship-heavy.

## Where AI hurts

- **The recommendation sentence.** Write it yourself. The model drafts generic versions every time.
- **The "what changed our mind" section.** Political work — tells the team their vote was honored even when testing complicated it. Write it from scratch.
- **The third-option scan.** The model can suggest a fourth option, but trusting it without your own filter ships ideas that are technically valid and politically impossible.

## The bottom line

Five testers is enough to call. Five testers is not enough to know. The synthesis is honest about both.

The four possible recommendations are: ship, iterate, abandon, third option. Most sprints land on iterate. The "what changed our mind" section is what keeps the team in the room after you've complicated their vote.

The recommendation lands Sunday night, not Monday morning, so the team has time to read before they meet.

## Source

*The Synthesis Playbook*, Chapter 6 "Design sprint synthesis." Worked example (swipe-or-not, expense-report approval prototype) is a composite.
