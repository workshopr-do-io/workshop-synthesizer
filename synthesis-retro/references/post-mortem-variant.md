# Post-Mortem Variant — Retro Recipe + Timeline + Cause-vs-Blame

A post-mortem is a retro for incidents, failed projects, or major misses. The recipe is mostly the same. Three differences.

## 1. Two readings, not one

A post-mortem has to be **factually clean** (a precise sequence of what happened) **and emotionally honest** (a real account of how it landed, what people felt, what's lost). The retro synthesis emphasizes the second. The post-mortem synthesis needs both, in balance.

## 2. The timeline matters

Post-mortems usually include a timeline. The timeline is the part the model can help with most — building a clean chronological narrative from logs, chat messages, and notes.

**Critical constraint: do not impose retrospective clarity.**

If a decision was made under uncertainty, the timeline entry says **what they knew at the time**, not what we know now. If two people remember a decision differently, surface the discrepancy rather than reconciling it. If logs and recollections conflict, flag the conflict.

Run **Prompt #18 (Post-mortem timeline structurer)** — see [`/prompts/retro/18-post-mortem-timeline-structurer.md`](../../prompts/retro/18-post-mortem-timeline-structurer.md).

The timeline produced by this prompt should look **messier than a typical post-mortem timeline.** That mess is honest. Cleaning it up is the failure to avoid.

## 3. The blame-vs-cause distinction

Post-mortems have to name the **cause without naming the blame.**

A junior engineer pushed the wrong config. The **cause** is the missing safety check on the deploy script. The **blame** is on the engineer. The post-mortem names the cause. It does not name the blame.

If you find yourself writing a sentence that puts a person at the center of the cause description, rewrite to put the system at the center.

Run **Prompt #19 (Cause-vs-blame check)** — see [`/prompts/retro/19-cause-vs-blame-check.md`](../../prompts/retro/19-cause-vs-blame-check.md).

Read each model rewrite carefully. The model will sometimes produce defensive rewrites that lose the meaning. **The goal is not to dodge accountability; it's to put accountability where it can do the most good, which is on the system, not on the person who tripped over the system.**

## Where to insert the post-mortem steps

Into the standard retro workflow:

1. Structure and cluster (Step 1 of retro)
2. **NEW: Post-mortem timeline structurer (Step 1.5)** — see Prompt #18
3. Distinguish noise from real dissent (Step 2 of retro)
4. Interpret linked themes (Step 3 of retro)
5. **NEW: Cause-vs-blame check (Step 3.5)** — see Prompt #19
6. Action items (Step 4 of retro)
7. Public write-up (Step 5 of retro)
8. One-page summary (Step 6, optional)
9. Pre-send check (Step 7 of retro)

## The pitfall that matters most for post-mortems

AI-generated timelines that read crisp but lose the messy-but-true sequence of decisions under pressure.

**Fix:** Hold the line on the "do not impose retrospective clarity" constraint. If the model produces a timeline that reads clean, re-run with the constraint reinforced explicitly.

## Worked example seed

A project failed for technical reasons stated (the database migration didn't scale). The post-mortem could have stopped there.

The synthesis, after a careful read of the timeline, surfaced that the team had had a clear early warning from a customer success report in week three of the project — and had decided not to escalate it because the project was already in motion.

The synthesis named both: the technical cause AND the earlier missed escalation signal. The team's response was to add a "did anyone see this before?" question to their standard post-mortem template, which surfaced two near-misses in the following quarter.

That's a post-mortem synthesis doing work no retro synthesis could have done.

## What's the same as the base retro

- Dissent preservation. Minority view is the data.
- Pre-send check to two voices from the room.
- Action items: 3–7, named, dated, tied to themes.
- Read the public write-up aloud.

## Source

*The Synthesis Playbook*, Chapter 8 "Retro & post-mortem synthesis," Post-mortem ADAPT sidebar.
