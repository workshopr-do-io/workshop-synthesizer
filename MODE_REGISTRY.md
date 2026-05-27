# Mode Registry

Single source of truth for all recipes and variants across the Workshop Synthesis suite. **6 recipes + 1 framework + 1 prompt library**, each with optional ADAPT variants.

When adding or modifying recipes, update this file first — SKILL.md files and command files should reference this registry.

Last updated: v0.1.0 (2026-05-27)

---

## synthesis-discovery (Ch 4 — interpretation-heavy)

> **Move mix:** 30% [CLUSTER] · 40% [INTERPRET] · 10% [PRIORITIZE] · 20% [NARRATE]

| Mode | Spectrum | Output | Oversight | Triggers |
|------|----------|--------|-----------|----------|
| `full` | Balanced | Opportunity-areas deck + Notion brief | High | "discovery synthesis", "synthesize interviews", "I just ran user interviews", "opportunity areas readout" |
| `cab` | Balanced | CAB synthesis with cross-session deduping | High | "Customer Advisory Board synthesis", "CAB readout" |
| `persona` | Balanced | Persona / JTBD archetypes + tensions | High | "persona work", "JTBD synthesis", "archetype clustering" |

## synthesis-offsite (Ch 5 — politics-heavy mix)

> **Move mix:** 10% [CLUSTER] · 30% [INTERPRET] · 30% [PRIORITIZE] · 30% [NARRATE]

| Mode | Spectrum | Output | Oversight | Triggers |
|------|----------|--------|-----------|----------|
| `full` | Fidelity | CEO memo + board deck + confidential appendix | Very High | "executive offsite synthesis", "C-suite readout", "CEO memo from offsite" |
| `founder-board` | Fidelity | Founder/board memo + appendix | Very High | "founder/board strategy day", "board-only working session" |

**Hardest recipe in the book.** The model assists with ~15% of the work. Day-One Read brief is mandatory.

## synthesis-sprint (Ch 6 — prioritize + narrate)

> **Move mix:** 15% [CLUSTER] · 25% [INTERPRET] · 35% [PRIORITIZE] · 25% [NARRATE]

| Mode | Spectrum | Output | Oversight | Triggers |
|------|----------|--------|-----------|----------|
| `full` | Balanced | Monday recommendation (ship/iterate/abandon/third option) | High | "design sprint synthesis", "Friday user tests", "Monday recommendation" |
| `mini` | Balanced | Compressed recipe for 1-week sprints | High | "mini sprint", "one-week sprint synthesis" |
| `prototype` | Balanced | Prototype validation outside sprint container | Medium | "prototype validation", "5-tester recommendation" |

Send Sunday night, not Monday morning. The four possible recommendations are exactly that — four. Don't invent a fifth.

## synthesis-ideation (Ch 7 — prioritize-dominant)

> **Move mix:** 20% [CLUSTER] · 15% [INTERPRET] · 50% [PRIORITIZE] · 15% [NARRATE]

| Mode | Spectrum | Output | Oversight | Triggers |
|------|----------|--------|-----------|----------|
| `full` | Balanced | Ranked shortlist (8–15) + kill list + next steps | Medium | "ideation synthesis", "200 stickies", "ranked shortlist", "kill list" |
| `roadmap` | Balanced | Same + sequencing critic (Now/Next/Later) | Medium | "roadmap synthesis", "quarterly roadmap workshop" |

The dots are seductive. The criteria are trustworthy. Every shortlist has a weird outlier.

## synthesis-retro (Ch 8 — cluster-dominant, dissent-preserving)

> **Move mix:** 40% [CLUSTER] · 30% [INTERPRET] · 10% [PRIORITIZE] · 20% [NARRATE]

| Mode | Spectrum | Output | Oversight | Triggers |
|------|----------|--------|-----------|----------|
| `full` | Balanced | Public write-up + action items + minority views | High | "retro synthesis", "team retro write-up", "minority view" |
| `post-mortem` | Fidelity | + timeline + cause-vs-blame check | High | "post-mortem", "blameless post-mortem", "incident review" |
| `project` | Balanced | + "what we would have done differently" | High | "project retro", "post-launch retro" |

The minority view is the data, not the noise.

## synthesis-training (Ch 9 — interpret + narrate, 3 audiences)

> **Move mix:** 15% [CLUSTER] · 35% [INTERPRET] · 20% [PRIORITIZE] · 30% [NARRATE]

| Mode | Spectrum | Output | Oversight | Triggers |
|------|----------|--------|-----------|----------|
| `full` | Balanced | Participant write-up + cohort analysis + one-pager | High | "training debrief", "cohort report", "personalized paragraph" |
| `cross-functional` | Balanced | Position map + parked-disagreement appendix | High | "cross-functional alignment workshop", "function-by-function summary" |
| `sales-customer` | Balanced | Shorter participant write-up + numbers-heavy cohort analysis | Medium | "sales training debrief", "customer-facing training" |

The personalized paragraph is the load-bearing artifact. ~4–8 hours of writing for 16 participants.

## synthesis-framework (Chs 1–3 — foundation, no modes)

The taxonomy. Loaded implicitly by every recipe. Read it once.

- Four moves (cluster, interpret, prioritize, narrate)
- Synthesis stack (5 layers)
- Synthesis-ready file template
- Stakes × Politics matrix
- "Human-authored, machine-assisted" principle
- Consent and data discipline

## synthesis-prompt-library (Ch 10 — meta-skill, no modes)

The twelve workhorses, the four-part prompt grammar, versioning discipline, the shrinkage rule. Use when extending the recipes to workshop types the book doesn't cover.

---

## Slash command → mode mapping

| Slash command | Skill | Default mode | Variant flags |
|---|---|---|---|
| `/ws-help` | (all) | index + decision tree | — |
| `/ws-discovery` | synthesis-discovery | `full` | `cab`, `persona` |
| `/ws-offsite` | synthesis-offsite | `full` | `founder-board` |
| `/ws-sprint` | synthesis-sprint | `full` | `mini`, `prototype` |
| `/ws-ideation` | synthesis-ideation | `full` | `roadmap` |
| `/ws-retro` | synthesis-retro | `full` | `post-mortem`, `project` |
| `/ws-training` | synthesis-training | `full` | `cross-functional`, `sales-customer` |

## Oversight legend

- **Very High** — human-authored steps at multiple checkpoints; model closed for 30%+ of the work
- **High** — human pauses at 2–3 named checkpoints; model assists with mechanical work
- **Medium** — human pauses at 1–2 checkpoints; model runs most of the workflow
- **Low** — not used in this plugin (synthesis is human-authored by design)

## Spectrum legend

- **Fidelity** — template-heavy, predictable output (used for high-stakes / high-politics recipes)
- **Balanced** — default, mix of structure and judgment
- **Originality** — exploratory, template-light (not used in v0.1; reserved for future Socratic modes)

---

## Source

*The Synthesis Playbook* (Workshopr facilitation series, Book 6), Chapters 4–9 (recipes), Chapter 10 (prompt library), Chapter 11 (agentic pipelines).
