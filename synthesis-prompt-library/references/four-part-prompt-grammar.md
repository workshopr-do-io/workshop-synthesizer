# The Four-Part Prompt Grammar

Every prompt in this plugin follows the same four-part grammar. If you can write a prompt that follows the grammar, you can build new prompts that work as well as the ones in the recipes.

## The four parts

### Part 1 — Role and stakes

Set the model's frame. What kind of work is the model doing?

```
You're helping me synthesize fourteen customer discovery interviews
for a B2B SaaS client.
```

This sentence tells the model what kind of work it's doing. It also tells the model what kind of work it's *not* doing — it's not summarization, it's not marketing copy, it's synthesis.

### Part 2 — Input and constraints

Describe what you're giving the model and what counts as valid output.

```
I'm going to paste fourteen transcripts below. They're raw — don't
clean up filler words. Preserve exact wording on quoted material.
```

The constraints are the part most prompts skip and the part that determines whether you get a useful answer or a generic one.

### Part 3 — Process

Tell the model how to work.

```
Do this in three passes, and show me each pass before moving to the
next.
```

This is the part most prompts get wrong. They ask the model to produce the final output directly. Better prompts ask the model to show its work in stages and let you intervene between stages.

### Part 4 — Anti-patterns

Tell the model what **not** to do.

```
Do not flatten contrarian quotes into majority themes. Do not invent
quotes. Do not create a "miscellaneous" bucket.
```

The anti-patterns are the difference between a competent generic answer and a useful specific one. Every model has default behaviors that are wrong for synthesis work. Naming them in the prompt is how you turn the defaults off.

## Read the recipes' prompts with the grammar in mind

Pick any prompt from `/prompts/` and find all four parts. You'll see them in every one. The ratio shifts:

- Clustering prompts have heavier **process** sections
- Stress-test prompts have heavier **role-and-stakes** sections
- Retro prompts have heavier **anti-patterns** sections (dissent preservation)

But the four parts are always there. If a prompt feels off, check which of the four is missing or weak.

## A worked example: building a new prompt

Building a prompt for a workshop type the book doesn't cover — say, a **vendor selection workshop** (procurement team + technical team evaluated three vendors over a half-day).

### Step 1 — Role and stakes

```
You're helping me synthesize a vendor selection workshop. Three
vendors were evaluated by a procurement team and a technical team
over a half-day session. The deliverable is a recommendation to the
VP who'll sign the contract. The recommendation has to be defensible
against a procurement audit and against a technical review six months
from now.
```

### Step 2 — Input and constraints

```
Inputs I'll paste below: the agreed evaluation criteria (weighted),
the scoring sheets from each team for each vendor, discussion notes
from the trade-off conversations, and any flags raised by either
team that didn't make it into the scoring.

Constraints: preserve scoring numbers exactly. Do not average across
teams when the teams scored a vendor differently — surface the
disagreement instead. Use vendor names exactly as they appear in the
source.
```

### Step 3 — Process

```
Do this in three passes, showing me each:

Pass 1 — Score reconciliation. For each criterion, show the
procurement team's score, the technical team's score, the
weighted-average if the teams agreed, and the disagreement flag if
they didn't.

Pass 2 — Trade-off surfacing. For each vendor, identify the strongest
case for selecting them and the strongest case against. Cite criteria.

Pass 3 — Recommendation candidates. Draft three candidate
recommendations, each with a one-line rationale.
```

### Step 4 — Anti-patterns

```
Do not produce a single "best vendor" answer without showing the
trade-offs. Do not flatten team disagreements. Do not use words like
"best," "ideal," "optimal," or "perfect" — they're sales words. Do
not assume any vendor is the answer; the recommendation comes from
the criteria, not from your prior knowledge of the vendors. Do not
invent capabilities or features.
```

That's a working prompt for a workshop type the book doesn't cover. **The four-part grammar took ten minutes to apply.** The prompt is reusable across future vendor selections by changing the inputs.

## How the library grows

Not by copying the prompts from the recipes. By writing **new prompts that follow the grammar**, when the recipes don't cover the work.

## Testing a new prompt

Before you call a prompt library-ready, test it on three inputs:

1. **A clean input** where you know what the right output looks like
2. **A messy input** that has the noise you'd see in the wild
3. **An adversarial input** designed to make the prompt fail (a transcript with no signal, a sticky export full of duplicates, a decision log with contradictions)

Run the prompt on all three. Save the outputs. Read them. If the prompt produces something useful on all three, it's library-ready. If it fails on the messy or adversarial input, you have specific work to do — usually a constraint to add in Part 4.

The test cards live in the library alongside the prompts they tested.

## Source

*The Synthesis Playbook*, prompt appendix "The four-part prompt grammar" section, plus Chapter 10 "Your reusable prompt library" (the worked example of building a vendor-selection prompt).
