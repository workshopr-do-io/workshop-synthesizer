# Strategic Offsite Recipe — Full Workflow

> **Move mix:** 10% [CLUSTER] · 30% [INTERPRET] · 30% [PRIORITIZE] · 30% [NARRATE]

The hardest recipe in the book. The model assists with ~15% of the work; the rest is yours.

## Prerequisite: the Day-One Read brief

Before you sleep on the first night of the offsite, write a one-page brief that captures what you've read in the room — who's aligned with whom on which calls, where the tension is, what's being said versus what's being decided. Plus the one sentence that captures the CEO's pre-existing position on the big call.

Without this brief, the Sunday synthesis tries to reconstruct political reads from notes that don't carry tone. **There's no recovery if you skip it.** See [`day-one-read-brief.md`](day-one-read-brief.md).

## Step 1 — Structure the decision log [PREP]

Your decision log is messy — co-authored with the chief of staff, written under pressure. Clean it into structured form.

Run **Prompt #5 (Decision log structurer)**. For each major decision, the model produces:
- The question as posed
- The room's answer in one sentence
- Decision quality (committed / leaning / parked / open)
- Who advocated (if explicit in notes only)
- Follow-up if named

You add attribution and pushback notes by hand. ~30 min.

## Step 2 — Political read [INTERPRET, model off]

**The model is closed.**

Sit with the decision log and your Day-One Read brief. For each decision, write a 3–4 sentence political note:

> **Decision:** [the question, the answer]
> **Content:** [why the room landed where it did, what evidence informed it]
> **Politics:** [who pushed for what, what the alignment shifted to, what was unsaid]
> **Confidence:** [how durable this decision is — will it hold next week?]

You write this by hand because the model can't. The model wasn't in the room.

~60 min.

## Step 3 — Prioritize decisions across artifacts [PRIORITIZE]

Decide which decisions belong in which artifact:

- **Committed decisions** → board deck + CEO memo
- **Leaning decisions** → CEO memo; board deck only if framed as direction-of-travel
- **Parked decisions** → CEO memo, board deck only if material
- **Open decisions** → CEO memo only. Never board deck.
- **Pure political observations** → confidential appendix only.

Use **Prompt #6 (Argue-the-other-side critic)** to sanity-check contested cuts.

## Step 4 — Draft the CEO memo [NARRATE, with model assist]

Six sections:

1. Opening paragraph — your voice, addressed to the CEO
2. Committed calls — model drafts (use **Prompt #7 — CEO memo draft assist**)
3. Leaning calls — adapt Prompt #7 with explicit "what would push the lean to a commit"
4. Parked calls — short list, dates
5. What the room did not resolve — your voice, from scratch (the most important section)
6. A short note from the facilitator — your read on the room

## Step 5 — Draft the board deck [NARRATE, with model assist]

12–15 slides at board altitude. Model drafts the committed-calls slides; you write the cover, "what we're not doing" slide, and "asks of the board" slide.

**Do not put internal pushback in the board deck.** Default to omission and let the CEO add it back if they want.

## Step 6 — Draft the confidential appendix [NARRATE, model off]

**The model is closed.**

One to two pages, prose, for the CEO alone. Personnel observations, cultural friction, the CEO's own pattern, what's likely to surface in the next offsite.

Save locally, encrypted if possible, and hand to the CEO directly rather than emailing.

## Step 7 — Political read pass [INTERPRET, model off]

**The model is closed.**

Read all three artifacts back-to-back in altitude order (memo → deck → appendix). Catch leaks. Memo content shouldn't show up in the deck; appendix content shouldn't show up anywhere else.

## Step 8 — In-person handoff [SOCIAL]

Schedule a one-hour debrief with the CEO. Bring printed copies of the memo and appendix. **No laptop.** Walk the CEO through both in person. Watch their face. Listen to the questions.

After the debrief, revise based on feedback. Then send the memo + deck by email. Keep the appendix in-person only.

## Why so few prompts

The recipe uses only three prompts (#5, #6, #7). That is deliberate. If you find yourself reaching for more, you're trying to outsource judgment that has to stay with you. Stop, close the model, write by hand.

## Source

*The Synthesis Playbook*, Chapter 5 "Strategic offsite & stakeholder politics."
