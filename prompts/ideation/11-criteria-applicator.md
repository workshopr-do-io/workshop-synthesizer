# Prompt #11 — Criteria applicator

> **From:** *The Synthesis Playbook*, prompt appendix, #11.
> **Recipe:** Ideation (Ch 7).
> **Used at:** Step 2 — [PRIORITIZE] in `synthesis-ideation/SKILL.md`.
> **Workhorse:** Yes.

## The prompt

```
Here is the list of tightened, deduplicated ideas: [paste].

The team agreed on [N] evaluation criteria during the session:

1. [Criterion 1] — [definition].
2. [Criterion 2] — [definition].
3. [Criterion 3] — [definition].
4. [Criterion 4] — [definition].

For each idea, score it on each criterion using a three-point scale:
High / Medium / Low. Be honest. If you're not sure, mark Unknown and
say why.

Then produce a ranked list using a weighted score
([criterion 1] %, [criterion 2] %, [criterion 3] %, [criterion 4] %).
Show the math.

Important: do not use the dot-vote count as input to the ranking.
The dots tell us what got hot in the room. The criteria tell us what
will work. We want the second.
```

## What to customize

- `[paste]` — output from prompt #10 (tightened, deduplicated ideas)
- `[N]` — number of criteria (typically 3–5)
- `[Criterion 1–4]` and `[definition]` — the team-agreed criteria from the room. Common ones: Impact, Feasibility, Novelty, Time-to-test
- `[criterion 1] %`, etc. — the weighting (e.g. impact 40%, feasibility 25%, novelty 20%, time-to-test 15%)

## Why "do not use the dot-vote count"

The dots tell you what got hot in the room. The criteria tell you what will work. The synthesis lives in the gap between those two — see [prompt #12](12-dots-vs-criteria-tension-surfacer.md), which surfaces the disagreements.

If you let the model weight by dot count, you ship the room's enthusiasm, not the team's commitment.

## What to do with the output

This list is candidate, not final. It will disagree with the dot-vote in interesting ways. Some heavily-dotted ideas will score badly. Some lightly-dotted ones will score well. **Those disagreements are where the synthesis earns its keep.**

Always run [prompt #12 (dots-vs-criteria tension surfacer)](12-dots-vs-criteria-tension-surfacer.md) after this one.

## Common failures

- **Model scores too generously by the end.** If 25 ideas all score Medium-Medium-Medium-Medium, the scoring is going soft. Re-run in batches of 5 with breaks between.
- **Model sneaks dot-vote into the ranking.** Spot-check: if the top-ranked items mysteriously match the top-dotted items, the constraint isn't being honored. Re-run.
- **Model misses the engineering feasibility nuance.** If feasibility scores look optimistic, override by hand — the model doesn't know your team's capacity.

## License

MIT. See `/LICENSE`.
