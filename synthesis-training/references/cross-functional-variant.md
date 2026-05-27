# Cross-Functional Alignment Workshop Variant

A cross-functional alignment workshop is a session where the deliverable has to land with multiple functions — product, engineering, GTM — none of whom were the "client" but all of whom have to live with the outcome.

The recipe shape is the same as training debrief. The audiences are different and the politics is sharper.

## What's different

### Audience swap

Instead of three audiences (participants, program owner, budget-holder), you have:

- **Three or four functions** in the room (product, engineering, GTM, design)
- **A single decision-maker** (usually a VP or director who convened the room)

Both are served by the same deliverable structure but at different altitudes.

### Replace Steps 2 and 3 with the position-mapper + real-disagreement surfacer

- **Step 2 (was: cohort-pattern surfacer):** Use **Prompt #22 (Position-mapper across functions)** instead. See [`/prompts/training/22-position-mapper.md`](../../prompts/training/22-position-mapper.md).
- **Step 3 (was: program-design signal extractor):** Use **Prompt #23 (Real-disagreement surfacer)** instead. See [`/prompts/training/23-real-disagreement-surfacer.md`](../../prompts/training/23-real-disagreement-surfacer.md).

### Deliverable structure

Instead of participant write-up + cohort analysis + one-pager:

1. **Function-by-function summary** — what each function committed to, what each function parked
2. **Cross-function decision summary** — what the room landed on, with explicit naming of trade-offs
3. **"Recommendation everyone can live with" framing** — not necessarily love
4. **Parked-disagreement appendix** — mandatory, named in the executive summary

### The parked-disagreement appendix is mandatory

The pitfall that matters most for cross-functional alignment: **synthesis that papers over the parked disagreements.**

The room ended with the disagreements parked, not resolved. The synthesis pretends they were resolved. Six weeks later, the parked disagreement surfaces as friction in execution.

**Fix:** Name parked disagreements in the executive summary. *We landed on direction A. We did not resolve [specific disagreement between functions X and Y]. That disagreement will need to be addressed by [date] or it will surface in execution.*

## Worked example seed

A product/eng/GTM disagreement on a launch date. The stated disagreement was timing (eng said February, GTM said December). The real-disagreement surfacer revealed the actual disagreement was scope — eng wanted a smaller launch in February, GTM wanted the full feature set in December.

Once the synthesis named the scope question explicitly, the room could be reconvened for a 30-minute follow-up that resolved it (smaller launch in December, full feature set rolling out through Q1). **The synthesis that named the real disagreement saved a quarter of execution friction.**

## What's the same as base training debrief

- The pulse data and co-facilitator notes (where applicable)
- The aloud test, three times
- The audience-tiered narrator discipline
- The COI patterns around naming functions vs. naming individuals

## Common failures specific to this variant

- **Papering over parked disagreements.** Most common failure. The mandatory parked-disagreement appendix is the fix.
- **Naming individual function members.** Don't. Name the function, not the person. *GTM raised cost concerns* is fine. *Maria raised cost concerns* is not (unless Maria is the decision-maker the deliverable is addressed to).
- **Treating the stated disagreement as the real disagreement.** This is what Prompt #23 (Real-disagreement surfacer) addresses. Use it.

## Source

*The Synthesis Playbook*, Chapter 9 "Training & workshop debrief synthesis," Cross-functional alignment ADAPT sidebar.
