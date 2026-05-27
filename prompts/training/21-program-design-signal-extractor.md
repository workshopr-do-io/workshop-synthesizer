# Prompt #21 — Program-design signal extractor

> **From:** *The Synthesis Playbook*, prompt appendix, #21.
> **Recipe:** Training debrief (Ch 9).
> **Used at:** Step 3 — [INTERPRET] in `skills/synthesis-training/SKILL.md`.

## The prompt

```
Here are the pulse surveys, co-facilitator role-play notes, and
closing-circle highlights from a [duration] [program type]: [paste].

For each of the [N] sessions in the program, identify:

1. Strength signal — what landed well, with evidence (pulse score,
   specific quote, role-play observation).
2. Friction signal — what landed less well, with evidence.
3. Skill demonstration — did participants actually demonstrate the
   skill in the room (role-play, peer coaching, structured exercise),
   or just discuss it?

Important: the goal here is honest assessment of the program, not
vindication of the design. If a session that we thought would be a
centerpiece landed flat, say so. If a session that was a fill-in
landed unexpectedly well, say so.

Constraint: do not infer. If the data is thin on a session, say "thin
signal" and recommend a specific question to ask in the next cohort.
```

## What to customize

- `[duration]` — e.g. `three-day`
- `[program type]` — e.g. `leadership development program`, `sales enablement bootcamp`
- `[paste]` — pulse surveys, co-facilitator notes, closing-circle highlights
- `[N]` — number of sessions in the program (e.g. `twelve`)

## The demonstration-vs-discussion distinction

This is the diagnostic that predicts whether a competency actually landed:

- **Discussed** is a low-quality signal — could be politeness, intellectual engagement, or vapor
- **Demonstrated** is a high-quality signal — they did the thing under pressure with another human watching

A session that participants demonstrate in (role-play, peer coaching, structured exercise) lands deeper than a session that participants only discuss. The model surfaces this distinction; you use it to recommend program changes.

## What to do with the output

This output goes into the program owner's cohort analysis (Step 5). It's the section the L&D leader will read most carefully — they paid for the program and they want to know whether to run it again, with what changes.

## Common failures

- **Model defaults to "successful" assessments to vindicate the design.** Re-prompt: "Honest assessment. If something didn't land, say so. The program owner needs this."
- **Model conflates discussion with demonstration.** Re-prompt the distinction; this is the load-bearing call.
- **Model infers from thin data.** If a session has only 2 pulse scores and one co-facilitator note, the model sometimes confidently assesses it. Re-prompt: "Where data is thin, say 'thin signal' and propose a question to ask next time."

## License

MIT. See `/LICENSE`.
