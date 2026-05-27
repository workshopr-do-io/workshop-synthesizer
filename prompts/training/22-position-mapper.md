# Prompt #22 — Position-mapper across functions

> **From:** *The Synthesis Playbook*, prompt appendix, #22.
> **Recipe:** Training debrief (Ch 9) — Cross-functional alignment ADAPT sidebar.
> **Used at:** Replaces Step 2 in the training recipe when running a cross-functional alignment workshop.

## The prompt

```
Here are the discussion notes and decision artifacts from a
cross-functional alignment session: [paste]. The functions in the
room were [product, engineering, GTM, etc.].

For each function, identify:

1. Starting position — what did this function appear to want walking
   into the session?
2. Closing position — what did this function commit to at the end?
3. Distance traveled — how much movement, and on what?
4. Parked disagreements — what did this function not agree to that
   others wanted them to?

Surface any place where two functions ended in genuine disagreement
that the room papered over. Don't flatten this — name it explicitly.
```

## What to customize

- `[paste]` — discussion notes and decision artifacts from the cross-functional session
- `[product, engineering, GTM, etc.]` — the actual functions in the room

## Why position-mapping is the cross-functional recipe's spine

Cross-functional rooms are political bodies. Each function walks in with a position. The synthesis isn't "what was decided"; it's "where did each function move, and where did they not."

The parked disagreements are the most important part. Cross-functional sessions routinely end with disagreements *papered over* — everyone nods, nobody dissents, nothing's resolved. Six weeks later it surfaces as friction in execution. The synthesis names the parked disagreement so it can be addressed before it surfaces.

## Pair with prompt #23

After position-mapping, run [prompt #23 (real-disagreement surfacer)](23-real-disagreement-surfacer.md) to surface where the stated disagreements aren't actually the real disagreements.

## Common failures

- **Model flattens parked disagreements.** Re-prompt: "Name parked disagreements explicitly. If two functions ended without agreement, say so by name."
- **Model assumes everyone agreed.** Cross-functional rooms often *appear* to agree because nobody contradicts. Re-prompt: "Look for what each function did NOT commit to."
- **Model invents function positions.** If your notes don't show a function's starting position, the model sometimes guesses. Re-prompt: "If a function's starting position is not in the notes, say 'unknown — needs verification' rather than inferring."

## License

MIT. See `/LICENSE`.
