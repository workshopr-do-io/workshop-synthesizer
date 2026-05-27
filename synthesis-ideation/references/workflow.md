# Ideation & Roadmap Recipe — Full Workflow

> **Move mix:** 20% [CLUSTER] · 15% [INTERPRET] · 50% [PRIORITIZE] · 15% [NARRATE]

200 stickies turn into 12 ranked commitments. The dots are seductive. The criteria are trustworthy. The synthesis lives in the gap.

## Prerequisite: synthesis-ready file

- The sticky export (CSV: sticky text, HMW prompt, room-grouped cluster, dot count)
- The 4–6 HMW prompts the session was structured around
- The team-agreed evaluation criteria (typically: impact, feasibility, novelty, time-to-test)
- The dot-vote tally
- Which voices were loudest and which quietest in the room
- Pre-existing roadmap context: what's already committed for the next quarter

## Step 1 — Dedupe and tighten [CLUSTER]

Run **Prompt #10 (Sticky deduper-and-clusterer)**. Three passes:

1. **Dedupe** — merge near-duplicates
2. **Tighten** — rewrite as specific noun-verb-object
3. **Re-cluster** — group into 8–12 thematic clusters

200 stickies usually collapse to ~80 concept entries after dedupe, ~25–35 distinct ideas after tightening.

## Step 2 — Apply the criteria explicitly [PRIORITIZE]

Run **Prompt #11 (Criteria applicator)**. The model scores each idea on each criterion (High / Medium / Low) and produces a weighted ranked list.

**The model does not use the dot-vote in this step.** The dots tell you what got hot in the room. The criteria tell you what will work.

## Step 3 — Dots-vs-criteria tension surfacer [PRIORITIZE]

Run **Prompt #12 (Dots vs. criteria tension surfacer)**. Surfaces three groups:

- **Hot and good** — easy includes
- **Hot but weak** — heavily dotted but low on criteria (novelty, social momentum, executive enthusiasm)
- **Cool but strong** — lightly dotted but high on criteria (introduced late, quieter voice, looks boring on sticky)

The disagreements are where the synthesis earns its keep.

## Step 4 — Pick the shortlist [PRIORITIZE]

**Model closed.** Pick 8–15 ideas, ranked. Rules from the book:

- **Top three are non-negotiable** — top on criteria + executable
- **Include at least one cool-but-strong** — the unsung idea
- **Include at most one hot-but-weak** — political signal honored
- **Include at least one weird outlier** — the idea the team would never have generated alone
- **Stop at 15**

See [`weird-outlier-rule.md`](weird-outlier-rule.md) for why every shortlist gets one weird outlier.

## Step 4.5 — Sequencing critic (roadmap variant only) [PRIORITIZE]

If this is a roadmap workshop, run **Prompt #14 (Sequencing critic)** to identify dependencies, resource conflicts, market-timing constraints, and organizational-readiness gaps.

See [`roadmap-variant.md`](roadmap-variant.md).

## Step 5 — The kill list [PRIORITIZE → NARRATE]

Run **Prompt #13 (Kill list reasoner)**. For each cut idea, name the primary reason:

- Already in flight
- Too dependent
- Low signal
- Out of scope
- Mergeable (name the shortlist item it folds into)
- Speculative
- Politically hard

The kill list is what makes the shortlist defensible.

## Step 6 — Next-step recommendations [NARRATE]

For each shortlist item:

- **Prototype** — build a small testable thing in 1–2 weeks
- **Research** — talk to N users to validate or sharpen
- **Commit** — skip prototyping; evidence is already strong
- **Monitor** — hold for 90 days

A shortlist where everything is "prototype" is unrealistic — the team won't prototype 10 things in a month. Distribute realistically: at most 3–4 prototypes, 3–4 research items, 1–2 commits, the rest monitor.

## Step 7 — Draft the readout [NARRATE]

One-pager + longer doc + optional deck.

Shape:
1. The shortlist (8–15 items in ranked order with next-step tags)
2. The top three in detail (rationale + next-step plan)
3. The weird outlier (one slide, worth flagging — the room will ask about it)
4. The kill list (organized by category)
5. The dot-vote disagreements (honest about where synthesis diverged from room)
6. Methodology and criteria

## Source

*The Synthesis Playbook*, Chapter 7 "Ideation & roadmap synthesis."
