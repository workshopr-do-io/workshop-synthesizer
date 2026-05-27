---
description: Workshop Synthesis index + decision tree — which recipe to use for which workshop
model: sonnet
---

Entry point for the Workshop Synthesis plugin. Walk the user through the decision tree below; route to the appropriate `/ws-*` slash command based on the workshop they just ran.

| Workshop type | Slash command |
|---|---|
| Customer discovery, user interviews, CAB, persona work | `/ws-discovery` |
| Executive offsite, board strategy day, founder/board | `/ws-offsite` |
| GV-style design sprint, prototype validation | `/ws-sprint` |
| Half-day ideation, brainstorm, roadmap workshop | `/ws-ideation` |
| Team retro, sprint retro, blameless post-mortem | `/ws-retro` |
| Multi-day training, cohort program, cross-functional alignment | `/ws-training` |

If unsure, ask: how many people in the room, was there a Decide vote, who's the audience?

Mode reference: `MODE_REGISTRY.md`.
Framework entry: `synthesis-framework/SKILL.md`.
