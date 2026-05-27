# Prompt #10 — Sticky deduper-and-clusterer (three-pass)

> **From:** *The Synthesis Playbook*, prompt appendix, #10.
> **Recipe:** Ideation (Ch 7).
> **Used at:** Step 1 — [CLUSTER] in `synthesis-ideation/SKILL.md`.

## The prompt

```
Here are [N] stickies from a [duration] ideation session. They were
generated under [N] HMW prompts and grouped by the room during the
session.

Source data: [paste CSV: sticky text, HMW prompt, room-grouped cluster,
dot count].

Do this in three passes, showing me each before moving on:

Pass 1 — Dedupe. Identify near-duplicates (different words, same idea).
Merge each cluster of duplicates into a single "concept entry" with:
the cleanest one-line phrasing, a list of the source stickies it
absorbs (with their dot counts), and the total dot count summed across
the originals.

Pass 2 — Tighten. Rewrite each concept entry as a specific idea:
noun-verb-object. Vague entries get a concrete framing or get flagged
for human review. ("Better onboarding" gets rewritten as "Reduce the
onboarding flow from 11 steps to 6, removing the company-info-collection
step" — only if the underlying sticky supports the specificity.
Otherwise flag.)

Pass 3 — Re-cluster. Group the tightened entries into thematic clusters
across the [N] HMW prompts. Aim for 8–12 thematic clusters. Some entries
will move across HMWs — that's fine; flag those moves.

Constraints: do not invent specificity. If an entry is genuinely vague,
leave it vague and flag it. Do not merge contradictory entries — surface
them as a "tension" within a theme. Do not create a "miscellaneous" bucket.
```

## What to customize

- `[N]` (first) — total sticky count (e.g. `200`)
- `[duration]` — e.g. `half-day`, `one-day`
- `[N]` (second/third) — number of HMW prompts the session used (e.g. `six`)
- `[paste CSV]` — sticky export with at minimum: sticky text, which HMW prompt it was generated under, the room-assigned cluster, dot count

## What to expect

The first time you do this, you'll be surprised how much is duplicate. A half-day ideation session typically has 30–40% duplicates by content. The dedupe pass is the move that takes you from "a wall of stickies" to "a workable list."

200 stickies usually collapse into ~80 concept entries after dedupe, then ~25–35 distinct ideas after tightening, then ~8–12 thematic clusters.

## Common failures

- **Model invents specificity to make vague entries "tighter."** Re-prompt: "Do not invent specificity. If the underlying sticky is vague, leave it vague and flag it."
- **Model merges contradictory entries.** Two stickies that say opposing things get smoothed into one "synthesis." Re-prompt the tension-preservation constraint.
- **Miscellaneous bucket sneaks back in.** Some models smuggle it in as "uncategorized" or "other." Re-run with the constraint re-enforced.

## License

MIT. See `/LICENSE`.
