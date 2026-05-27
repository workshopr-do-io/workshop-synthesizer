# Training & Workshop Debrief Recipe — Full Workflow

> **Move mix:** 15% [CLUSTER] · 35% [INTERPRET] · 20% [PRIORITIZE] · 30% [NARRATE]

Three audiences, three altitudes, three documents. The room was the deliverable; the synthesis is the receipt.

## Prerequisite: synthesis-ready file

- All facilitation notes from each session
- Each participant's 30-60-90 plan (the most important single artifact)
- Pulse survey responses
- Co-facilitator observation notes (especially role-play notes)
- Closing-circle recording or transcript
- A pre-program baseline (what each participant said walking in)
- The program design
- A cohort roster with each person's role, tenure, pre-program manager note

**The crucial item is the baseline-to-close pair** — what each participant said at the start, what they said at the end. Without it, the synthesis reports on outputs instead of outcomes.

## Step 1 — Build the baseline-to-close pair [INTERPRET prep]

For each participant, write a structured record:

> **[Participant name].** **Baseline:** [what they said they wanted, in their words]. **Close:** [what they said they took away, in their words]. **Distance:** [your read of how much they moved and on what specifically].

This is the foundation. Spend the time. ~4 hours for 16 participants.

For some participants the pair will be neat (*baseline: I want to learn how to give hard feedback. Close: I learned a framework and used it on day two*). For others, revealing (*baseline: I want to be a better manager. Close: I realized I don't want to be a manager*). Both are valid. The first is a competency move; the second is a career move. Both go in the write-up, with care.

## Step 2 — Identify the cohort's pattern [CLUSTER → INTERPRET]

Run **Prompt #20 (Cohort-pattern surfacer)**. Look for sub-cohorts, strongest-and-weakest competency movement, participants whose growth direction surprised the design, participants who moved less than the others.

You verify by hand. The model is pattern-matching from text; it can't see who's recently joined the team, who's in a hard situation.

## Step 3 — Identify program-design signals [INTERPRET]

Run **Prompt #21 (Program-design signal extractor)**. For each session: strength signal, friction signal, skill demonstration vs. discussion.

The demonstration-vs-discussion distinction is the diagnostic that predicts whether a competency actually landed.

## Step 4 — Participant write-up [NARRATE]

The document each participant receives. Six sections:

1. Short opening addressed to the cohort
2. What the program was meant to do (one paragraph)
3. What the cohort got on average (one paragraph — the pattern from Step 2)
4. What to practice now (3–4 bullets at the cohort level)
5. **A personalized paragraph** addressed to the individual participant by name — your voice, 3–5 sentences, citing one specific moment from the program
6. What comes next (post-program touchpoints)

**The personalized paragraph is the single most authorship-heavy moment in any recipe in this book.** See [`personalized-paragraph-template.md`](personalized-paragraph-template.md).

Sixteen of these. 4–8 hours.

## Step 5 — Cohort-level analysis [NARRATE]

The program owner's document. 6–10 pages. Six sections:

1. Cohort summary
2. Cohort movement patterns
3. Skill demonstration vs. discussion
4. Program-design signals (session-by-session)
5. **The flags section** — participants whose movement was below cohort average (mandatory; do not skip)
6. Recommended next-cohort changes

The flags section requires human writing — the model will soften too much to name names.

## Step 6 — Budget-holder one-pager [NARRATE]

One page for the VP, customer exec, or budget-holder. Five sections:

1. One-line summary
2. Three outcome bullets (specific, with numbers where possible)
3. **Two named stories** (anonymized but specific — these survive the retelling test)
4. One recommended next investment
5. A note on what didn't work (mandatory — pure success documents lose credibility)

The named stories are what get re-told in meetings where you won't be in the room. Spend time on them.

## Step 7 — Aloud test, three times [NARRATE check]

Read each document aloud as if you were its audience.

- Participant write-up — as if you were the participant. Does the personalized paragraph land?
- Cohort analysis — as if you were the program owner. Does the flags section give them what they need to act?
- One-pager — as if you were the budget-holder re-telling it to your CEO. Does the retelling work?

The one-document approach (write once, trim for each audience) never survives this test. The audiences are too different.

## Cross-functional alignment variant

If running a cross-functional alignment workshop instead of training, swap Steps 2 and 3 for:

- Position-mapper across functions (Prompt #22)
- Real-disagreement surfacer (Prompt #23)

See [`cross-functional-variant.md`](cross-functional-variant.md).

## Source

*The Synthesis Playbook*, Chapter 9 "Training & workshop debrief synthesis."
