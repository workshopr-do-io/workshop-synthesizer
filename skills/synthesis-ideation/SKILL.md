---
name: synthesis-ideation
description: >
  Synthesize a half-day or one-day ideation workshop, brainstorming session,
  or quarterly roadmap session. 200 stickies become a ranked shortlist of
  8–15 ideas with rationale, a "killed and why" list, and a recommended
  next step per top idea. Prioritize-dominant recipe. Use when the user
  has just run an ideation room and needs to commit to a small set of
  bets. Triggers on: "synthesize ideation", "ideation readout", "200
  stickies", "ranked shortlist", "kill list", "roadmap synthesis",
  "dot-vote", "HMW prompts".
---

# Ideation & Roadmap Synthesis Recipe

> **Move mix:** 20% [CLUSTER] · 15% [INTERPRET] · 50% [PRIORITIZE] · 15% [NARRATE]
> **Dominant move:** [PRIORITIZE]

The room hands you volume; you hand back commitments. Two hundred stickies turn into twelve ideas, ranked, with next steps and a kill list. The dots are seductive. The criteria are trustworthy. When they disagree, the criteria usually win — but you keep one hot-but-weak idea for political reasons and one cool-but-strong idea for synthesis credibility.

## When to use this recipe

- Half-day or one-day ideation workshops
- Brainstorming sessions with HMW (How Might We) prompts
- Idea-generation offsites
- Quarterly roadmap sessions (see Roadmap variant — adds sequencing)

## When NOT to use this recipe

- Pre-ideation discovery (use `synthesis-discovery`)
- Design sprints with prototype testing (use `synthesis-sprint`)
- Strategic decision sessions without idea generation (use `synthesis-offsite`)

## The workflow at a glance

1. **Dedupe and tighten** — [CLUSTER] Three-pass prompt: dedupe near-duplicates → tighten vague entries to noun-verb-object → re-cluster across HMW prompts. ~80 concepts from 200 stickies.
2. **Apply the criteria explicitly** — [PRIORITIZE] Score each idea against the team-agreed criteria (impact, feasibility, novelty, time-to-test). Ignore dot-vote at this stage.
3. **Dots-vs-criteria tension surfacer** — [PRIORITIZE] Find the hot-but-weak and cool-but-strong ideas. These are where the synthesis earns its keep.
4. **Pick the shortlist** — [PRIORITIZE] 8–15 ideas, ranked. Rules: top three non-negotiable, include one cool-but-strong, at most one hot-but-weak, include one weird outlier, stop at 15.
5. **The kill list** — [PRIORITIZE → NARRATE] Categorized: already in flight / too dependent / low signal / out of scope / mergeable / speculative / politically hard.
6. **Next-step recommendations** — [NARRATE] Per shortlist item: prototype / research / commit / monitor.
7. **Draft the readout** — [NARRATE] One-pager + longer doc + optional deck.

For roadmap workshops: **Step 4.5 — Sequencing critic.** Identifies dependency, resourcing, market-timing, and organizational-readiness constraints. See [`references/roadmap-variant.md`](references/roadmap-variant.md).

Full step-by-step: [`references/workflow.md`](references/workflow.md).

## The prompts (5–6, depending on variant)

| # | Prompt | Used at |
|---|---|---|
| 10 | Sticky deduper-and-clusterer (three-pass) | Step 1 [CLUSTER] |
| 11 | Criteria applicator | Step 2 [PRIORITIZE] |
| 12 | Dots vs. criteria tension surfacer | Step 3 [PRIORITIZE] |
| 13 | Kill list reasoner | Step 5 [PRIORITIZE → NARRATE] |
| 14 | Sequencing critic (roadmap variant) | Step 4.5 — roadmap only |
| 6 | Argue-the-other-side critic | Anywhere a contested cut needs a sanity check |

Verbatim text: [`references/prompts.md`](references/prompts.md). Copy-paste: [`../../prompts/ideation/`](../../prompts/ideation/).

## Reference files

| File | Load when... |
|---|---|
| [`references/workflow.md`](references/workflow.md) | Running the recipe end-to-end |
| [`references/prompts.md`](references/prompts.md) | Need the 5–6 prompts in one place |
| [`references/pitfalls.md`](references/pitfalls.md) | Tired and scoring softly; killing weird outliers; shortlist creeping past 15 |
| [`references/worked-example.md`](references/worked-example.md) | Want to see what a 200→12 synthesis looks like (B2B composite) |
| [`references/roadmap-variant.md`](references/roadmap-variant.md) | Quarterly roadmap session — adds sequencing as a fifth criterion |
| [`references/weird-outlier-rule.md`](references/weird-outlier-rule.md) | The rule that every shortlist gets one weird outlier, and why |

## Pipeline agent

[`agents/ideation_pipeline_agent.md`](agents/ideation_pipeline_agent.md) implements the 7-step workflow. Pauses at Step 4 (you pick the shortlist) — the model can sanity-check, but committing is yours.

## Where AI hurts

- **The final shortlist pick.** Model ranks. Model cannot commit. The choice carries weight the model doesn't.
- **The weird-outlier inclusion.** Model won't recommend keeping a low-scoring idea. The judgment that the outlier deserves a research-first slot is yours.
- **The politically-hard kill category.** Model can guess politics but can't read the room. Categorize politically-hard kills by hand.

## The bottom line

Two hundred stickies into twelve commitments. The dots are seductive. The criteria are trustworthy. Every shortlist has a weird outlier — not decoration, the move that tells the team you read the session generously.

For roadmap variants: a roadmap that ranks well but doesn't sequence well is a broken roadmap. Run the sequencing critic before you publish.

## Source

*The Synthesis Playbook*, Chapter 7 "Ideation & roadmap synthesis." Worked example (200-to-12, B2B product company composite).
