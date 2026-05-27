# Discovery Recipe — Full Workflow

The 8-step workflow with each step's prompt, constraint, and what to do with the output.

## Prerequisite: build a synthesis-ready file before the workshop ends

For a discovery sprint, the file should point to:

- All interview transcripts (Granola, Otter, Fireflies — whichever)
- Sticky exports from stakeholder sessions (CSV)
- The original research plan and working hypotheses
- The interview guide (the actual questions you asked)
- A short closing-discussion recording from the final stakeholder session
- The interviewee list with role, tenure, pre-known context
- The deliverable spec — audience, format, due date

Plus: **the one sentence that captures what the client believed walking in.** This is the hypothesis you'll either confirm or break.

See [`synthesis-framework/references/synthesis-ready-file.md`](../../synthesis-framework/references/synthesis-ready-file.md).

## Step 1 — Prepare transcripts [CLUSTER prep]

For each interview transcript:

1. Concatenate into a single block.
2. Add a header with: interviewee name (or anonymized handle), role, tenure, date, one-line context.
3. Do **not** clean up filler words, false starts, or speaker labels.

Save as one file per interview, plus one combined file. The combined file is what the cluster pass runs on.

~20 minutes for a typical sprint.

## Step 2 — First-pass cluster [CLUSTER]

Run **Prompt #1 (Transcript-to-quotes extractor + first-pass clusterer)**.

Three passes: quote extraction → cluster → theme summary. Show each pass before moving to the next.

Read all three. **Do not skip directly to Pass 3.** The cluster looks clean at the summary level and uglier at the quote level — that ugliness is what you need to see.

You'll usually find 7–9 themes, of which 5–6 are obvious, 2–3 are borderline, and 4–7 quotes are ungrouped. Hold all of it. Don't trim yet.

## Step 3 — Anti-flattening pass [CLUSTER critic]

**The step most people skip. The step where discovery synthesis lives or dies.**

Run **Prompt #2 (Anti-flattening critic)**.

For each flagged item, do one of three things:

- **Promote to its own theme** — when the contrarian view has 2+ quotes the cluster missed
- **Mark as an explicit exception inside its theme** — when it's a real minority view but the cluster is otherwise sound
- **Park it** — when it's an outlier without enough support yet, but you don't want to lose it

After this step you usually have 7–9 themes, 1–2 newly promoted from buried quotes, 3–6 on a Park List.

## Step 4 — Interpretation [INTERPRET]

The model goes quieter. You start writing.

For each theme, write a one-sentence interpretation in your own voice. The structure:

> **Theme name.** *Interpretation:* The customer is describing [observed behavior], which means [working theory of why], which contradicts/confirms [the working hypothesis] because [reasoning].

Don't draft this in the model. Draft on paper, in a doc, in a markdown file. Your voice, your sentence.

Then run **Prompt #3 (Interpretation stress-test)** against each interpretation. The model argues the strongest case that you're wrong.

You'll discover one of three things:

- **The interpretation holds.** Alternative reading is weaker. Keep going.
- **Partially holds.** Model surfaces evidence you missed. Revise.
- **Falls apart.** Alternative is stronger. Rewrite from scratch.

The third one happens. It's painful. It's the reason the step exists. Better to rewrite on Sunday than to have a CPO take it apart on Wednesday.

## Step 5 — Opportunity framing [INTERPRET → NARRATE bridge]

Turn interpretations into opportunity areas.

An interpretation is a sentence about a finding. An opportunity area is a sentence about what the company could *do*. The shift is from observation to action-shaped framing.

Run **Prompt #4 (Opportunity-area framer)**. Three candidate framings per theme (JTBD, HMW, plain-language). Pick one per theme. The opportunity areas are drafted.

Pick **one format across the whole deck** — don't mix JTBD and HMW. Sharpest for product teams: JTBD. More inviting for cross-functional: HMW.

## Step 6 — Prioritization [PRIORITIZE]

You have 7–9 opportunity areas. The deck has room for 3–5. Time to cut.

**Model closed.** Read them. Score each against:

1. **Evidence sharpness** — 12 quotes from mixed segments > 4 quotes from one segment
2. **Uncomfortable-truth content** — the uncomfortable findings are what the client paid for
3. **90-day actionability** — opportunity areas requiring an 18-month rebuild belong in the appendix

Pick the 3–5 that score well across all three. Write the rest into a "did-not-make-the-top-tier" appendix with a one-line reason each.

The model can argue trade-offs ("argue the case that B should be top-tier instead of D"). The final pick is yours.

## Step 7 — Narrative [NARRATE]

Draft the deck. Standard discovery deck shape:

1. **Cover slide**
2. **What we did, who we talked to** — one slide. Interview count, segment mix, hypothesis walked in with.
3. **The call** — one slide. The single most important sentence: *the hypothesis was [confirmed / partially confirmed / wrong], and the bigger story underneath it is [X].* **Slide 3, max** — never slide 15.
4. **Opportunity areas** — one slide per area. Each: opportunity in one line, three quotes as evidence, recommended next step.
5. **Did-not-make-the-top-tier** — one slide with one-line reasons.
6. **Recommended next steps, organized** — 30/60/90 day buckets.
7. **Appendix** — quote library, full theme list, methodology, interviewee list.

Then draft the Notion brief. Each opportunity area gets two paragraphs instead of three quotes. Methodology gets a full page.

**Always two artifacts.** The deck carries the call. The brief carries the evidence.

The model is useful for tightening — paste a slide draft, ask for a tighter version, take what's better. **Don't ask it to draft the call slide.** That one is yours.

## Step 8 — The aloud test [NARRATE check]

Read the deck out loud. The whole thing.

If you stumble on a sentence, rewrite. If a slide bores you, the client will skip it. If the call slide doesn't make you sit up a little when you read it, it doesn't carry enough.

Then read just the call slide and the 4–5 opportunity-area slides as if they were a 5-slide deck. If those alone wouldn't be enough for the client to act on, the rest of the deck is decoration. Fix the five.

This step takes about an hour. Don't skip it.

## Quote verification (do this last, every time)

Before you ship: verify every quote in the deck against the source transcript. **By hand. By ear if there's audio.**

5–12 quotes typically survive into the final deck. Verify all of them. 30 minutes.

The model occasionally invents or misattributes. The harm is asymmetric — a misattributed quote at the readout is a credibility-killer with no "the model did it" recovery.

## Two to three days total

On a typical 14-interview sprint: two days if you're rested, three if you're not.

The CPO's reply, on a synthesis that did its job: *"Thank you for not telling me what I asked you to find."*

That's the bar.

## Source

*The Synthesis Playbook*, Chapter 4 "Discovery & qualitative synthesis."
