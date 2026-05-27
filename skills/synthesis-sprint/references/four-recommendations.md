# The Four Possible Recommendations

The Step 4 sentence in the Design Sprint recipe is **exactly one of these four.** Don't invent a fifth.

## 1. Ship the winner

> *Ship [winning concept]. The testing supports the hypothesis with minor caveats: [list the caveats]. Recommended next step: [specific next move — usually a beta with N customers].*

When: testing supports the hypothesis in 4+ of 5 sessions. Breaks are minor and addressable in iteration.

How common: **rare.** Sprints are designed to surface issues that didn't show up in the room. They usually do.

## 2. Iterate before shipping

> *Iterate before shipping. The [winning concept] tests well on [dimension A] but fails [dimension B] in [N] of 5 sessions. We recommend [specific iteration] and re-testing with [N] more participants. If the iteration resolves [dimension B], ship. If not, [explicit fallback].*

When: testing complicates the hypothesis but a specific change could close the gap. Most common outcome.

How common: **most common** — the default sprint outcome.

Note: name the explicit fallback. *If the iteration doesn't work, here's the alternative.* This is what makes the recommendation defensible if the iteration fails.

## 3. Abandon the winner

> *Abandon [winning concept]. The testing breaks the hypothesis structurally in [N] of 5 sessions. The break is not addressable in iteration because [specific reason]. We recommend [returning to the room with a different question / re-running the sprint with a different prototype / pausing to gather more data].*

When: testing breaks the hypothesis structurally. The break is not addressable through tweaks; it's a fundamental mismatch.

How common: **rarer** than iterate. But it happens, and when it does, the team needs a clean break-and-redirect rather than a half-hearted iteration.

## 4. Explore a third option

> *Explore a third option not voted on Thursday. The testing reveals that the room voted on the wrong question entirely. Specifically: [what the room thought it was testing vs. what the testing actually revealed]. We recommend [specific third option] and a re-test with [N] participants.*

When: the testing reveals the room voted on the wrong question. The right answer wasn't in the Decide round. Often surfaces when a tester response opens a question the team hadn't considered.

How common: **rarest, most valuable when correct.** A sprint that ends with a third option means the testing did its load-bearing work — surfaced something the room couldn't see.

## How to choose between them

Use the supports/complicates/breaks tally:

| Tally | Likely recommendation |
|---|---|
| 4–5 supports, 0 breaks | Ship the winner |
| Mix of supports and complicates, 0 breaks | Iterate before shipping |
| 1–2 breaks, supports in others | Iterate before shipping (with the parallel-mode pattern) |
| 3+ breaks, structural issue | Abandon the winner |
| Testing reveals the room voted on the wrong question | Explore a third option |

## The fallback rule

Every "Iterate before shipping" recommendation must name an **explicit fallback** for when the iteration doesn't work.

Why: without a fallback, "iterate" becomes a soft no — the team doesn't know what to do if the iteration fails. With a fallback, the iteration is a real test with a real off-ramp.

From the swipe-or-not worked example: *If the parallel mode resolves the audit issue, ship the winner. If not, reconsider the list-view alternative voted down on Thursday.* The list-view alternative was the explicit fallback.

## Why not a fifth recommendation

Some practitioners try to construct hybrid recommendations: *Ship a small version then iterate the rest.* These collapse into one of the four when you press on them:

- "Ship a small version" = ship the winner (smaller scope, but still ship)
- "Then iterate the rest" = iterate before shipping (for the rest)
- These are two distinct decisions, not one

The discipline of choosing one of four sentences forces clarity. If you can't fit your recommendation into one of the four, you haven't yet made the call.

## What the four NOT do

- They don't equivocate. "Ship with caution" is not a recommendation; it's a hedge.
- They don't punt. "Bring it back to the team for further discussion" means you didn't write a recommendation.
- They don't bury the call. The recommendation is the first sentence of the readout, not the last.

## Source

*The Synthesis Playbook*, Chapter 6, Step 4 of the sprint recipe.
