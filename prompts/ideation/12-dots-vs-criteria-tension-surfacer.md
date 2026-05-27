# Prompt #12 — Dots vs. criteria tension surfacer

> **From:** *The Synthesis Playbook*, prompt appendix, #12.
> **Recipe:** Ideation (Ch 7).
> **Used at:** Step 3 — [PRIORITIZE] in `synthesis-ideation/SKILL.md`.

## The prompt

```
Here is the ranked list using criteria: [paste]. Here are the dot
counts: [paste].

Identify three groups of ideas:

1. Hot and good — high on the criteria and heavily dotted. These are
   easy includes.
2. Hot but weak — heavily dotted but low on the criteria. Common
   reasons: novelty, social momentum in the room, executive enthusiasm.
   Name the likely reason for each.
3. Cool but strong — lightly dotted but high on the criteria. Common
   reasons: introduced late in the session, advocated by a quieter
   voice, looks boring on the sticky. Name the likely reason for each.

For each item in groups 2 and 3, write one sentence on whether the
dot signal or the criteria signal is more trustworthy here.
```

## What to customize

- `[paste]` (first) — output from prompt #11 (ranked list with criteria scores)
- `[paste]` (second) — dot-vote tally from the room

## Why this prompt is the move that earns the synthesis

For ideation, cool-but-strong ideas are often the most valuable shortlist additions. The room missed them because they were proposed by a quieter voice, or because they look boring on a sticky and read sharp once expanded.

Hot-but-weak ideas are often the ones to cut — they made the room excited but won't survive contact with production.

The synthesis lead's job is to read these tensions and make calls. The prompt surfaces them; you make the calls.

## What to do with the output

Take the three groups. For each item in groups 2 and 3, decide:

- **Include in shortlist** — when criteria signal is more trustworthy AND the idea passes other shortlist tests
- **Cut to kill list** — when dot signal was a flash and criteria are right
- **Park for follow-up** — when neither signal is conclusive yet

The decision is yours; the model can frame the trade-off, but the call carries weight the model doesn't.

## Common failures

- **Model misclassifies "hot and good" too liberally.** If everything ends up in group 1, your criteria are too soft. Re-run with tighter scoring.
- **Model invents likely-reasons.** "Hot but weak because of executive enthusiasm" is fine if you can confirm; not fine if there was no exec leaning forward. Cross-check against what actually happened in the room.

## License

MIT. See `/LICENSE`.
