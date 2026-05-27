# Quick Start

Get from zero to your first synthesis in 3 steps.

## Step 1: Install

### Via Claude Code plugin marketplace (recommended, v0.1.0+)

```text
/plugin marketplace add bbulman/workshop-synthesizer
/plugin install workshop-synthesizer
```

### Via direct clone

```bash
git clone https://github.com/bbulman/workshop-synthesizer.git ~/workshop-synthesizer

cd /path/to/your/project
mkdir -p .claude/skills
ln -s ~/workshop-synthesizer/synthesis-framework .claude/skills/synthesis-framework
ln -s ~/workshop-synthesizer/synthesis-discovery .claude/skills/synthesis-discovery
ln -s ~/workshop-synthesizer/synthesis-offsite .claude/skills/synthesis-offsite
ln -s ~/workshop-synthesizer/synthesis-sprint .claude/skills/synthesis-sprint
ln -s ~/workshop-synthesizer/synthesis-ideation .claude/skills/synthesis-ideation
ln -s ~/workshop-synthesizer/synthesis-retro .claude/skills/synthesis-retro
ln -s ~/workshop-synthesizer/synthesis-training .claude/skills/synthesis-training
ln -s ~/workshop-synthesizer/synthesis-prompt-library .claude/skills/synthesis-prompt-library
```

Each skill must sit at `.claude/skills/<skill-name>/SKILL.md` for Claude Code to discover it.

### Without Claude Code (any LLM)

Browse [`prompts/`](./prompts/) and copy whichever prompt fits your workshop. The four-part prompt grammar at the bottom of [`prompts/README.md`](./prompts/README.md) explains how to adapt them. Works in any long-context LLM.

## Step 2: Launch

```bash
claude
```

Then try one of:

- `/ws-help` — index + decision tree (start here if unsure which recipe)
- `/ws-discovery` — synthesize a customer discovery sprint
- `/ws-offsite` — synthesize an executive offsite
- `/ws-sprint` — synthesize a design sprint (Friday user tests → Monday recommendation)
- `/ws-ideation` — synthesize a half-day ideation or roadmap workshop
- `/ws-retro` — synthesize a team retro or post-mortem
- `/ws-training` — synthesize a multi-day training or cohort program

## Step 3: First synthesis — Discovery, end-to-end

Walking through a Discovery synthesis with a sample test:

```bash
# Create a synthesis-ready file with the inputs the recipe needs.
# (Template at synthesis-framework/references/synthesis-ready-file.md)
cat > /tmp/test-engagement.md <<'EOF'
Synthesis pack — Test Discovery Sprint

Capture
- 3 short interview transcripts (paste below)
- Working hypothesis: "the onboarding flow is too long"

Reference
- Workshop goal: surface opportunity areas from 3 customer interviews
- Deliverable spec: deck + brief for product team, due Monday

[transcripts here]
EOF

# Then invoke the recipe
claude  # if not already running
```

Inside Claude Code: `/ws-discovery /tmp/test-engagement.md`

The plugin will:

1. Run the cluster pass (Prompt #1)
2. Run the anti-flattening critic (Prompt #2)
3. **Pause and ask you to write interpretations by hand** ← human-authorship checkpoint
4. Run the stress-test against your interpretations
5. Run the opportunity-area framer
6. **Pause and ask you to pick the shortlist by hand** ← human-authorship checkpoint
7. Draft the deck + brief
8. Save outputs to a workspace folder

Expected output: a structured opportunity-areas readout with the call slide left empty (you write that yourself — see [`synthesis-framework/references/human-authored-machine-assisted.md`](synthesis-framework/references/human-authored-machine-assisted.md)).

## What this plugin is not

- **Not an autonomous synthesis writer.** The recipes are explicit about which moves require human authorship. The plugin enforces those pauses.
- **Not a replacement for the book.** *The Synthesis Playbook* teaches the framework. The plugin runs it.
- **Not lock-in to Claude Code.** The prompts in [`prompts/`](./prompts/) work in any long-context LLM. The plugin is the convenient runner.

## Next steps

- Read [README.md](README.md) for the full plugin overview
- Read [MODE_REGISTRY.md](MODE_REGISTRY.md) for the recipe-by-recipe mode list
- Read [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) for the pipeline view
- Read [POSITIONING.md](POSITIONING.md) for what the plugin is (and isn't)
- Read [NOTICE.md](NOTICE.md) for the Workshopr.io commercial-interest disclosure

## When you hit a snag

- A prompt produces hedged or sycophantic output → see the "When prompts go stale" section of [`prompts/README.md`](prompts/README.md)
- The pipeline agent refused to advance → that's by design at human-authorship checkpoints
- A recipe doesn't fit your workshop type → see [`synthesis-prompt-library/references/extending-the-recipes.md`](synthesis-prompt-library/references/extending-the-recipes.md) for the five-step pattern to build your own

## Source

The plugin's recipes and prompts are derived from *The Synthesis Playbook* by Bill Bulman (Workshopr facilitation series, Book 6). The book is the source of truth; the plugin runs it.
