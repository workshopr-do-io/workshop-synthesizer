---
name: synthesis-offsite
description: >
  Synthesize an executive offsite, founder-and-board strategy day, or
  sensitive cross-leadership decision session into three tiered artifacts —
  a candid CEO memo, a calmer board deck, and a confidential appendix
  read only by the CEO. The recipe where AI hurts the most and the
  "human-authored, machine-assisted" principle stops being a guideline and
  becomes the whole game. Use when the user has just run a C-suite or
  founder/board working session and needs to capture political reads and
  decision quality without flattening either. Triggers on: "synthesize
  offsite", "strategic offsite synthesis", "exec offsite readout", "board
  strategy day", "CEO memo", "confidential appendix", "decision log".
---

# Strategic Offsite & Stakeholder Politics Recipe

> **Move mix:** 10% [CLUSTER] · 30% [INTERPRET] · 30% [PRIORITIZE] · 30% [NARRATE]
> **Dominant move:** politics-aware mix — three moves nearly equal, [CLUSTER] near-zero.

The hardest recipe in the book. The volume is tiny (5 executives, 12 hours of conversation, often no transcript by choice). The stakes are unusually high (the deliverable shapes a quarter or a year). The politics is most of what matters. AI does maybe 15% of the work. You do the other 85%.

## When to use this recipe

- Executive offsites (5–10 senior leaders, 1–3 days)
- Founder-and-board strategy days
- Sensitive cross-leadership decision sessions
- C-suite alignment sessions where political dynamics carry the deliverable

## When NOT to use this recipe

- Team-level retros (use `synthesis-retro`)
- Cross-functional alignment workshops (use `synthesis-training`'s cross-functional variant)
- Product strategy sessions with no political tension (use `synthesis-discovery` or `synthesis-ideation`)

## The workflow at a glance

1. **Structure the decision log** — [PREP] Clean the co-authored room notes into structured decision entries. ~30 min, model assists.
2. **Political read** — [INTERPRET, model off] You write the political-read note for each decision by hand. The model wasn't in the room. ~60 min.
3. **Prioritize decisions across artifacts** — [PRIORITIZE] Decide which decisions belong in the memo, the deck, the appendix, or all three.
4. **Draft the CEO memo** — [NARRATE, with model assist] Five pages, prose, addressed to the CEO as "you." Model drafts committed-calls section; you write the opening, the unresolved-questions section, and the facilitator's note.
5. **Draft the board deck** — [NARRATE, with model assist] 12–15 slides at board-altitude. No internal pushback in the deck.
6. **Draft the confidential appendix** — [NARRATE, model off] One to two pages, prose, for the CEO alone. Personnel observations, cultural friction, the CEO's own pattern. Written by hand.
7. **Political read pass** — [INTERPRET, model off] Read all three artifacts back-to-back. Catch altitude leaks.
8. **In-person handoff** — [SOCIAL] One-hour debrief with the CEO. Bring printed copies. No laptop. Watch the CEO's face.

Full step-by-step: [`references/workflow.md`](references/workflow.md).

## The prompts (3)

| # | Prompt | Used at |
|---|---|---|
| 5 | Decision log structurer | Step 1 [PREP] |
| 6 | Argue-the-other-side critic | Step 3 [PRIORITIZE] sanity check |
| 7 | CEO memo draft assist | Step 4 [NARRATE] |

Three prompts. That is deliberate. If you find yourself reaching for more, you're trying to outsource judgment that must stay with you. Stop, close the model, write by hand.

Verbatim text: [`references/prompts.md`](references/prompts.md). Copy-paste: [`../prompts/offsite/`](../prompts/offsite/).

## Reference files

| File | Load when... |
|---|---|
| [`references/workflow.md`](references/workflow.md) | Running the recipe end-to-end |
| [`references/prompts.md`](references/prompts.md) | Need the 3 prompts in one place |
| [`references/pitfalls.md`](references/pitfalls.md) | Synthesis is drifting; deck reads like McKinsey |
| [`references/worked-example.md`](references/worked-example.md) | Want to see what a finished tiered synthesis looks like (Reset-Co composite) |
| [`references/day-one-read-brief.md`](references/day-one-read-brief.md) | Template for the political read brief you write before sleeping on the first night of any offsite |

## Pipeline agent

[`agents/offsite_pipeline_agent.md`](agents/offsite_pipeline_agent.md) implements the 8-step workflow with the model closed for steps 2, 6, and 7. The agent will explicitly tell you when to put the model down.

## Where AI hurts — longest sidebar in the book

Six places where the model adds risk in offsite synthesis:

- **Reading the room politically.** The model has no access to body language, tone, sequencing, or relationships.
- **Distinguishing performative dissent from real dissent.** Executives sometimes dissent for positioning, not for substance.
- **Writing in leadership voice.** Generic leadership prose is the model's failure mode.
- **Naming who's right when the room disagreed.** Clean narratives in executive synthesis are dangerous.
- **Predicting durability.** Will this decision hold next week? Model can't answer.
- **The opening sentence of the memo.** This is the sentence the CEO reads first. Write it from scratch.

## The bottom line

Three artifacts at three altitudes. The CEO memo is candid prose. The board deck is calm bullets. The confidential appendix is yours-and-the-CEO's only.

If you take one practical thing: **write your Day-One Read brief before you sleep on the first night of every offsite.** The Sunday synthesis depends on it. There's no recovery if you skip it.

## Source

*The Synthesis Playbook*, Chapter 5 "Strategic offsite & stakeholder politics." Worked example (Reset-Co) is a composite.
