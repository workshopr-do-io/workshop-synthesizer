# Prompt #8 — User-test notes structurer

> **From:** *The Synthesis Playbook*, prompt appendix, #8.
> **Recipe:** Design sprint (Ch 6).
> **Used at:** Step 1 — [CLUSTER, light] in `synthesis-sprint/SKILL.md`.

## The prompt

```
Here are my raw notes from five user tests of a prototype: [paste].
The prototype is [one-line description]. The hypothesis the prototype
was testing is [one-line hypothesis].

For each tester, produce three sections:

1. What worked — specific behaviors the tester executed successfully.
   Behavioral observations only, not affective.
2. What broke — specific behaviors the tester failed at or expressed
   confusion about.
3. What surprised — anything in the test session that didn't fit
   either category.

Constraints: use only what's in my notes. Do not infer or extrapolate.
If a tester's notes are thin in one category, write "no data" rather
than inventing.
```

## What to customize

- `[paste]` — your raw test-session notes (one block per tester)
- `[one-line description]` — what the prototype is (e.g. `a swipe-style expense approval flow for managers`)
- `[one-line hypothesis]` — what the prototype was testing (e.g. `swipe-based approval will reduce manager review time without compromising audit defensibility`)

## Why "behavioral only, not affective"

A tester saying "I liked it" is affective and weak. A tester *doing the swipe* in 90 seconds is behavioral and strong. The structuring forces you to separate signal from noise — affective claims belong in the "surprised" column where you can decide whether to weight them; behavioral claims drive the synthesis.

## Pair with prompt #9

After structuring, run [the sprint evidence stress-test (#9)](09-sprint-evidence-stress-test.md) against your mapping of testers vs. hypothesis. The two prompts together are the whole agentic component of the sprint recipe — the rest is judgment.

## Common failures

- **Model invents behaviors.** If your notes say "didn't engage with the rail," the model sometimes elaborates to "tested the rail twice, then abandoned." Hold the line — re-prompt: "Use only what's in my notes verbatim. Do not extrapolate."
- **Model conflates affective and behavioral.** "Liked the interface" is affective, not behavioral. Recategorize by hand if the model misplaces them.

## License

MIT. See `/LICENSE`.
