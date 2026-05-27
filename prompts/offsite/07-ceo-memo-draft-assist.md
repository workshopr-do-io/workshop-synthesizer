# Prompt #7 — CEO memo draft assist

> **From:** *The Synthesis Playbook*, prompt appendix, #7.
> **Recipe:** Strategic offsite (Ch 5).
> **Used at:** Step 4 — [NARRATE, with model assist] in `synthesis-offsite/SKILL.md`.

## The prompt

```
I'm drafting a five-page CEO memo from a two-day strategic offsite.
Here is the structured decision log: [paste].

Draft the "committed calls" section as paragraphs. One paragraph per
committed call. Each paragraph names the call, the rationale, the
owner, and the timeline. Write in plain prose. Address the CEO as
"you."

Do not use words like "leverage," "empower," "strategic,"
"comprehensive," "robust," "key," or "critical." Do not editorialize.
Just translate the structured log into clean paragraphs.
```

## What to customize

- `[paste]` — output from prompt #5 (decision log structurer), refined with your hand-added attribution and pushback notes

## What this prompt does NOT cover

The CEO memo has six sections. This prompt only drafts the **committed calls** section. The other five sections you write by hand:

1. **Opening paragraph** — the framing. *Two days, five of you, three big calls.* Yours.
2. **Committed calls** — this prompt drafts. You edit heavily.
3. **Leaning calls** — similar shape to committed, but explicit about what would push the lean to a commit. Adapt this prompt for that section.
4. **Parked calls** — short list, dates, no narrative.
5. **What the room did not resolve** — the section the CEO reads most carefully. Yours, from scratch.
6. **A short note from the facilitator** — your read on the room. Yours.

## Common failures

- **Model uses banned words anyway.** Re-prompt with the exact banned list and add: "If you used any of these words, rewrite that paragraph completely."
- **Model writes all paragraphs at the same length and rhythm.** Vary them by hand in editing; the model tends to homogenize.
- **Model overstates decision strength.** "Strongly committed" where the reality was "agreed with conditions." Soften in editing.

## License

MIT. See `/LICENSE`.
