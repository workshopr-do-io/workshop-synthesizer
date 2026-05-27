# Extending the Recipes — Building New Recipes for Workshops This Plugin Doesn't Cover

The book covers six workshop types. There are more — Customer Advisory Boards (one quarter or four), vendor selections, hiring loops, board meetings, executive-coaching debriefs, sales-pipeline reviews, town halls. All candidates.

When you need a recipe the book doesn't cover, use this five-step pattern.

## The five-step pattern

### Step 1 — Name the move mix

What percentage of the work is **cluster, interpret, prioritize, narrate**?

If you can't write the move mix as a one-liner, you don't yet understand the recipe well enough to build it. For comparison, the six built-in recipes:

| Recipe | [CLUSTER] | [INTERPRET] | [PRIORITIZE] | [NARRATE] |
|---|---|---|---|---|
| Discovery | 30% | 40% | 10% | 20% |
| Strategic offsite | 10% | 30% | 30% | 30% |
| Design sprint | 15% | 25% | 35% | 25% |
| Ideation & roadmap | 20% | 15% | 50% | 15% |
| Retro & post-mortem | 40% | 30% | 10% | 20% |
| Training debrief | 15% | 35% | 20% | 30% |

If your new recipe is similar to one of these, copy that recipe's mix and adjust. If it's genuinely new, start from scratch.

### Step 2 — Name the audience and altitude

Who reads the synthesis? At what altitude?

Is it one audience (e.g., a CPO) or several at different altitudes (e.g., participants + program owner + budget-holder, like the training debrief)?

Tiered deliverables require the audience-tiered narrator discipline. See [`/prompts/workhorses/audience-tiered-narrator.md`](../../../prompts/workhorses/audience-tiered-narrator.md).

### Step 3 — Reach for the roll

Which of the twelve workhorses apply?

Most recipes use 4–7 of the workhorses. For example:

- **Vendor selection workshop:** criteria applicator (#6), argue-the-other-side critic (#8), audience-tiered narrator (#11), aloud test (#12) — plus one or two recipe-specific
- **Hiring loop synthesis:** dissent-vs-noise distinguisher (#5), decision log structurer (#7), cause-vs-blame check (#9 — for hiring misfires)
- **Quarterly business review (QBR) synthesis:** criteria applicator (#6), audience-tiered narrator (#11), sequencing critic (#10 if forward-looking)

See [`twelve-workhorses.md`](twelve-workhorses.md) for the full roll.

### Step 4 — Identify recipe-specific moves

What does this workshop type need that the roll doesn't cover? Usually one or two specialized prompts. Build them with the four-part grammar.

See [`four-part-prompt-grammar.md`](four-part-prompt-grammar.md) for the grammar plus a worked vendor-selection example.

### Step 5 — Worked-example test

Before you call the recipe done, run it on one real engagement (or one synthetic engagement with realistic data).

Where did it stall? Where did it produce slop? Iterate.

The recipes in the book were built this way. R1 (Discovery) was first; it took six months of real engagements before the prompts stabilized. R2 (Strategic offsite) took six weeks because R1 had done most of the grammar work. R6 (Training debrief) was muscle memory by then.

## When NOT to build a new recipe

If you run the workshop type once a year, you don't need a recipe. You need a folder of notes and a willingness to write the prompt fresh each time.

Roughly: **if you do more than one major synthesis a month, the library pays back. If you do one a quarter, the library is overhead.**

The break-even is honest. Don't build the recipe before the workload justifies it.

## Sharing recipes back

If you build a recipe that works well, the plugin welcomes contributions:

1. Open an issue first with the workshop type, the move mix, and the proposed prompts
2. Once scoped, follow the structure of `skills/synthesis-discovery/` as your template
3. Submit a PR with the new skill folder

See [`/CONTRIBUTING.md`](../../../CONTRIBUTING.md) for the contribution process.

## Source

*The Synthesis Playbook*, Chapter 10 "Your reusable prompt library."
