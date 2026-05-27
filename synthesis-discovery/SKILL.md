---
name: synthesis-discovery
description: >
  Synthesize a customer discovery sprint, foundational research round,
  interview round, voice-of-customer study, Customer Advisory Board, or
  persona/JTBD work into opportunity areas, insight statements, and
  recommended next steps. Cluster-and-interpret-heavy recipe. Use when the
  user has just run interviews or qualitative research and needs a defensible
  readout — deck, brief, one-pager. Triggers on: "synthesize discovery",
  "discovery synthesis", "I just ran user interviews", "opportunity areas",
  "discovery readout", "CAB synthesis", "persona work", "JTBD synthesis".
---

# Discovery & Qualitative Synthesis Recipe

> **Move mix:** 30% [CLUSTER] · 40% [INTERPRET] · 10% [PRIORITIZE] · 20% [NARRATE]
> **Dominant move:** [INTERPRET]

The recipe for turning a pile of interview transcripts and stakeholder stickies into something the client can act on. The bigger the pile, the more the model helps at [CLUSTER]. The most uncomfortable findings — the ones you got paid for — surface at [INTERPRET].

## When to use this recipe

- Customer discovery sprints (10–20 interviews + stakeholder sessions)
- Foundational research rounds
- Voice-of-customer studies
- Customer Advisory Boards (single quarter or across quarters — see CAB variant)
- Persona or Jobs-to-be-Done work (see Persona/JTBD variant)

## When NOT to use this recipe

- Strategic offsites (use `synthesis-offsite`)
- Design sprints with Decide votes (use `synthesis-sprint`)
- Half-day ideation sessions (use `synthesis-ideation`)
- Team retros (use `synthesis-retro`)

## The workflow at a glance

1. **Prepare transcripts** — [CLUSTER prep] Concatenate, tag with interviewee context. Don't clean filler words. 20 min.
2. **First-pass cluster** — [CLUSTER] Three-pass prompt: extract quotes → cluster → theme summary. ~5 min model time.
3. **Anti-flattening pass** — [CLUSTER critic] **Do not skip.** Surfaces the buried contrarian quote that was the whole point of the engagement.
4. **Interpretation** — [INTERPRET] You write the one-sentence interpretation per theme, by hand. Then use the stress-test prompt against your own draft.
5. **Opportunity framing** — [INTERPRET → NARRATE bridge] Three candidate framings per theme (JTBD, HMW, plain-language). Pick one.
6. **Prioritization** — [PRIORITIZE] Model closed. Score against evidence sharpness, uncomfortable-truth content, and 90-day actionability. Cut to 3–5.
7. **Narrative** — [NARRATE] Draft the deck. Call slide on slide 3, max. Then the brief.
8. **Aloud test** — Read the deck out loud. Stumble → rewrite.

Full step-by-step workflow: [`references/workflow.md`](references/workflow.md).

## The prompts (7)

| # | Prompt | Used at |
|---|---|---|
| 1 | Transcript-to-quotes extractor + first-pass clusterer | Step 2 [CLUSTER] |
| 2 | Anti-flattening critic | Step 3 [CLUSTER critic] |
| 3 | Interpretation stress-test | Step 4 [INTERPRET] |
| 4 | Opportunity-area framer | Step 5 [INTERPRET → NARRATE] |
| 24 | Cross-session deduper (CAB variant) | Cross-quarter CAB only |
| 25 | Archetype clusterer (Persona/JTBD variant) | Persona/JTBD only |
| 26 | Archetype tension finder | Persona/JTBD only |

Verbatim prompt text: [`references/prompts.md`](references/prompts.md). Copy-paste versions: [`../prompts/discovery/`](../prompts/discovery/).

## Reference files

| File | Load when... |
|---|---|
| [`references/workflow.md`](references/workflow.md) | Running the recipe end-to-end |
| [`references/prompts.md`](references/prompts.md) | Need the 7 prompts in one place |
| [`references/pitfalls.md`](references/pitfalls.md) | Something is going wrong in the synthesis |
| [`references/worked-example.md`](references/worked-example.md) | Want to see what a finished synthesis looks like (Mid-Co composite) |

## Pipeline agent

[`agents/discovery_pipeline_agent.md`](agents/discovery_pipeline_agent.md) implements the 8-step workflow as an agentic loop: runs steps 1–3, 5–6, and 8 automatically; pauses at steps 4 ([INTERPRET]) and 7 ([PRIORITIZE]) for your authorship. Invoke via `/ws-discovery` slash command.

## Where AI hurts

Three places to keep the model out:

- **Final prioritization.** The 3–5 opportunity areas that survive are a political call about which uncomfortable truths the client can stomach this quarter. The model has no view on this. Pick by hand.
- **The call slide.** Single sentence at the top of the deck. Highest-stakes sentence in the whole deliverable. Write it yourself.
- **Quote attribution.** Model occasionally invents or misattributes. Verify every quote against the source transcript. 30 minutes, no exceptions.

## The bottom line

Discovery is interpretation-heavy. The model helps you cluster, but the cluster is candidate, not final. The anti-flattening pass is the single most important step — skip nothing else, but skip that and you ship a synthesis that smooths the spiky quote that was the whole point.

A successful Discovery synthesis returns the inconvenient finding. If you've written something the client could have written from their desk in an hour, go back.

## Source

*The Synthesis Playbook*, Chapter 4 "Discovery & qualitative synthesis." Worked example (Mid-Co) lifted as composite per the book's disclosure convention.
