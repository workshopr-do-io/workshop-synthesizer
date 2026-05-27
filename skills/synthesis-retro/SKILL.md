---
name: synthesis-retro
description: >
  Synthesize a team quarterly retro, sprint retro, project retro, or
  blameless post-mortem. Cluster-dominant recipe with one job above all
  others: preserve dissent. The minority view is the data, not the
  noise. Use when the user has just run a team retro or post-mortem
  and needs a public write-up that protects quiet voices and surfaces
  patterns without becoming a blame document. Triggers on: "synthesize
  retro", "retro write-up", "post-mortem", "blameless post-mortem",
  "minority view", "trust sticky", "what went wrong", "blame vs cause".
---

# Retro & Post-Mortem Synthesis Recipe

> **Move mix:** 40% [CLUSTER] · 30% [INTERPRET] · 10% [PRIORITIZE] · 20% [NARRATE]
> **Dominant move:** [CLUSTER] (dissent-preserving)

Retros are workshops about things that broke. The dissent is the data, not noise around the signal. A retro synthesis that smooths the disagreement is a retro synthesis that lies about the team.

The other thing that makes retros different: the team will read the write-up. They will look for whether their voice was captured fairly. The political weight is relationship-high, not stakes-high.

## When to use this recipe

- Team quarterly retros (8–15 people, 90–120 minutes)
- Sprint retros
- Project retros (shipped or didn't)
- Blameless post-mortems on incidents (see Post-mortem variant)
- Cross-functional alignment retros

## When NOT to use this recipe

- C-suite political sessions (use `synthesis-offsite`)
- Sprint readouts with user testing (use `synthesis-sprint`)
- Ideation sessions (use `synthesis-ideation`)

## The workflow at a glance

1. **Structure and cluster** — [CLUSTER] Three-pass prompt: cluster within column → cross-column linking → minority view extraction.
2. **Distinguish noise from real dissent** — [CLUSTER critic] Real structural dissent / one-off frustration / adjacent topic / vague signal. Real dissent goes in the write-up.
3. **Interpret linked themes** — [INTERPRET] You write one paragraph per linked theme, by hand. Use the retro stress-test prompt for the uncomfortable framing.
4. **Action items** — [PRIORITIZE] Three to seven, named, dated, tied to themes. Beyond seven the team starts no-shipping.
5. **Public write-up** — [NARRATE] Six sections: one-line summary / what worked / what didn't / what we're changing / what we discussed but didn't commit / room temperature note.
6. **One-page summary** — [NARRATE, optional] For sharing up to managers or across teams.
7. **Pre-send check** — [SOCIAL] Send draft to one quiet voice and one loud voice in the room. Listen carefully. Edit.

For post-mortems: **add Steps 1.5 (timeline structurer) and 3.5 (cause-vs-blame check).** See [`references/post-mortem-variant.md`](references/post-mortem-variant.md).

Full step-by-step: [`references/workflow.md`](references/workflow.md).

## The prompts (5)

| # | Prompt | Used at |
|---|---|---|
| 15 | Retro sticky clusterer with explicit minority-view output | Step 1 [CLUSTER] |
| 16 | Dissent-vs-noise distinguisher | Step 2 [CLUSTER critic] |
| 17 | Retro write-up drafter | Step 5 [NARRATE] |
| 18 | Post-mortem timeline structurer | Step 1.5 (post-mortem only) |
| 19 | Cause-vs-blame check | Step 3.5 (post-mortem only) |

Verbatim text: [`references/prompts.md`](references/prompts.md). Copy-paste: [`../../prompts/retro/`](../../prompts/retro/).

## Reference files

| File | Load when... |
|---|---|
| [`references/workflow.md`](references/workflow.md) | Running the recipe end-to-end |
| [`references/prompts.md`](references/prompts.md) | Need the 5 prompts in one place |
| [`references/pitfalls.md`](references/pitfalls.md) | Synthesis is polishing the loudest theme; minority view is getting buried |
| [`references/worked-example.md`](references/worked-example.md) | Want to see what dissent-preservation looks like (trust-sticky composite) |
| [`references/post-mortem-variant.md`](references/post-mortem-variant.md) | Blameless post-mortem on an incident or failed project |
| [`references/project-retro-variant.md`](references/project-retro-variant.md) | Project retro (shipped or didn't) |

## Pipeline agent

[`agents/retro_pipeline_agent.md`](agents/retro_pipeline_agent.md) implements the 7-step workflow. Pauses at Step 3 (you write the interpretation) and Step 4 (you pick the action items). The pre-send check is your social work, not the agent's.

## Where AI hurts

- **Final language on minority views.** Model defaults to politely softening dissent. The minority view needs to retain enough sharpness to read as real.
- **Action item ownership decisions.** Model doesn't know who has capacity or political weight.
- **The room temperature note.** The most human paragraph in the write-up. Always by hand.
- **The pre-send check.** Don't ask the model to predict how the room will react. Ask a real person.

## The bottom line

Retros are about dissent preservation. The cluster move dominates because the cluster step is where dissent gets flattened. Every theme that touches disagreement carries a minority-view subsection. The minority view is the data.

For post-mortems: name the cause, not the blame. The system failed, not the person who tripped over the system. Hold the messy-but-true sequence of decisions; do not impose retrospective clarity.

## Source

*The Synthesis Playbook*, Chapter 8 "Retro & post-mortem synthesis." Worked example (the trust sticky, eleven-person engineering team) is a composite.
