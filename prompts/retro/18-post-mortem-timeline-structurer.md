# Prompt #18 — Post-mortem timeline structurer

> **From:** *The Synthesis Playbook*, prompt appendix, #18.
> **Recipe:** Retro (Ch 8) — Post-mortem ADAPT sidebar.
> **Used at:** Step 1.5 — added when running a post-mortem instead of a retro.

## The prompt

```
Here are the source materials: incident logs, chat transcripts, meeting
notes, and individual recollections. [paste].

Build a timeline of what happened. Each entry: timestamp, what happened,
who was involved, what they knew at the time.

Critical constraint: do not impose retrospective clarity. If a decision
was made under uncertainty, the timeline entry says what they knew at
the time, not what we know now. If two people remember a decision
differently, surface the discrepancy rather than reconciling it. If
logs and recollections conflict, flag the conflict.
```

## What to customize

- `[paste]` — concatenated source materials: incident logs, chat transcripts, meeting notes, individual recollections

## Why "do not impose retrospective clarity"

The timeline produced by this prompt should look messier than a typical post-mortem timeline. That mess is honest. Cleaning it up is exactly the failure to avoid.

If a decision was made under uncertainty, the entry should say what the people knew **at the time**, not what we know now. Hindsight clarity in a post-mortem timeline produces a narrative that suggests the team should have known better — which is exactly what blameless post-mortems are designed to prevent.

## What to do with the output

The timeline becomes the spine of the post-mortem. Discrepancies between logs and recollections are flagged for follow-up — either someone misremembers (worth knowing) or the logs are incomplete (also worth knowing).

Pair with [prompt #19 (cause-vs-blame check)](19-cause-vs-blame-check.md) for the cause-analysis portion of the post-mortem.

## Common failures

- **Model imposes a clean narrative.** "At 02:14, the engineer decided to roll back" — but the engineer didn't decide that cleanly; they were guessing under pressure. Re-prompt: "Surface uncertainty in the timeline. Use phrases like 'X believed', 'X chose, based on what they could see at the time'."
- **Model reconciles conflicting recollections.** If two participants remember a decision differently, the model wants to pick the "real" version. Re-prompt: "Surface the discrepancy. Do not reconcile."
- **Model attributes intent retroactively.** "They decided to ignore the warning" implies intent that may not have existed. Soften by hand.

## License

MIT. See `/LICENSE`.
