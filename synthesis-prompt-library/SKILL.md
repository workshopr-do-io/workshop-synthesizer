---
name: synthesis-prompt-library
description: >
  The twelve workhorses — the reusable prompts that show up across multiple
  recipes — plus the four-part prompt grammar for building new prompts the
  book doesn't cover, plus the aloud test discipline, plus versioning and
  shrinkage rules. Use when the user wants to understand the meta-structure
  of the recipes' prompts, build a new prompt for a workshop type not
  covered by the recipes, or set up a personal prompt library. Triggers on:
  "twelve workhorses", "prompt grammar", "four-part grammar", "aloud test",
  "prompt versioning", "build my own prompt", "prompt library", "extend
  the recipes".
---

# The Prompt Library

The meta-skill. Read this when you want to understand why the recipes' prompts work, or when you need to build a new prompt for a workshop type the book doesn't cover.

## The twelve workhorses

Across the six recipes there are 26 named prompts. Twelve of them — the workhorses — show up across multiple recipes. If you only ever internalize twelve, internalize these.

| # | Workhorse | Used in |
|---|---|---|
| 1 | Transcript-to-quotes extractor | Discovery; any interview-based work |
| 2 | First-pass clusterer | Discovery, Ideation, Retro |
| 3 | Anti-flattening critic | Discovery, Retro |
| 4 | Interpretation stress-test | Discovery, Sprint, Retro |
| 5 | Dissent-vs-noise distinguisher | Retro; any dissent-heavy synthesis |
| 6 | Criteria applicator | Ideation, Roadmap |
| 7 | Decision log structurer | Offsite |
| 8 | Argue-the-other-side critic | Offsite, Ideation |
| 9 | Cause-vs-blame check | Post-mortem |
| 10 | Sequencing critic | Roadmap |
| 11 | Audience-tiered narrator | Training, Offsite (discipline, see below) |
| 12 | The aloud test | Every recipe (discipline, see below) |

Full text of the 10 actual prompts: [`references/twelve-workhorses.md`](references/twelve-workhorses.md). Disciplines #11 and #12 are explained in dedicated reference files.

## The four-part prompt grammar

Every prompt in this plugin follows the same four-part structure. If you can write a prompt that follows the grammar, you can build new prompts that work as well as the ones in the recipes.

1. **Role and stakes.** What kind of work the model is doing.
   *Example: "You're helping me synthesize fourteen customer discovery interviews for a B2B SaaS client."*

2. **Input and constraints.** What you're giving the model and what counts as valid output.
   *Example: "I'll paste fourteen transcripts below. Preserve exact wording on quoted material. Don't clean up filler words."*

3. **Process.** How to work — usually multi-pass with show-me-each-pass discipline.
   *Example: "Do this in three passes, showing me each pass before moving on."*

4. **Anti-patterns.** What not to do.
   *Example: "Do not flatten contrarian quotes into majority themes. Do not invent quotes. Do not create a 'miscellaneous' bucket."*

If a prompt is missing any of the four parts, it's undercooked. Add the missing part and run again.

Full grammar with examples: [`references/four-part-prompt-grammar.md`](references/four-part-prompt-grammar.md).

## The aloud test (not a prompt, a discipline)

Read the deliverable aloud. The whole thing. If you stumble on a sentence, rewrite it. If a slide bores you, the client will skip it. If a paragraph would let someone off the hook for something the room addressed, rewrite. If a paragraph would land hard in a way the room didn't intend, rewrite.

The aloud test is the bracket on the whole synthesis. It's the single best detector of generic, AI-flavored, slightly-off prose. Use it on every artifact before ship.

Full discipline: [`references/aloud-test.md`](references/aloud-test.md).

## Building a recipe the book doesn't cover

Five-step pattern. Use this when you need a recipe for a workshop type that's not one of the six.

1. **Name the move mix.** Cluster/Interpret/Prioritize/Narrate as percentages. If you can't write the mix as one line, you don't yet understand the recipe well enough.
2. **Name the audience and altitude.** Who reads the synthesis? At what altitude? One audience or several?
3. **Reach for the roll.** Which of the twelve workhorses apply? Most recipes use 4–7 of them.
4. **Identify recipe-specific moves.** What does this workshop type need that the roll doesn't cover? Usually 1–2 specialized prompts. Build them with the four-part grammar.
5. **Worked-example test.** Run the recipe on one real engagement before you call it done.

Full extension pattern: [`references/extending-the-recipes.md`](references/extending-the-recipes.md).

## Versioning prompts

A small discipline that pays back fast. Every prompt in your library has a version. Not semver — just a date and a one-line note.

```
# Anti-flattening critic
v3 / 2026-03-22 — added "minority view" framing explicitly; v2 was
producing technically correct but politically tone-deaf outputs.
```

Full versioning discipline (plus the shrinkage rule, the test-card discipline, and when to retire a prompt): [`references/versioning-discipline.md`](references/versioning-discipline.md).

## Reference files

| File | Load when... |
|---|---|
| [`references/twelve-workhorses.md`](references/twelve-workhorses.md) | Want the 10 workhorse prompts in one place, with cross-references to where they're used |
| [`references/four-part-prompt-grammar.md`](references/four-part-prompt-grammar.md) | Building a new prompt; debugging a prompt that stopped working |
| [`references/aloud-test.md`](references/aloud-test.md) | About to ship a deliverable; want to catch AI-flavored prose |
| [`references/extending-the-recipes.md`](references/extending-the-recipes.md) | Building a new recipe for a workshop type the book doesn't cover |
| [`references/versioning-discipline.md`](references/versioning-discipline.md) | Setting up or pruning a personal prompt library |
| [`references/audience-tiered-narrator.md`](references/audience-tiered-narrator.md) | Drafting the same content at three altitudes (personal / operational / executive / board) |

## How this skill is used

`synthesis-prompt-library` rarely runs as a slash command. It's the meta-skill the other recipes reach into. When a recipe says "use the four-part grammar to adjust this prompt," the recipe is pointing back here.

It also runs when you're explicitly building something new — a new prompt for a custom workshop, a new recipe for a workshop type, a personal prompt library on your own machine.

## The bottom line

Twelve tools is enough. The book covers six recipes; the recipes use those twelve tools in different mixes. Build new recipes by reaching for the same twelve, plus one or two recipe-specific specialists. Don't grow the roll beyond twelve unless you've earned it.

The quarterly prune is what makes the library a library and not a hoarder's drawer. Most prompt libraries grow forever. Yours should breathe — same size or smaller, almost never bigger.

## Source

*The Synthesis Playbook*, Chapter 10 "Your reusable prompt library." Plus the appendix's "Four-part prompt grammar" section and "The discipline that isn't a prompt" (aloud test).
