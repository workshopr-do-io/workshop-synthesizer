# Prompt #19 — Cause-vs-blame check

> **From:** *The Synthesis Playbook*, prompt appendix, #19.
> **Recipe:** Retro (Ch 8) — Post-mortem ADAPT sidebar.
> **Used at:** Step 3.5 — added when running a post-mortem instead of a retro.
> **Workhorse:** Yes.

## The prompt

```
Here is my draft cause analysis: [paste].

For each sentence, identify whether it's describing:

1. A cause — a system failure, missing safeguard, ambiguous process,
   or contextual factor.
2. A blame — an attribution of fault to a specific person or role.

Rewrite any blame sentence as a cause sentence, where possible. If a
sentence cannot be rewritten without losing the meaning, flag it for
human review.
```

## What to customize

- `[paste]` — your draft cause analysis for the post-mortem

## The blame-vs-cause distinction

Post-mortems have to name the cause without naming the blame. A junior engineer pushed the wrong config. The **cause** is the missing safety check on the deploy script. The **blame** is on the engineer.

The post-mortem names the cause. It does not name the blame. If you find yourself writing a sentence that puts a person at the center of the cause description, rewrite to put the system at the center.

## Examples

- **Blame:** "The engineer didn't check the config file."
  **Cause:** "The deploy script did not block bad configs from being pushed. The check for [pattern] was not in place."

- **Blame:** "The on-call missed the escalation page."
  **Cause:** "The escalation policy had no fallback to a secondary on-call when the primary did not acknowledge within 5 minutes."

- **Blame:** "The PM made the wrong call on launch readiness."
  **Cause:** "The launch readiness checklist had no quantitative threshold; the call was judgment-based without a forcing function."

## What to do with the output

The model will sometimes produce defensive rewrites that lose the meaning. Read each rewrite carefully. The goal is not to dodge accountability; it's to put the accountability where it can do the most good, which is on the system, not on the person who tripped over the system.

If a sentence cannot be rewritten without losing the meaning, the model flags it. You decide: keep the blame language (rare; only when the person's specific action is genuinely material to learning) or restructure the cause analysis.

## Common failures

- **Model rewrites "the engineer made an error" as "errors occurred."** Passive voice removes the system focus. Re-prompt: "Name the system or process that allowed the error, not the person who made it AND not just 'errors occurred'."
- **Model produces no real rewrites; just adds "the system allowed" in front of every sentence.** That's a tell that the cause analysis is too thin. Strengthen the analysis by hand before re-running.

## License

MIT. See `/LICENSE`.
