# Prompt #14 — Sequencing critic (roadmap variant)

> **From:** *The Synthesis Playbook*, prompt appendix, #14.
> **Recipe:** Ideation (Ch 7) — Roadmap ADAPT sidebar.
> **Used at:** Step 4.5 — [PRIORITIZE] in `skills/synthesis-ideation/SKILL.md` (roadmap variant only).
> **Workhorse:** Yes.

## The prompt

```
Here is the proposed roadmap: [paste with Now/Next/Later assignments].

For each item, identify whether its time horizon is constrained by:

1. Dependencies — needs another item to land first.
2. Resourcing — needs a team member or budget that's committed elsewhere.
3. Market timing — needs an external condition (customer signal,
   competitor move) to be true.
4. Organizational readiness — needs a process or capability the team
   doesn't have yet.

Then identify any sequencing errors: items in Now that have unresolved
dependencies in Next, items in Later that could move forward if a Now
item shifted, and Now items that compete for the same resource.
```

## What to customize

- `[paste]` — your proposed roadmap with each item assigned to Now / Next / Later

## Why this prompt is the roadmap-specific value-add

It catches the most common roadmap failure — *a roadmap that ranks well but doesn't sequence well, because the dependencies got glossed.*

The Now bucket tends to fill with the top-rated items, regardless of whether they can actually start. Three months later, two of the Now items are blocked, the team is frustrated, and the roadmap looks broken even though the ranking was correct.

**Never publish a roadmap without running the sequencing critic.**

## What to do with the output

For each flagged sequencing error:

- **Move the blocked item to Next** — and elevate the dependency to Now
- **Promote a Later item to Now** — if the prerequisite has actually shifted
- **Resolve the resource conflict** — by either compressing scope, adding capacity, or moving one item to Next

## Common failures

- **Model misses dependencies that come from organizational context rather than technical.** "We can't ship this until Marketing has hired a launch lead" is the kind of dependency the model doesn't see. Add these by hand.
- **Model over-flags market-timing dependencies.** Not every item needs to wait for a customer signal. If everything is flagged as market-timing-dependent, you're under-committing.

## License

MIT. See `/LICENSE`.
