# Prompt #6 — Argue-the-other-side critic

> **From:** *The Synthesis Playbook*, prompt appendix, #6.
> **Recipe:** Strategic offsite (Ch 5), Ideation (Ch 7). The steelman move.
> **Used at:** Step 3 — [PRIORITIZE] sanity check in `synthesis-offsite/SKILL.md`. Also used wherever a contested cut needs a sanity check.
> **Workhorse:** Yes.

## The prompt

```
Here is my proposed [decision / split / interpretation]: [paste].

Argue the strongest case that [the alternative], or be specific
about the risk you'd be naming if you went the other way.

Make the alternative as strong as you can. Do not soften it. The goal
is to surface the trade-off, not to confirm the original choice.
```

## What to customize

- `[decision / split / interpretation]` — pick the relevant noun for your situation
- `[paste]` — your proposed choice
- `[the alternative]` — the alternative path (e.g. `decision X should go in artifact Y instead of artifact Z`, or `we should keep idea N on the shortlist rather than cut it`)

## How this differs from prompt #3 (interpretation stress-test)

- Prompt #3 is for interpretations — *what does this cluster mean?*
- Prompt #6 is for decisions and cuts — *should we go this way or that way?*

Both follow the same logic: the model is good at steelmanning, bad at advocating. Use prompt #6 anytime you've made a call that costs you something to make and you want to know if you can defend it.

## Common failures

- **Model softens the alternative.** Re-prompt: "Treat the alternative as if you genuinely believe it. Do not signal hedge."
- **Model just summarizes your decision.** If you get back "Here are the trade-offs of your decision..." instead of "Here is the case for the opposite...", re-prompt with the framing: "Pretend a colleague disagrees with me and you're writing their best argument."

## License

MIT. See `/LICENSE`.
