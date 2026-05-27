# Roadmap Variant — Ideation Recipe + Sequencing

The roadmap workshop is ideation plus alignment. You're not just ranking ideas, you're sequencing bets across time horizons and committing functions to them.

## What's different from base ideation

Three differences from the standard ideation recipe.

### 1. Sequencing is the new prioritization

A roadmap workshop produces ideas **with time horizons** — Now, Next, Later. The synthesis ranks within each horizon **and** asks: is the sequencing right?

- Could a Now item actually be a Next item if the Later item lands first?
- Could a Next item be a Now if we resourced it differently?

**Run Prompt #14 (Sequencing critic) after Step 4 of the base recipe** — see [`/prompts/ideation/14-sequencing-critic.md`](../../prompts/ideation/14-sequencing-critic.md).

The prompt identifies whether each item's time horizon is constrained by:
- **Dependencies** — needs another item to land first
- **Resourcing** — needs a team member or budget committed elsewhere
- **Market timing** — needs an external condition (customer signal, competitor move)
- **Organizational readiness** — needs a process or capability the team doesn't have yet

### 2. Function commitments

A roadmap commits people, not just ideas. The synthesis names which function (product, engineering, design, GTM) owns each Now item. The synthesis surfaces conflicts: *engineering is committed to three Now items that share the same team.*

In the readout, include a one-slide "function commitments" view:

| Item | Owner function | Owner person | Date committed |
|---|---|---|---|
| ... | ... | ... | ... |

Look for the conflicts. Three Now items with the same owner is a roadmap that won't survive Q2.

### 3. The dependency map

The roadmap deliverable usually includes a small map showing which items depend on which. The model can draft it from the sequencing critic's output. You verify by hand — the model will sometimes miss dependencies that come from organizational context rather than technical context.

## The pitfall that matters most

**A roadmap that ranks well but doesn't sequence well.**

The Now bucket fills with the top-rated items, regardless of whether they can actually start. Three months later, two of the Now items are blocked, the team is frustrated, and the roadmap looks broken even though the ranking was correct.

**Fix:** Never publish a roadmap without running the sequencing critic. One step. Five minutes. Saves a quarter.

## Worked example seed

A quarterly roadmap exercise at a mid-size company. Top-rated item by criteria was *Build a new data export feature.* The sequencing critic flagged it: the data export depended on a schema migration that was sitting in Next.

The synthesis moved the data export to Next and surfaced the schema migration as the actual Now-priority enabler. The team initially resisted (the data export was the customer-visible win they wanted to ship), but accepted the sequence.

The roadmap held all quarter. Three months later the data export shipped on time, after the schema migration landed clean.

## When NOT to use the roadmap variant

If the room generated ideas without time-horizon commitments, you're running the base ideation recipe — not the roadmap variant. The variant adds work that doesn't pay back if there are no horizon decisions to make.

If the team's "roadmap" is actually just a prioritized backlog without time commitments, treat it as base ideation. The variant is for actual roadmaps with Now/Next/Later structure.

## Source

*The Synthesis Playbook*, Chapter 7 "Ideation & roadmap synthesis," Roadmap ADAPT sidebar.
