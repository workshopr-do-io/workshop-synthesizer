# The Prompts

Every prompt from the book's appendix, in copy-paste form. **You don't need this plugin — or Claude Code — to use them.** Paste them into ChatGPT, Claude.ai, Gemini, or whatever long-context model you trust. The plugin is the convenient runner; the prompts are the product.

## How the folder is organized

```
prompts/
├── workhorses/           # The 10 most-reused prompts + 2 disciplines
├── discovery/            # 7 prompts (Discovery recipe, Ch 4)
├── offsite/              # 3 prompts (Strategic Offsite recipe, Ch 5)
├── sprint/               # 2 prompts (Design Sprint recipe, Ch 6)
├── ideation/             # 5 prompts (Ideation/Roadmap recipe, Ch 7)
├── retro/                # 5 prompts (Retro/Post-mortem recipe, Ch 8)
└── training/             # 4 prompts (Training Debrief recipe, Ch 9)
```

Each file is numbered to match the book's appendix (e.g., `02-anti-flattening-critic.md` is prompt #2). Variables in `[brackets]` are placeholders — replace them with your engagement-specific content before pasting.

## The twelve workhorses

These are the prompts that show up across multiple recipes. If you only ever internalize twelve, internalize these. Two of them are disciplines, not prompts.

| # | Workhorse | Used in |
|---|---|---|
| 1 | Transcript-to-quotes extractor | Discovery, any interview-based work |
| 2 | First-pass clusterer | Discovery, Ideation, Retro |
| 3 | Anti-flattening critic | Discovery, Retro |
| 4 | Interpretation stress-test | Discovery, Sprint, Retro |
| 5 | Dissent-vs-noise distinguisher | Retro, any dissent-heavy synthesis |
| 6 | Criteria applicator | Ideation, Roadmap |
| 7 | Decision log structurer | Offsite |
| 8 | Argue-the-other-side critic | Offsite, Ideation |
| 9 | Cause-vs-blame check | Post-mortem |
| 10 | Sequencing critic | Roadmap |
| 11 | Audience-tiered narrator | Training, Offsite (a discipline, not a single prompt — see `workhorses/11-audience-tiered-narrator.md`) |
| 12 | The aloud test | Every recipe (a discipline, not a prompt — see `workhorses/12-aloud-test.md`) |

The 10 workhorses that are actual prompts have copies in `workhorses/` for convenience; their primary files live in the recipe folders.

## The four-part prompt grammar

Every prompt in this folder follows the same four-part structure. If you want to write your own prompts for workshop types not covered here, follow the grammar.

1. **Role and stakes.** What kind of work is the model doing?
   *Example: "You're helping me synthesize fourteen customer discovery interviews for a B2B SaaS client."*

2. **Input and constraints.** What are you giving the model, and what counts as valid output?
   *Example: "I'll paste fourteen transcripts below. Preserve exact wording on quoted material. Don't clean up filler words."*

3. **Process.** How should the model work?
   *Example: "Do this in three passes, showing me each pass before moving on."*

4. **Anti-patterns.** What should the model not do?
   *Example: "Do not flatten contrarian quotes into majority themes. Do not invent quotes. Do not create a 'miscellaneous' bucket."*

If a prompt is missing any of the four parts, it's undercooked. Add the missing part and run again.

## The aloud test (not a prompt, a discipline)

Read the model's output aloud before you trust it. The whole thing. If you stumble on a sentence, rewrite it. If a paragraph feels rehearsed, rewrite. If a slide bores you, the client will skip it.

The aloud test is the single best detector of generic, AI-flavored, slightly-off prose. Use it on every artifact before you ship.

## When prompts go stale

The prompts in this folder were tested against Claude 4.x and ChatGPT-5-class models as of May 2026. Models change. A prompt that worked clean last quarter can start producing hedged, verbose, or sycophantic output six months later.

If a prompt stops working:

1. Read the four-part grammar above. Which part is the model now violating?
2. Tighten the anti-patterns section (it's usually that one).
3. Test against a known-good model to isolate whether it's the prompt or the model that drifted.
4. Open an issue on the repo and tell me what failed.

## License

MIT. See [`/LICENSE`](../LICENSE). Copy, adapt, steal. If you build a version that works better than mine, I want to see it.

---

*"The prompts are the product." — from the book*
