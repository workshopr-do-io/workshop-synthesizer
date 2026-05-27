# Prompt #15 — Retro sticky clusterer with explicit minority-view output

> **From:** *The Synthesis Playbook*, prompt appendix, #15.
> **Recipe:** Retro (Ch 8).
> **Used at:** Step 1 — [CLUSTER] in `skills/synthesis-retro/SKILL.md`.

## The prompt

```
Here are [N] retro stickies from a [duration] retro. Three columns:
"what worked," "what didn't," "what we should change."
Source CSV: [paste].

Do this in three passes, showing me each:

Pass 1 — Cluster within column. Group the stickies in each column into
themes. Aim for 4–6 themes per column. Do not create a "miscellaneous"
bucket. If a sticky doesn't fit, leave it ungrouped and call it out at
the end.

Pass 2 — Cross-column linking. Identify themes that span columns. A
"what didn't" theme often has a paired "what we should change" theme,
and sometimes a paired "what worked" theme too (something that worked
precariously, by individual effort). Link them.

Pass 3 — Minority view extraction. For each theme, identify any sticky
that pushes against the dominant theme position. Surface these as
minority views, not as exceptions to be dismissed. A minority view is
a sticky that says the opposite of what the rest of the cluster says,
or that names a cost the cluster doesn't acknowledge.

Important: do not combine the minority view into the majority theme as
"nuance." Surface it as its own subsection. The minority view is the
data, not the noise.

Constraints: preserve exact wording for stickies. Do not paraphrase to
soften. If a sticky is sharp, keep it sharp.
```

## What to customize

- `[N]` — total sticky count (e.g. `66`)
- `[duration]` — e.g. `quarterly`, `sprint`, `project`
- `[paste]` — sticky export with: sticky text, column ("what worked" / "what didn't" / "what we should change"), who wrote it if known, dot count

## Why "the minority view is the data, not the noise"

Most retros produce stickies that disagree with each other. The disagreement is the signal. A retro synthesis that smooths the disagreement is a retro synthesis that lies about the team.

Pass 3 is the load-bearing pass in this prompt. Don't skip it; don't accept a model output that softens it.

## What to do with the output

Run [prompt #16 (dissent-vs-noise distinguisher)](16-dissent-vs-noise-distinguisher.md) on the minority views to figure out which are real structural dissent vs. one-off frustration. Real dissent goes in the write-up.

## Common failures

- **Model paraphrases stickies to soften.** If a sticky said "we don't trust each other on decisions" and the cluster reports "decision-making concerns," the model has softened. Re-prompt: "Preserve exact wording. Do not paraphrase."
- **Minority view gets buried as "nuance."** Re-prompt: "Surface minority views as their own subsection, not as nuance inside the majority theme."

## License

MIT. See `/LICENSE`.
