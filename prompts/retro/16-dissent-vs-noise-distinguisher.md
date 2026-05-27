# Prompt #16 — Dissent-vs-noise distinguisher

> **From:** *The Synthesis Playbook*, prompt appendix, #16.
> **Recipe:** Retro (Ch 8).
> **Used at:** Step 2 — [CLUSTER critic] in `synthesis-retro/SKILL.md`.
> **Workhorse:** Yes.

## The prompt

```
Here are the minority views surfaced in the previous pass: [paste].

For each minority view, evaluate whether it's:

1. Real structural dissent — names a pattern or systemic issue that
   the dominant theme is missing. Should be surfaced in the write-up.
2. One-off frustration — names a specific instance, not a pattern.
   Worth acknowledging in the discussion but probably not in the
   write-up.
3. Adjacent topic — actually about a different theme. Should be moved.
4. Vague signal — could be either dissent or noise; we'd need more
   context to tell.

For category 1 and 4 items: write a one-sentence framing of what the
dissent is actually saying, in its strongest form.
```

## What to customize

- `[paste]` — output from prompt #15's Pass 3 (the minority views)

## Why the four-category split matters

Not every minority view is a real minority view. Sometimes one person is venting about a one-off frustration that isn't structural. The synthesis has to tell the difference.

- **Real structural dissent (category 1)** → goes in the write-up, surfaced explicitly
- **One-off frustration (category 2)** → worth acknowledging verbally but doesn't load the write-up
- **Adjacent topic (category 3)** → moved to its proper theme
- **Vague signal (category 4)** → flagged for human follow-up; sometimes the most important category, because vague signals are where you find dissent that's still finding its words

## What to do with the output

The model will sometimes misclassify — it'll put real dissent in "vague signal" because it doesn't see how the dissent connects to the team's history. You correct by hand using context the model doesn't have.

For category 1 items, the model's one-sentence framing becomes the basis of how you write the minority view into the public write-up.

## Common failures

- **Model softens real dissent into "vague signal."** If you see a sticky that you know is structural getting classified as vague, the model lacks team context. Override.
- **Model categorizes everything as one-off.** Re-prompt: "Many of these are patterns, not single incidents. Look for the systemic version of each frustration."

## License

MIT. See `/LICENSE`.
