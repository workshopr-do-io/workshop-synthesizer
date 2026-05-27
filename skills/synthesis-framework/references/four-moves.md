# The Four Moves

Every workshop synthesis you'll ever do is some arrangement of four moves. Learn them once and you stop relearning synthesis every Friday.

## [CLUSTER]

**The first move.** Group the raw pile into candidate themes.

You take what came out of the room — stickies, notes, quotes, sketches, votes, transcripts — and you collect them into piles that look like they belong together.

This is the part most facilitators dread, because it's the most mechanical and the part where the volume usually beats you. It's also where AI is genuinely useful in a way that nothing else in the synthesis stack is. A model can read 400 stickies in 20 seconds and group them into 8 candidate themes. A human cannot, on a Sunday afternoon, with any reliability.

**Two things to understand:**

- **The cluster is *candidate*, not final.** The model proposes; you dispose. A first-pass cluster is a draft of the themes, not the themes themselves.
- **The cluster is where AI flattens dissent.** Every clustering pass has a built-in pressure to round off the spiky stickies. The math is doing what the math does — minimizing distance to cluster centers, and spiky points increase that distance. The job is to catch it.

The good news is that catching the flattening is a prompting move. Always pair [CLUSTER] with an anti-flattening pass (prompt #2 in the appendix).

**Posture:** Hands-off. The model works. You're checking, not authoring.

## [INTERPRET]

**The second move.** Name what each cluster means.

A cluster is a pile. An interpretation is a sentence. The cluster says *these eighteen quotes are about onboarding.* The interpretation says *the onboarding flow is doing what it was designed to do; the problem is that what it was designed to do isn't what people need.*

The interpretation is the *so what*. The cluster is the *what*.

This is the move where most synthesis fails — not because people skip it, but because they outsource it to the model. The model's interpretations always read clean. That's exactly the problem. A clean interpretation that flattens the meaning is worse than a messy interpretation that holds it. The reader can tell the difference.

**The rule: AI clusters; the human decides.**

The model can draft an interpretation, stress-test an interpretation you wrote, argue against your interpretation as a steelman. The interpretation itself — the sentence in the deck — comes out of your head, in your voice, with your name on the consequences.

Two reasons:

- **You were in the room.** The model wasn't. The room had body language, tone, a glance between two people when the third one said the thing. Only you have access to it.
- **The client will ask you why.** They will not ask the model. If you can't answer without saying "the model suggested it," you handed in slop.

**Posture:** Hands-on. The model assists. You author.

## [PRIORITIZE]

**The third move.** Decide which interpretations matter most, and in what order.

Most workshop outputs have more themes than a deliverable can carry. A discovery sprint with 20 interviews might surface 12 interpretations. The deck has room for 4. Which 4?

This is the move where AI is least useful and most dangerous in the whole synthesis stack. Three reasons:

- **Prioritization is political.** *Which finding goes first* is a question about whose preferences get foregrounded. The model has no idea who is in the room next to you, or who has the budget, or who is the actual decider.
- **Prioritization is contextual.** The same finding that's top-three for one client is obvious-already for the next. The model doesn't know which company you're in.
- **Prioritization carries consequences.** The thing you put first is the thing the client commits to. If you put the wrong thing first because the model said so, you've burned credibility you'll spend a quarter earning back.

In nearly every recipe, [PRIORITIZE] is the move where you turn the model off and reach for the analog tools. A 2×2. A dot vote with yourself. A walk around the block. A phone call with one person from the room.

The model can frame trade-offs ("argue the case for putting A first; now argue B first"). That use is fine. **Asking it to rank for you is not.**

**Posture:** Hands-only. The model is closed or used sparingly as a sparring partner.

## [NARRATE]

**The fourth move.** Shape the whole into a story the client receives.

Synthesis is a sequence — beginning that earns attention, middle that walks through findings, end that hands them what to do. The narrate move is where you decide the sequence.

AI is helpful here in a specific way. It's a decent first-draft writer. Hand it your interpretations, your prioritization, and the audience, and it'll give you a workable outline. Hand it the outline plus your voice samples, and it'll draft passable prose. Hand it the prose and ask it to tighten, and it'll often tighten.

What it can't do:

- **The audience-specific part.** The board deck and the team write-up and the CEO memo carry the same findings, but each carries them in a different voice, at a different altitude, with different things in foreground and background. That sequencing is yours.
- **The callback.** The thing where the first scene and the last scene rhyme. The model doesn't know how to do this consistently. The best narratives come from humans who use the model for the middle and write the open and close themselves.

**Posture:** Co-writing. The model drafts. You shape.

## The bracket tags

You'll see `[CLUSTER]`, `[INTERPRET]`, `[PRIORITIZE]`, `[NARRATE]` as inline tags throughout the recipes. When you see a tag, it tells you which move you're inside, which tells you which posture to take.

- Inside `[CLUSTER]`, you're hands-off — model works, you check
- Inside `[INTERPRET]`, you're hands-on — model assists, you author
- Inside `[PRIORITIZE]`, you're hands-only — model closed or sparring
- Inside `[NARRATE]`, you're co-writing — model drafts, you shape

The tags break the drift that happens when synthesizers use the model as one undifferentiated tool — paste, click, paste, click. The synthesis flattens. The tags make the posture switch explicit.

## The move-mix chart

Every recipe weights the moves differently:

| Recipe | [CLUSTER] | [INTERPRET] | [PRIORITIZE] | [NARRATE] | Dominant move |
|---|---|---|---|---|---|
| Discovery | 30% | 40% | 10% | 20% | Interpret |
| Strategic offsite | 10% | 30% | 30% | 30% | Politics-heavy mix |
| Design sprint | 15% | 25% | 35% | 25% | Prioritize + narrate |
| Ideation & roadmap | 20% | 15% | 50% | 15% | Prioritize |
| Retro & post-mortem | 40% | 30% | 10% | 20% | Cluster (dissent-preserving) |
| Training debrief | 15% | 35% | 20% | 30% | Interpret + narrate |

The percentages are vibes, not measurements. Don't take a calculator to them. The point is that the recipes aren't six different things. They're four moves in different mixes.

## The principle

The four moves are connected by one principle that holds the whole stack together:

> **Human-authored, machine-assisted.**

See [`human-authored-machine-assisted.md`](human-authored-machine-assisted.md) for the full operationalization.

## Source

*The Synthesis Playbook*, Chapter 2 "The four moves."
