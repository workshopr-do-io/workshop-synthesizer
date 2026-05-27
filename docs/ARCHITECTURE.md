# Architecture

How the Synthesis Playbook plugin is wired.

## The picture

```
synthesis-playbook/                    (the GitHub repo / installable plugin)
│
├── .claude-plugin/
│   └── plugin.json                    Plugin manifest — declares skills + metadata
│
├── README.md                          Public entry; install + decision tree
├── LICENSE                            MIT
├── CONTRIBUTING.md
├── SECURITY.md
├── CHANGELOG.md
├── .gitignore
│
├── skills/                            8 sub-skills, each its own folder
│   ├── synthesis-framework/           Foundation (Chs 1-3) — every other skill depends on this
│   ├── synthesis-discovery/           Ch 4 recipe + pipeline agent
│   ├── synthesis-offsite/             Ch 5 recipe + pipeline agent
│   ├── synthesis-sprint/              Ch 6 recipe + pipeline agent
│   ├── synthesis-ideation/            Ch 7 recipe + pipeline agent
│   ├── synthesis-retro/               Ch 8 recipe + pipeline agent
│   ├── synthesis-training/            Ch 9 recipe + pipeline agent
│   └── synthesis-prompt-library/      Ch 10 meta-skill (the twelve workhorses)
│
├── commands/                          7 slash commands
│   ├── synthesis-help.md              /ws-help — index + decision tree
│   ├── synthesis-discovery.md
│   ├── synthesis-offsite.md
│   ├── synthesis-sprint.md
│   ├── synthesis-ideation.md
│   ├── synthesis-retro.md
│   └── synthesis-training.md
│
├── prompts/                           26 prompts, organized by recipe
│   ├── README.md
│   ├── workhorses/                    10 most-reused + 2 disciplines
│   ├── discovery/                     7 prompts (#1–4, #24–26)
│   ├── offsite/                       3 prompts (#5–7)
│   ├── sprint/                        2 prompts (#8–9)
│   ├── ideation/                      5 prompts (#10–14)
│   ├── retro/                         5 prompts (#15–19)
│   └── training/                      4 prompts (#20–23)
│
└── docs/
    ├── architecture.md                This file
    ├── using-without-claude-code.md
    ├── publishing-checklist.md
    └── relationship-to-book.md
```

## How a slash command flows through the plugin

User invokes `/ws-discovery`.

```
1. Claude Code loads commands/ws-discovery.md
   ↓
2. The command file describes the recipe and references
   synthesis-discovery/SKILL.md
   ↓
3. SKILL.md describes the recipe in detail and references:
   - references/workflow.md (step-by-step)
   - references/prompts.md (which prompts at which steps)
   - references/pitfalls.md (5 ways the synthesis fails)
   - references/worked-example.md (the Mid-Co composite)
   - agents/discovery_pipeline_agent.md (the 8-step automated pipeline)
   ↓
4. Pipeline agent reads the synthesis-ready file and runs the recipe:
   - Steps 1-3, 5-6, 8 — automated (model runs prompts from prompts/discovery/)
   - Steps 4, 7 — paused for human authorship
   ↓
5. Output: a deck + brief in workspace/, plus interim artifacts
```

## How a skill references other skills

Skills depend on the framework skill. When `synthesis-discovery/SKILL.md` references `[CLUSTER]`, the bracket tag points back to `synthesis-framework/references/four-moves.md`.

The framework is the only skill that runs alone (or runs as a reference for others). The recipe skills always implicitly load the framework.

## How a skill references a prompt

Each recipe skill's `references/prompts.md` lists the prompts used at each step with paths to `prompts/<recipe>/<NN>-<name>.md` files. The prompts live in `prompts/` (one canonical location); the skills point to them by path.

When the pipeline agent needs to run a prompt, it reads the prompt file content from `prompts/<recipe>/<NN>-<name>.md` and uses it verbatim.

## Why this structure

Matches two existing precedents:

1. **`academic-research-skills`** — multi-skill plugin with `skills/`, `commands/`, and `.claude-plugin/plugin.json`. This plugin follows the same convention so users familiar with that pattern can navigate.
2. **Bill Bulman's `ebook-publishing` skill** — single-skill structure with `SKILL.md`, `references/`, README, LICENSE, CONTRIBUTING. The Synthesis Playbook plugin uses the same documentation hygiene at the repo level and inside each sub-skill.

The 26 prompts are organized by recipe (not by workhorse) so that copy-paste users can find what they need by workshop type. The 10 workhorse prompts are duplicated/linked in `prompts/workhorses/` for users who want the most-reused subset.

## What happens when a recipe variant is invoked

Some recipes have ADAPT sidebars (e.g., the Discovery recipe has CAB and Persona/JTBD variants). The pipeline agent for each recipe has conditional logic:

- The Discovery agent runs the base recipe by default
- If the user signals "this is a CAB synthesis," the agent adds the cross-session deduper step
- If the user signals "this is persona work," the agent swaps the cluster step for the archetype clusterer

The variants are documented in `references/<variant>.md` files (e.g., `synthesis-retro/references/post-mortem-variant.md`).

## Platform neutrality

The prompts in `prompts/` work in any long-context LLM. The plugin runs the workflow inside Claude Code. The book teaches the framework.

Three surfaces. Same recipes. No lock-in to any one platform.

This is by design — see `docs/using-without-claude-code.md` for the copy-paste path.

## Version compatibility

The plugin manifest declares `version: 0.1.0`. Future versions will follow semver:

- **Patch** (0.1.x) — prompt improvements, doc fixes, minor reference content additions
- **Minor** (0.x.0) — new recipes (e.g., a vendor-selection recipe), new variants, new pipeline agents, structural improvements
- **Major** (x.0.0) — structural changes that break existing workflows

See `CHANGELOG.md` for what's shipped.

## Source

This file is original to the plugin (not lifted from the book). The book's Chapter 11 ("A gentle on-ramp to agents") describes the agentic pipeline pattern that this plugin instantiates.
