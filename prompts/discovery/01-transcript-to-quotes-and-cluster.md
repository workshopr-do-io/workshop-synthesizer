# Prompt #1 — Transcript-to-quotes extractor + first-pass clusterer

> **From:** *The Synthesis Playbook*, prompt appendix, #1.
> **Recipe:** Discovery (Ch 4). Adaptable to any recipe with interview or discussion transcripts.
> **Used at:** Step 2 — [CLUSTER] in `synthesis-discovery/SKILL.md`.
> **Workhorse:** Yes (counts as two of the twelve — the transcript-to-quotes extractor and the first-pass clusterer).

## The prompt

```
You're helping me synthesize [N] customer discovery interviews for a
[client type] client. The interviewees are [interviewee description].
The working hypothesis is: [paste hypothesis here].

I'm going to paste all [N] transcripts below in one block, separated
by headers.

Do this in three passes, and show me each pass before moving to the next:

Pass 1 — Quote extraction. For each interview, pull out the 5–8 quotes
that contain the highest-signal content. Signal means: anything that
contradicts the working hypothesis, anything that surprised the
interviewer, anything where the customer described their workaround
or workflow in their own words, and anything where the customer
expressed frustration, delight, or doubt. Skip everything else.
Preserve the customer's exact wording. Tag each quote with the
interview header.

Pass 2 — Cluster the quotes. Group the extracted quotes into
candidate themes. Aim for 6–10 themes. Do not create a "miscellaneous"
bucket. If a quote doesn't fit a theme, leave it ungrouped and call
it out at the end as "ungrouped — needs human review."

Pass 3 — Theme summary. For each theme: a one-line name, a one-sentence
description, the count of supporting quotes, and a list of the three
most representative quotes (verbatim, with attribution).

Important constraints:
- Do not flatten contrarian quotes into majority themes. If a quote
  pushes against a cluster, surface it as a "minority view" within
  the theme rather than dropping it.
- Do not invent quotes or paraphrase. If you're going to attribute
  a quote, it must appear verbatim in the source transcript.
- Flag any cluster that contains fewer than three quotes as
  "thin — verify before relying on it."
```

## What to customize

- `[N]` — number of interviews (e.g. `fourteen`)
- `[client type]` — e.g. `B2B SaaS`, `consumer fintech`, `healthcare provider`
- `[interviewee description]` — e.g. `existing customers, mid-tier customers, and two churned customers`
- `[paste hypothesis here]` — the one-sentence hypothesis the team walked in with

## Always pair with Prompt #2

This prompt clusters. Clustering smooths. **Always follow this prompt with the [anti-flattening critic (#2)](02-anti-flattening-critic.md)** before you trust the themes. Discovery synthesis lives or dies at that second pass.

## Common failures

- **Theme inflation.** If the model returns 12+ themes for a 10-interview round, re-run with the constraint "aim for 6–8 themes; consolidate adjacent ones."
- **Miscellaneous bucket sneaking back in.** Some models smuggle it in as "other themes" or "additional findings." Re-run and re-enforce the constraint.
- **Paraphrased quotes.** Spot-check 3–5 quotes against the source transcript. If any are paraphrased, escalate the verbatim constraint in the prompt and re-run.

## License

MIT. Copy, adapt, steal. See `/LICENSE`.
