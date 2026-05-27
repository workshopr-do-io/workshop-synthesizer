# Design Sprint Recipe — Full Workflow

> **Move mix:** 15% [CLUSTER] · 25% [INTERPRET] · 35% [PRIORITIZE] · 25% [NARRATE]

The room already did most of the synthesis — Decide vote, five user tests. Your job is to back the room's vote or call it wrong. Sometimes both at once.

## Prerequisite: synthesis-ready file

For a sprint, the file is small but specific:

- The five user-test notes (raw, written during the test)
- Recordings if consented to
- The Decide-stage artifacts (winning sketch, two alternatives, vote breakdown)
- The sprint goal
- The sprint hypothesis — *we believe X. If true, we'd expect Y in testing.*
- The team's pre-existing positions (CEO, product lead, eng lead each may have horses)

If the team didn't write down the hypothesis, write it down Friday afternoon as you remember it. Get the team to confirm. The hypothesis is the test the synthesis evaluates.

## Step 1 — Structure the test notes [CLUSTER, light]

Run **Prompt #8 (User-test notes structurer)**. For each tester, three sections:

1. **What worked** — behaviors the tester executed successfully (behavioral, not affective)
2. **What broke** — behaviors the tester failed at or expressed confusion about
3. **What surprised** — anything that didn't fit either category

~20 min.

## Step 2 — Map evidence against hypothesis [CLUSTER → INTERPRET bridge]

For each tester, ask: did this test session **support** the hypothesis, **complicate** it, or **break** it?

Tally:
- *N supports, N complicate, N break.*

That tally is the synthesis spine.

## Step 3 — Stress-test your read [INTERPRET]

Run **Prompt #9 (Sprint evidence stress-test)**. The model argues that you've overstated the testing evidence.

You'll either incorporate the sharpening or reject the comfort-framing. See [`/prompts/sprint/09-sprint-evidence-stress-test.md`](../../prompts/sprint/09-sprint-evidence-stress-test.md).

## Step 4 — Draft the Monday recommendation [PRIORITIZE → NARRATE]

Write one of four sentences (see [`four-recommendations.md`](four-recommendations.md)):

1. **Ship the winner** — rare
2. **Iterate before shipping** — most common
3. **Abandon the winner** — rarer
4. **Explore a third option** — rarest, most valuable when correct

You write this sentence yourself, by hand. The model drafts generic versions every time.

## Step 5 — Surface what changed your mind [NARRATE]

The section most sprint syntheses skip. Add it.

The "what changed our mind" section names what the five user tests showed that the Decide vote could not have shown. Honors the room's vote even when testing complicates it.

Write this from scratch. Political work.

## Step 6 — Risks list [NARRATE]

Three to five risks, ordered by severity. For each:

> **Risk:** [one-line description]. **Severity:** Low / Medium / High. **Mitigation:** [what you'd do to reduce it].

## Step 7 — Draft the readout [NARRATE]

One-pager + 6–8 slide deck.

- Slide 1: Recommendation (one sentence)
- Slide 2: What we tested and how
- Slide 3: Evidence summary (tester-by-tester)
- Slide 4: What changed our mind
- Slide 5: Risks list
- Slide 6: Proposed next step
- Slides 7–8 (optional): Methodology + alternatives

## Step 8 — Send Sunday night

Send the readout Sunday evening, not Monday morning. The team will read it before their Monday standup. By the time you're in standup, the team has had eight hours to absorb and write their pushback. Monday-morning discussion is sharper because of it.

If you send Monday morning, the team reads it for the first time in standup. The discussion is shallower; slow readers get behind.

**Send Sunday. Be available by text. The discussion happens Monday.**

## Source

*The Synthesis Playbook*, Chapter 6 "Design sprint synthesis."
