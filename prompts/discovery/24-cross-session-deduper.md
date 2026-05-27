# Prompt #24 — Cross-session deduper (CAB variant)

> **From:** *The Synthesis Playbook*, prompt appendix, #24.
> **Recipe:** Discovery (Ch 4) — Customer Advisory Board ADAPT sidebar.
> **Used at:** Replaces standard [CLUSTER] step for cross-quarter CAB synthesis.

## The prompt

```
Here are the theme lists from [N] quarterly CABs: [paste theme summaries
for each quarter].

Identify themes that recur across quarters. For each recurring theme:
name it, list which quarters it appeared in, note how the framing
evolved across quarters, and flag whether the underlying signal is
getting stronger, weaker, or unchanged.

Separately, identify themes that appeared in only one or two quarters
and explain whether they're (a) new signals that will likely recur,
(b) one-time noise, or (c) signals that died because the company
addressed them.
```

## What to customize

- `[N]` — number of CAB sessions (typically 4 quarters)
- `[paste theme summaries for each quarter]` — output from prompt #1 for each quarter, concatenated

## Why this prompt earns its keep

The dominant CAB synthesis failure is letting the most recent session dominate, even when the pattern is older. The fix is to weight evidence by recurrence across sessions, not by which session is freshest in your head.

If a theme appeared in three of four quarters but was quiet in the most recent one, that's still a real signal. The opposite — a theme that's loud in the most recent but absent from the prior three — is usually noise or a single voice you should verify before promoting.

## Common failures

- **Model overweights the most recent quarter.** Re-prompt: "Weight recurrence across quarters, not recency."
- **Model invents quarter labels.** Always paste the actual quarter dates; never let the model infer them.

## License

MIT. See `/LICENSE`.
