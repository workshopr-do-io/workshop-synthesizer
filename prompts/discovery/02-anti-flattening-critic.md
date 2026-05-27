# Prompt #2 — Anti-flattening critic

> **From:** *The Synthesis Playbook*, prompt appendix, #2.
> **Recipe:** Discovery (Ch 4). Used after the first-pass cluster in any cluster-heavy recipe.
> **Used at:** Step 3 — [CLUSTER critic] in `synthesis-discovery/SKILL.md`.
> **Workhorse:** Yes.

## The prompt

```
Here are the themes from the previous pass.

Now act as a critic. Look at the original quote-extraction list.
Identify any quotes that:

1. Got assigned to a theme they don't clearly belong to.
2. Got dropped or buried inside a "minority view" note when they
   actually contradict the majority theme.
3. Express a sentiment or workflow that doesn't appear anywhere else
   but is unusually vivid or specific.
4. Came from [specific segment, e.g. churned customers] and got
   flattened into themes dominated by [the other segment, e.g.
   current customers].

For each problem you find: name the quote, the theme it was assigned
to (or buried in), why the assignment is wrong, and what the quote
actually wants to be — a separate theme, an exception within the
theme, a counter-finding, or evidence that a different theme is more
correct.

Be specific. "This quote doesn't fit" is not an answer. "This quote
contradicts the cluster because the customer is describing the
opposite workflow" is an answer.
```

## What to customize

- `[specific segment]` and `[the other segment]` — e.g. `churned customers` vs. `current customers`, or `enterprise` vs. `SMB`, or `power users` vs. `mid-tier`

## Why this prompt is the most important one in the Discovery recipe

The book is explicit: "skip nothing else, but skip the anti-flattening pass and you ship a synthesis that smooths the spiky quote that was the whole point of the engagement."

Clustering is a math operation that minimizes distance to cluster centers. Spiky outliers increase that distance. The model is not being malicious — it is doing what clustering does. Your job is to catch the smoothing before it ships.

## What to do with the output

For each flagged item:

- **Promote to its own theme** — when the contrarian view has 2+ quotes the cluster missed
- **Mark as an explicit exception inside the theme** — when it's a real minority view but the cluster is otherwise sound
- **Park it** — when it's an outlier without support yet but you don't want to lose it. The Park List is a real file. Keep it.

## Common failures

- **Model declines to push back.** Older models sometimes refuse to "criticize their own output." Re-prompt: "You are not the same agent. You are a critic reviewing prior work."
- **Critic finds nothing.** If the critic returns "all themes look fine," the prompt isn't being honored — re-run with sharper segment framing.

## License

MIT. See `/LICENSE`.
