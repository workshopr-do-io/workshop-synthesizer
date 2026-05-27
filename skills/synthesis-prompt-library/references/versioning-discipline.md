# Versioning Discipline — Prompts, Tests, and Shrinkage

A small discipline that pays back fast. Don't skip it.

## Why version

Prompts that get worse over time exist. The model you used in November isn't the same as the model you use in March. A prompt that produced beautiful clustering in November can produce verbose hedging in March.

When that happens, you want to roll back, see what changed, rewrite.

## How to version

Every prompt in your library has a version. Not semver — just a date and a one-line note.

```markdown
# Anti-flattening critic
v3 / 2026-03-22 — added "minority view" framing explicitly; previous
version (v2) was producing technically correct but politically
tone-deaf outputs.

## Prompt
[the prompt itself]

## Notes
[what it does well, what it does poorly, what models it's been tested on]

## History
- v3 / 2026-03-22 — current
- v2 / 2026-01-14 — added the "expert-vs-noise" framing
- v1 / 2025-11-04 — initial version, worked but produced too much hedging
```

The history matters because when a colleague asks for "your discovery prompt," you can hand them v3 plus the version history. They can see what you've already tried and avoid repeating the experiments that didn't work.

## Test cards — testing a new prompt

For every new prompt, write a "test card" with three inputs:

1. **A clean input** where you know what the right output looks like
2. **A messy input** that has the noise you'd see in the wild
3. **An adversarial input** designed to make the prompt fail

Run the prompt on all three. Save the outputs. Read them.

- If the prompt produces something useful on all three, it's library-ready.
- If it fails on the messy or adversarial input, you have specific work — usually a constraint to add in the anti-patterns section.

The test cards live in the library alongside the prompts they tested. When you update a prompt to v4, you re-run the test cards. If v4 fails on a test card v3 passed, you've regressed.

## The shrinkage rule

This is the discipline that makes the library a library and not a hoarder's drawer.

**Every quarter, look at the library and prune.**

For each prompt:

- **In the workhorses folder:** have I used this in the last quarter? If yes, keep. If no, ask why. Sometimes you didn't have a relevant engagement; that's fine. Sometimes the prompt has been quietly superseded by a better version; move the old one to `retired/`.
- **In recipe folders:** did the recipe ship as-is, or did I have to deviate? If I deviated, capture the deviation in the recipe or write a new variant.
- **In a "new prompts" folder:** it's been here for three months. Did it earn a promotion to workhorses or recipe? If not, retire it. New prompts that linger past a quarter are usually dead.
- **In a "retired" folder:** is there a successor in the active folders? If not, the lesson hasn't been learned yet. Write the successor or remove the retired entry.

The quarterly prune takes about 90 minutes. The library either stays the same size or gets smaller. Almost never bigger.

## A working folder structure

For your personal library (separate from this plugin):

```
synthesis-library/
├── README.md                 # the index — what's here and how to find it
├── 00-the-roll/              # the twelve workhorses with the grammar visible
│   ├── 01_transcript-to-quotes.md
│   ├── 02_first-pass-cluster.md
│   ├── ...
├── recipes/                  # workshop-type recipes
│   ├── discovery.md
│   ├── offsite.md
│   ├── sprint.md
│   ├── ...
├── new-prompts/              # prompts I'm testing
│   ├── 2026-04-12_vendor-selection.md
│   └── 2026-04-19_postmortem-timeline.md
└── retired/                  # prompts that didn't work, with notes on why
    └── 2025-11-04_executive-tone.md
```

Five folders. The most important is `retired/` — most prompt libraries have no retired folder, which means they keep accumulating prompts whether or not they work. The retired folder is the shrinkage discipline. When a prompt stops working, you don't delete it. You move it to retired, add a note on why, and write a successor.

## Working with collaborators

A library that's only yours is half a library.

A few rules learned the hard way:

- **Share the index, not the whole library.** Most collaborators don't want all twelve prompts; they want the one prompt for the specific problem. Send the README index link.
- **Annotate the customization burden.** Each prompt has things you customize per engagement (names, hypotheses, criteria, context) and things you don't. Mark the customization clearly with `[brackets]`.
- **Version what they send back.** When a collaborator improves a prompt, version it explicitly. *v4 / 2026-04-12 / Bill — sharpened the dissent-vs-noise distinction.* *v5 / 2026-05-08 / Maya — added an additional category for context-bound dissent.*
- **Resist the urge to consolidate.** Two facilitators using slightly different prompts is fine. Forcing convergence loses information.

## When the library is overkill

If you run two workshops a year, you don't need a library. You need a folder of notes and a willingness to write the prompt fresh each time.

Roughly: if you do more than one major synthesis a month, the library pays back. If you do one a quarter, the library is overhead.

The break-even is honest. Don't build the library before the workload justifies it.

## Source

*The Synthesis Playbook*, Chapter 10 "Your reusable prompt library."
