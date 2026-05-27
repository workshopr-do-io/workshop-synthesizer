# The Twelve Workhorses

The reusable prompts that show up across multiple recipes. If you only ever internalize twelve, internalize these.

## What "workhorse" means

A workhorse is a prompt (or discipline) that gets used in more than one recipe. The book calls them "the twelve tools in the roll" after a cabinet-restoration metaphor — a tradesperson with 12 tools who has tried bigger rolls but keeps coming back to the same 12.

Of the twelve, **ten are actual prompts** and **two are disciplines** (instructions you follow, not text you paste into a model).

## The list

| # | Workhorse | Where it lives (primary file) | Used in |
|---|---|---|---|
| 1 | Transcript-to-quotes extractor | [`/prompts/discovery/01-transcript-to-quotes-and-cluster.md`](../discovery/01-transcript-to-quotes-and-cluster.md) | Discovery; any interview-based work |
| 2 | First-pass clusterer | (same file as #1 — the prompt does both in one pass) | Discovery, Ideation, Retro |
| 3 | Anti-flattening critic | [`/prompts/discovery/02-anti-flattening-critic.md`](../discovery/02-anti-flattening-critic.md) | Discovery, Retro |
| 4 | Interpretation stress-test | [`/prompts/discovery/03-interpretation-stress-test.md`](../discovery/03-interpretation-stress-test.md) | Discovery, Sprint, Retro |
| 5 | Dissent-vs-noise distinguisher | [`/prompts/retro/16-dissent-vs-noise-distinguisher.md`](../retro/16-dissent-vs-noise-distinguisher.md) | Retro; any dissent-heavy synthesis |
| 6 | Criteria applicator | [`/prompts/ideation/11-criteria-applicator.md`](../ideation/11-criteria-applicator.md) | Ideation, Roadmap |
| 7 | Decision log structurer | [`/prompts/offsite/05-decision-log-structurer.md`](../offsite/05-decision-log-structurer.md) | Offsite |
| 8 | Argue-the-other-side critic | [`/prompts/offsite/06-argue-the-other-side-critic.md`](../offsite/06-argue-the-other-side-critic.md) | Offsite, Ideation |
| 9 | Cause-vs-blame check | [`/prompts/retro/19-cause-vs-blame-check.md`](../retro/19-cause-vs-blame-check.md) | Post-mortem |
| 10 | Sequencing critic | [`/prompts/ideation/14-sequencing-critic.md`](../ideation/14-sequencing-critic.md) | Roadmap |
| 11 | **Audience-tiered narrator** (discipline) | [`audience-tiered-narrator.md`](audience-tiered-narrator.md) | Training, Offsite |
| 12 | **The aloud test** (discipline) | [`aloud-test.md`](aloud-test.md) | Every recipe |

Each prompt file (numbered 1–10) contains the prompt verbatim from the book's appendix, the variables to customize, and known failure modes.

## Why two of the twelve are disciplines

The audience-tiered narrator and the aloud test are not single prompts you paste. They are working practices that survive across recipes and model versions.

- **Audience-tiered narrator** — drafting the same content at multiple altitudes for different readers (personal, operational, executive, board). Multiple prompts implement it; the discipline is the same. See [`audience-tiered-narrator.md`](audience-tiered-narrator.md).
- **The aloud test** — reading the deliverable aloud before shipping. No prompt, no model. The single best detector of generic AI-flavored prose in the book. See [`aloud-test.md`](aloud-test.md).

## How the twelve compound

Once you've internalized the twelve, you can build new recipes for workshop types this plugin doesn't cover. The book's Chapter 10 walks the pattern:

1. Name the move mix (cluster/interpret/prioritize/narrate as percentages)
2. Name the audience and altitude
3. Reach for the roll — which of the twelve apply? Most recipes use 4–7 of them.
4. Identify recipe-specific moves — usually 1–2 specialized prompts. Build them with the four-part grammar (see [`/skills/synthesis-prompt-library/`](../../skills/synthesis-prompt-library/)).
5. Worked-example test before you call the recipe done.

## When prompts go stale

The prompts here were tested against Claude 4.x and ChatGPT-5-class models as of May 2026. Models change. A prompt that worked clean last quarter can start producing hedged, verbose, or sycophantic output six months later.

When a prompt stops working: tighten the anti-patterns section (it's usually that one); test against a known-good model to isolate whether it's the prompt or the model that drifted; open an issue.

## Source

*The Synthesis Playbook*, Chapter 10 "Your reusable prompt library."
