# Prompt #5 — Decision log structurer

> **From:** *The Synthesis Playbook*, prompt appendix, #5.
> **Recipe:** Strategic offsite (Ch 5).
> **Used at:** Step 1 — [PREP] in `skills/synthesis-offsite/SKILL.md`.
> **Workhorse:** Yes.

## The prompt

```
Here is my raw decision log from a [duration] [workshop type]: [paste].
And here are my notes: [paste].

Restructure into a list of decisions. For each decision: the question
posed, the room's answer in one sentence, the decision quality
(committed / leaning / parked / open) — be conservative; if you're
not sure something was committed, mark it leaning — and the follow-up
if one was named.

Do not attribute who said what unless my source notes name them
explicitly. If attribution is implied but not stated, leave it blank
and I'll fill it in.

Flag any decision where my notes are too thin to tell what was decided.
```

## What to customize

- `[duration]` — e.g. `two-day`, `half-day`
- `[workshop type]` — e.g. `executive offsite`, `founder/board strategy day`, `quarterly leadership working session`
- `[paste]` (first) — raw decision log from the room
- `[paste]` (second) — your handwritten or typed notes

## The "do not attribute" constraint matters

The model will guess at attribution otherwise. A wrong attribution in an executive synthesis is unrecoverable. Force it to leave attribution blank if not explicit in your notes — you'll fill those in by hand from memory.

## What to do with the output

Take the model's structured output. Add your own attribution and pushback notes by hand. The model gives you the spine; you add the political read.

## Common failures

- **Model overstates decision quality.** Pushes "leaning" decisions into "committed." The conservative-bias instruction in the prompt addresses this; if it slips, re-prompt with the explicit list.
- **Model invents follow-ups.** If your notes don't name a follow-up, the model sometimes fabricates one. Spot-check; cut anything not in the source.

## License

MIT. See `/LICENSE`.
