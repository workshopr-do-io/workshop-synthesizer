# Prompt #13 — Kill list reasoner

> **From:** *The Synthesis Playbook*, prompt appendix, #13.
> **Recipe:** Ideation (Ch 7).
> **Used at:** Step 5 — [PRIORITIZE → NARRATE] in `skills/synthesis-ideation/SKILL.md`.

## The prompt

```
Here are the ideas that did not make the shortlist: [paste with
criteria scores and dot counts].

For each idea, name the single primary reason it was cut. Use these
categories where possible:

- Already in flight — the team is already doing this or something close.
- Too dependent — requires a prerequisite the team isn't going to
  build first.
- Low signal — the underlying problem isn't supported by enough evidence.
- Out of scope — interesting, but for a different team or different
  time horizon.
- Mergeable — the idea is absorbed into a shortlist item; name which one.
- Speculative — could be interesting but the criteria don't support it
  yet; revisit next quarter.
- Politically hard — would require organizational change the company
  isn't ready for.

One category per idea. One-line reason.
```

## What to customize

- `[paste]` — the list of ideas you decided not to include in the shortlist, with their criteria scores and dot counts attached

## Why the kill list matters

The kill list is what makes the shortlist defensible. The client will ask about the ones you cut. "They didn't make the top tier because [specific reason]" is a strong answer. "I forgot" is not.

The kill list is the second deliverable of the ideation recipe — not decoration. It tells the team where their backlog is bunched up:

- *Twenty ideas in "low signal"* → the room generated more speculation than evidence
- *Eight in "mergeable"* → the room generated convergent ideas, a healthy sign
- *Three in "politically hard"* → flags a structural conversation the room skated past

## What to do with the output

Review by hand. The model will sometimes miscategorize, especially the "politically hard" cases — which it can't see directly. Override by hand where you know better.

The categorized kill list goes into the long-form deliverable, organized by category.

## Common failures

- **Model defaults to "Speculative" for anything uncertain.** Re-prompt to use a specific reason — speculative is the residual bucket, not the default.
- **Model misses "Mergeable" cases.** If two cut ideas should fold into one shortlist item, the model sometimes misses the merge. Spot-check by hand.
- **"Politically hard" gets sanitized.** The model is reluctant to call this out. Override; if the room skated past a structural issue, name it in the kill list — that's where it'll get noticed without becoming a confrontation.

## License

MIT. See `/LICENSE`.
