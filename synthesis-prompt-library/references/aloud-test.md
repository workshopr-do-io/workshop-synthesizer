# The Aloud Test (Reference)

See [`/prompts/workhorses/aloud-test.md`](../../prompts/workhorses/aloud-test.md) for the full discipline.

## Quick summary

Read the deliverable aloud. The whole thing.

- If you stumble on a sentence, rewrite it.
- If a slide bores you, the client will skip it.
- If a paragraph would let someone off the hook for something the room addressed, rewrite.
- If a paragraph would land hard in a way the room didn't intend, rewrite.

## Why this lives in the prompt-library skill

The aloud test is not a prompt. It's not text you paste into a model. It's a working practice — the single best detector of AI-flavored, slightly-off prose. The book is explicit:

> *The aloud test is the bracket on the whole synthesis. It's the single best detector of generic, AI-flavored, slightly-off prose. Use it on every artifact before publish.*

Because it lives across every recipe (not inside any one), it belongs in the meta-skill (`synthesis-prompt-library`) and in the workhorses folder.

## When the aloud test catches something

You'll stumble most often on:

- The opening line
- The call slide
- Any sentence you wrote tired
- Any paragraph the model drafted

Mark each stumble. Rewrite, then read again from that paragraph. Continue until you can read the whole artifact without stumbling.

## The retelling test (paired discipline)

For artifacts that will be re-told without you in the room — board decks, budget-defender one-pagers, cohort analyses going up to the VP — pair the aloud test with the retelling test:

Imagine someone you haven't met re-telling the synthesis. Does it survive?

- *73.4% of participants* doesn't survive a retelling. *Three of four participants* does.
- *Strategic alignment* sounds hollow when re-told. *We're shifting from A to B* doesn't.

If the retelling fails, edit.

## Source

*The Synthesis Playbook*, the prompt appendix ("The discipline that isn't a prompt") and Chapter 12 (the retelling test).
