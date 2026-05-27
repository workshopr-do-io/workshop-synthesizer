# Using the Synthesis Playbook Without Claude Code

The plugin is a convenient runner. The prompts are the product.

If you don't run Claude Code — or don't want to — every prompt in [`prompts/`](../prompts/) works in any long-context LLM. Copy, paste, adapt.

This document is the practitioner's guide for the copy-paste path.

## What you need

1. **A long-context LLM you trust.** ChatGPT, Claude.ai, Gemini, your enterprise's hosted model. Any of the current major frontier models with 100K+ context will run these prompts.

2. **A synthesis-ready file.** Build it before the workshop ends. Template in [`synthesis-framework/references/synthesis-ready-file.md`](../synthesis-framework/references/synthesis-ready-file.md).

3. **Twenty minutes to read the framework before your first synthesis.** Don't skip this — see [`synthesis-framework/SKILL.md`](../synthesis-framework/SKILL.md).

## Three things to do before pasting anything

### 1. Check consent and data

Run the four-question check from Chapter 3 of the book (also in [`synthesis-framework/references/consent-and-data.md`](../synthesis-framework/references/consent-and-data.md)):

- Does your consent form allow third-party LLM processing?
- Is your model provider's "no training" setting on?
- Does GDPR / HIPAA / FERPA / sector-specific law apply?
- Have you stripped names, emails, IDs, and account numbers?

If any answer is uncertain, **do not paste client material.** Run the synthesis by hand or sort the consent question first.

### 2. Pin yourself on the Stakes × Politics matrix

See [`synthesis-framework/references/stakes-politics-matrix.md`](../synthesis-framework/references/stakes-politics-matrix.md). Decide before you start which quadrant your engagement is in. This tells you which moves the model is on for and which it's off for.

### 3. Pick a recipe

Match your workshop type to one of the six recipes:

| Workshop you ran | Use recipe |
|---|---|
| Customer discovery, interviews, CAB, persona work | [`synthesis-discovery/`](../synthesis-discovery/) |
| Executive offsite, board strategy day | [`synthesis-offsite/`](../synthesis-offsite/) |
| GV-style design sprint, prototype validation | [`synthesis-sprint/`](../synthesis-sprint/) |
| Half-day ideation, brainstorm, roadmap | [`synthesis-ideation/`](../synthesis-ideation/) |
| Team retro, project retro, post-mortem | [`synthesis-retro/`](../synthesis-retro/) |
| Multi-day training, cohort program, cross-functional alignment | [`synthesis-training/`](../synthesis-training/) |

## Running a recipe without the plugin

Each recipe's `SKILL.md` describes the workflow in plain English. Each `references/workflow.md` walks the steps. For each step that uses a prompt, the workflow names the prompt; find the prompt file in [`prompts/<recipe>/`](../prompts/) and copy-paste.

### A worked example — running the Discovery recipe by hand

1. Read [`synthesis-discovery/SKILL.md`](../synthesis-discovery/SKILL.md) — the recipe overview.
2. Read [`synthesis-discovery/references/workflow.md`](../synthesis-discovery/references/workflow.md) — the 8-step workflow.
3. Step 1 (Prepare transcripts) — by hand, no LLM. Concatenate transcripts.
4. Step 2 ([CLUSTER]) — open ChatGPT or Claude.ai. Copy [`prompts/discovery/01-transcript-to-quotes-and-cluster.md`](../prompts/discovery/01-transcript-to-quotes-and-cluster.md). Fill in the `[brackets]`. Paste. Run.
5. Step 3 ([CLUSTER critic]) — same chat window or new. Copy [`prompts/discovery/02-anti-flattening-critic.md`](../prompts/discovery/02-anti-flattening-critic.md). Paste and run.
6. Step 4 ([INTERPRET]) — by hand, no LLM. Write your interpretations.
7. Step 5 — use [`prompts/discovery/03-interpretation-stress-test.md`](../prompts/discovery/03-interpretation-stress-test.md) against your interpretations.
8. Step 6 — use [`prompts/discovery/04-opportunity-area-framer.md`](../prompts/discovery/04-opportunity-area-framer.md).
9. Step 7 ([PRIORITIZE]) — by hand, no LLM.
10. Step 8 ([NARRATE]) — draft by hand, use the model for tightening. Read aloud before shipping.

The plugin runs this workflow as an agent. Without the plugin, you run it as a sequence of pastes. Same recipe. Slower.

## What you give up without the plugin

- **Automation.** You paste manually between steps. The plugin pastes for you.
- **Persistent context.** Each new chat starts fresh; you re-paste earlier outputs into later prompts.
- **The pipeline pauses.** The plugin's pipeline agents enforce "model closed" at the right steps. Without the plugin, you have to enforce this yourself — close the chat tab, write by hand, then come back.

## What you keep without the plugin

- **The recipes.** All six.
- **The framework.** The four moves, the synthesis stack, the matrix, the principle.
- **The 26 prompts.** Verbatim, with customization notes and known failure modes.
- **Platform neutrality.** No lock-in. The prompts are about prompts, not about a runtime.
- **The book.** Chapters 1–12 of *The Synthesis Playbook*.

## When the manual approach tops out

The book's Chapter 11 names six signals that the manual approach has topped out:

1. You're running the same recipe more than once a month
2. Your prompts have stabilized
3. The volume per engagement is large (4,000+ stickies)
4. You're losing context across pastes
5. You collaborate with someone on the same recipe
6. You have a recurring client engagement

If two or more apply, the plugin pays back. If none apply, the manual approach is fine.

## Source

This document is original to the plugin. The book's Chapter 11 ("A gentle on-ramp to agents") describes the topped-out signals and the rationale for staying manual until volume justifies automation.
