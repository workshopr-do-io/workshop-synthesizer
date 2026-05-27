# Prompt #20 — Cohort-pattern surfacer

> **From:** *The Synthesis Playbook*, prompt appendix, #20.
> **Recipe:** Training debrief (Ch 9).
> **Used at:** Step 2 — [CLUSTER → INTERPRET] in `synthesis-training/SKILL.md`.

## The prompt

```
Here are [N] baseline-to-close pairs from a [program description]:
[paste].

Identify patterns across the cohort. Specifically:

1. Are there sub-cohorts who moved similarly? (For example:
   high-experience participants who deepened existing skills versus
   low-experience participants who acquired new skills.)
2. Which of the [N] program competencies showed the strongest movement
   across the cohort? Which showed the weakest?
3. Were there participants whose baseline expectation was not what they
   ended up gaining? Surface these as worth-naming-individually.
4. Were there participants who moved less than the others? Don't
   soften — name them. We need to be honest with the program owner
   about who didn't get what they needed.

Format: prose paragraphs, not bullets. Be specific. Cite the participants
you're drawing patterns from.
```

## What to customize

- `[N]` (first) — number of participants (e.g. `sixteen`)
- `[program description]` — e.g. `three-day leadership development program for first-time managers`
- `[paste]` — baseline-to-close pairs you built in Step 1 (one per participant)
- `[N]` (second) — number of program competencies (e.g. `three`)

## Why the "don't soften — name them" matters

The dominant training-synthesis failure is wanting to deliver a positive program write-up by hiding the participants who moved less than others. The flags section is mandatory for honest synthesis. If you can't name at least one participant who moved less, you haven't looked.

The program owner needs the candor. The L&D leader can't run the next cohort better if they don't know who didn't get what they needed in this one.

## What to do with the output

The patterns the model surfaces will not all be correct. The model is pattern-matching from text; it can't see who's recently joined the team, who's in a particularly hard situation, who said one thing on day one and meant something different.

You verify by hand. The patterns that survive verification become the spine of the cohort-level analysis (for the program owner) and the source of named stories in the budget-holder one-pager.

## Common failures

- **Model softens the below-average participants.** Re-prompt: "Name the specific participants who moved less. Be honest. The program owner needs this."
- **Model invents sub-cohorts.** If sub-cohorts have weak evidence, the model sometimes manufactures them. Spot-check: are the sub-cohort traits actually present in the baseline-to-close pairs?
- **Model misses the surprising-direction participants.** Participants who came in for X and left with Y are the most interesting ones; if the model misses them, re-prompt to scan for "baseline-vs-close mismatches in expected outcome."

## License

MIT. See `/LICENSE`.
