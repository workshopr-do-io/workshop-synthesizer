# Prompt #25 — Archetype clusterer (Persona/JTBD variant)

> **From:** *The Synthesis Playbook*, prompt appendix, #25.
> **Recipe:** Discovery (Ch 4) — Persona/JTBD ADAPT sidebar.
> **Used at:** Replaces standard [CLUSTER] step for persona work.

## The prompt

```
Here are the interview transcripts: [paste].

Group the interviewees into candidate archetypes based on:

1. The job they're trying to get done (not the role they have).
2. The context around when they reach for a product like ours.
3. The success criterion they use, in their own words.

Aim for 3–5 archetypes. Do not create archetypes based on demographics,
company size, or industry unless those are the behavioral drivers.
Archetypes are about jobs and contexts, not about census categories.

For each archetype: name it (an evocative name, not "Persona 1"), one
sentence on the job, one sentence on the context, two representative
quotes verbatim.
```

## What to customize

- `[paste]` — concatenated interview transcripts (same input as prompt #1)

## Why "not demographics"

The persona work that ages worst is the one where archetypes are built around census categories — age brackets, company size buckets, industries — instead of behavioral drivers. The book is explicit: archetypes are about *jobs and contexts*, not about who fits in which demographic box.

If your archetypes could be redrawn by swapping age bands or revenue brackets, they aren't archetypes. They're segmentation by census.

## Pair with prompt #26

After archetypes are drafted, **run [the archetype tension finder (#26)](26-archetype-tension-finder.md)** to surface where archetypes overlap or conflict. Personas that don't tension against each other usually aren't sharply defined enough.

## Common failures

- **Archetypes too narrow or too broad.** 3–5 is the target. If the model returns 8+, re-prompt: "Consolidate adjacent archetypes; the differentiator must be behavioral."
- **Generic archetype names.** "Persona 1," "Early Adopter," "Power User" — re-prompt: "Use evocative names tied to the archetype's specific job."

## License

MIT. See `/LICENSE`.
