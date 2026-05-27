# Prompt #3 — Interpretation stress-test

> **From:** *The Synthesis Playbook*, prompt appendix, #3.
> **Recipe:** Discovery (Ch 4). Used at the [INTERPRET] step in any recipe.
> **Used at:** Step 4 — [INTERPRET] in `skills/synthesis-discovery/SKILL.md`. Also used in Sprint and Retro recipes.
> **Workhorse:** Yes.

## The prompt

```
Here is my interpretation of Theme [X]: [paste your sentence].

Now argue the strongest case that this interpretation is wrong.
Specifically:

1. What's the alternative reading of the same quotes? Make the
   alternative as strong as you can.
2. What evidence in the transcripts would have to be true for my
   interpretation to be correct but isn't?
3. What's the most uncomfortable thing my interpretation implies
   that I might be avoiding?
4. If a skeptical [stakeholder role, e.g. CPO] read my interpretation,
   what's the first question they'd ask?
```

## What to customize

- `[X]` — theme number or name
- `[paste your sentence]` — your one-sentence interpretation
- `[stakeholder role]` — the most skeptical reader of your readout, by role (e.g. `CPO`, `CFO`, `head of engineering`, `board member`)

## Why this is the most useful prompt in the book

The model is a competent steelman and a terrible advocate. Asked to argue against your interpretation, it does it well. Asked to argue for it, it flatters. **Always ask it to push back.**

This prompt works because it never asks the model to evaluate your interpretation. It asks the model to construct the alternative case. The model has no incentive to soften.

## What you'll discover

One of three things:

- **Your interpretation holds.** Alternative reading is weaker than yours. Keep going.
- **Your interpretation partially holds.** Model surfaces evidence you missed that complicates your reading. Revise the sentence.
- **Your interpretation falls apart.** Alternative is stronger than yours. Rewrite the interpretation from scratch.

The third one happens. It's painful. It's the whole reason the step exists. Better to rewrite on Sunday than to have a CPO take it apart on Wednesday.

## Common failures

- **Model softens the alternative.** If the steelman reads as "well, you could maybe argue X, but really your interpretation is fine," re-prompt: "Make the alternative as strong as you can. Do not soften it."
- **Model invents evidence.** Sometimes models hallucinate quotes that "would support" the alternative. Always cross-reference against the actual transcripts before changing your interpretation.

## License

MIT. See `/LICENSE`.
