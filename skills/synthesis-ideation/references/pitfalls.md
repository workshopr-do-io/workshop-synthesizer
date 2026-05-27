# Ideation & Roadmap Recipe — Pitfalls

Five ways an ideation synthesis fails.

## 1. Dedupe pass merging ideas that look similar but aren't

**Symptom:** Two stickies say "improve search." One is about ranking; one is about filtering. The model merges into "improve search." The synthesis loses the distinction.

**Fix:** In the dedupe pass, instruct the model to surface "near-merges" — ideas that look similar but might be distinct. Review by hand.

## 2. Criteria drift across the shortlist

**Symptom:** You score the first ten ideas honestly. By idea 25, you're tired and scoring generously. The bottom of the shortlist is softer than the top.

**Fix:** Score in batches of five. Take a five-minute break between batches. Or have the model do the first pass and you verify rather than scoring from scratch.

## 3. Killing the weird outlier because it doesn't fit the criteria

**Symptom:** The criteria are conservative by design — feasibility, near-term impact, known evidence. The weird outlier scores Low across the board because it's a different kind of bet. The synthesis kills it. The room loses the thing they generated this session that wasn't on their roadmap before.

**Fix:** Every shortlist has at least one weird outlier. The criteria do not get to veto it. See [`weird-outlier-rule.md`](weird-outlier-rule.md).

## 4. Ranking that smuggles in the loudest voter's preferences

**Symptom:** The CPO leaned forward on idea X during the room. You can't help thinking about it. Idea X moves up the list without the criteria justifying it.

**Fix:** The dots-vs-criteria tension surfacer prompt forces you to name when you're including a hot-but-weak idea because of room signal rather than scoring. **Honesty disclosed is defensible. Honesty hidden is suspect.**

## 5. A shortlist with no next-step variation

**Symptom:** Twelve ideas, all marked "prototype." The team can't prototype twelve things.

**Fix:** Budget the next steps. At most three or four prototypes, three or four research items, one or two commits, the rest monitor.

## Roadmap-specific pitfall

**A roadmap that ranks well but doesn't sequence well.** The Now bucket fills with the top-rated items, regardless of whether they can start. Three months later, two of the Now items are blocked. The roadmap looks broken even though the ranking was correct.

**Fix:** Never publish a roadmap without running the sequencing critic (Prompt #14). See [`roadmap-variant.md`](roadmap-variant.md).

## Source

*The Synthesis Playbook*, Chapter 7 "Ideation & roadmap synthesis," pitfalls section.
