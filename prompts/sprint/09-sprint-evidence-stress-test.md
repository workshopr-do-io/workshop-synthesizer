# Prompt #9 — Sprint evidence stress-test

> **From:** *The Synthesis Playbook*, prompt appendix, #9.
> **Recipe:** Design sprint (Ch 6).
> **Used at:** Step 3 — [INTERPRET] in `synthesis-sprint/SKILL.md`.

## The prompt

```
The team voted [tally] for [winning concept]. The hypothesis was
[hypothesis].

Here are the five test summaries with my mapping against hypothesis:
[paste]. My tally is [supports / complicates / breaks counts].
My interpretation is [one-sentence interpretation].

Argue the strongest case that my interpretation overstates the testing
evidence. Specifically:

1. What's the alternative read where the testing actually supports the
   room's vote more than my tally suggests?
2. What would I have to believe about the breakers to make the room's
   vote correct anyway?
3. Where in the testing is the signal strongest, and where is it weakest?
4. If a confident product leader read my recommendation, what's the
   first counter-argument they'd make?
```

## What to customize

- `[tally]` — e.g. `4–1`
- `[winning concept]` — short name for the winning sketch (e.g. `the swipe interface`)
- `[hypothesis]` — the sprint hypothesis the prototype was testing
- `[paste]` — output from prompt #8, with your Supports/Complicates/Breaks mapping added per tester
- `[supports / complicates / breaks counts]` — e.g. `1 supports, 2 complicate, 2 break`
- `[one-sentence interpretation]` — your current read of what the testing showed

## Why this prompt exists

Five users is a small sample. The temptation, especially when testing pushes against the room's vote, is to second-guess the testing. *Maybe tester 4 was inattentive. Maybe tester 5 was unusually conservative.* The model helps you check yourself.

The point isn't to change your call. It's to make you confident the call survives the strongest counter-argument.

## What you'll find

The model will produce a credible counter-case. Read it carefully:

- **If it sharpens your interpretation** — e.g., "Tester 4's failure could be onboarding-addressable" — incorporate it
- **If it just flatters the room** — e.g., "the four supports outweigh the two breaks" — reject it; the hypothesis was a conjunction

## Common failures

- **Model defaults to the flattering case.** If the counter-case is "well, you have more supports than breaks so really the vote stands," re-prompt: "The hypothesis is a conjunction. A 'break' on either leg of a conjunction is a hypothesis-level break. Account for that."
- **Model questions tester reliability without evidence.** If the counter-case is "Tester 5 was unusual," ask the model to cite what about Tester 5 was specifically unusual based on the notes.

## License

MIT. See `/LICENSE`.
