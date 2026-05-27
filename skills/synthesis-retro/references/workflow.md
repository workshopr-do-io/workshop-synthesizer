# Retro & Post-Mortem Recipe — Full Workflow

> **Move mix:** 40% [CLUSTER] · 30% [INTERPRET] · 10% [PRIORITIZE] · 20% [NARRATE]

One job above all others: **preserve dissent.** The minority view is the data, not the noise.

## Prerequisite: synthesis-ready file

- The sticky export (CSV: sticky text, column, who wrote it if known, dot count)
- A discussion transcript or recording (the second half of the retro, if you ran a discussion portion)
- Vote tally per sticky and per column
- A feelings-temperature read with names (if you ran one — e.g., "1–5, how are you feeling about this quarter")
- Pre-existing context: what the team committed to at the start of the quarter

The discussion transcript and feelings-temperature read are how you separate sticky-volume from sticky-importance. **Get them.**

## Step 1 — Structure and cluster [CLUSTER]

Run **Prompt #15 (Retro sticky clusterer with explicit minority-view output)**. Three passes:

1. **Cluster within column** — group "what worked," "what didn't," "what we should change" each into 4–6 themes
2. **Cross-column linking** — link themes that span columns
3. **Minority view extraction** — for each theme, surface stickies that push against the dominant position

The third pass is the load-bearing pass. **Do not skip it.**

## Step 2 — Distinguish noise from real dissent [CLUSTER critic]

Run **Prompt #16 (Dissent-vs-noise distinguisher)**. Four categories:

- **Real structural dissent** — goes in the write-up
- **One-off frustration** — acknowledged verbally but probably not in the write-up
- **Adjacent topic** — moved to its proper theme
- **Vague signal** — flagged for human follow-up

The model will sometimes misclassify because it doesn't see team history. You correct by hand.

## Step 3 — Interpret the linked themes [INTERPRET]

For each linked theme, write a one-paragraph interpretation in your own voice.

Format:

> **Theme name.** *What worked / didn't / what to change.* The pattern across the columns is: [one-sentence interpretation]. The dominant view is: [summary]. The minority view, where present: [summary]. The change the team is proposing is: [summary of "what should change" sticky cluster].

Use the retro interpretation stress-test (Prompt #3 from the Discovery recipe — it works across recipes) to force the uncomfortable framing.

## Step 4 — Action items [PRIORITIZE]

Three to seven action items, no more. Beyond seven, the team starts no-shipping.

For each candidate:

- **Specificity** — concrete enough that an owner can execute without re-discussion
- **Owner clarity** — named person
- **Falsifiability** — will the team know in 90 days whether this happened?
- **Connection to a theme** — actually addresses one of the themes

The rest go in a "we discussed but didn't commit" appendix.

**Don't ask the model to pick.** The model doesn't know the team's capacity.

## Step 5 — The public write-up [NARRATE]

Run **Prompt #17 (Retro write-up drafter)** for sections 2 and 3. You write the rest.

Six sections:

1. One-line summary
2. What worked (Prompt #17 drafts)
3. What didn't (Prompt #17 drafts)
4. What we're changing (your action items)
5. What we discussed but didn't commit to
6. A short note on the room (feelings-temperature)

Read the whole write-up aloud with the room in mind. If you stumble, rewrite.

## Step 6 — One-page summary (if needed) [NARRATE, optional]

For sharing up to managers or across teams. Two-line summary, 3–5 bullets on what's changing, one sentence on team sentiment. The model drafts from the write-up; you edit lightly.

## Step 7 — The pre-send check [SOCIAL]

Send the draft to one quiet voice and one loud voice from the room. Ask: *does this read fairly?*

If the EM says "the cross-team section is sharper than the room was," sharpen back. If the quiet engineer says "the trust dissent is named, thank you," you got the dissent right.

**This step adds an hour. It saves relationships.**

## Post-mortem variant

For incidents or failed projects, add Steps 1.5 and 3.5:

- **1.5 — Post-mortem timeline structurer** (Prompt #18) — does NOT impose retrospective clarity
- **3.5 — Cause-vs-blame check** (Prompt #19) — names the cause, not the person

See [`post-mortem-variant.md`](post-mortem-variant.md).

## Source

*The Synthesis Playbook*, Chapter 8 "Retro & post-mortem synthesis."
