# Prompt #17 — Retro write-up drafter

> **From:** *The Synthesis Playbook*, prompt appendix, #17.
> **Recipe:** Retro (Ch 8).
> **Used at:** Step 5 — [NARRATE] in `synthesis-retro/SKILL.md`.

## The prompt

```
I'm drafting a public write-up for a team retro. Here are the linked
themes with my interpretations: [paste].

Draft sections 2 and 3 of the write-up: "what worked" and "what didn't."
Two or three paragraphs per section. For each theme, name the theme,
summarize the dominant view, and if a minority view is present, surface
it explicitly with framing that doesn't soften it.

Tone: this write-up will be read by the [N] people who were in the room.
Treat them as adults. Do not soften sharp findings into management-speak.
Do not use words like "leverage," "robust," "key," "critical," "strategic."
Use the team's own words from the stickies where they're clean enough.

Constraints: preserve quoted sticky wording where it's exact. Do not
invent stickies. Where a minority view contradicts the dominant view,
surface both in the same paragraph, not in separate sections.
```

## What to customize

- `[paste]` — your linked themes with the interpretations you wrote by hand (output of Step 3 in the recipe)
- `[N]` — number of people in the retro

## What this prompt does NOT cover

The public retro write-up has six sections. This prompt only drafts sections 2 and 3 (what worked, what didn't). The other four sections you write by hand or draft elsewhere:

1. **One-line summary** — yours
2. **What worked** — this prompt drafts
3. **What didn't** — this prompt drafts
4. **What we're changing** — your action items (Step 4 of the recipe)
5. **What we discussed but didn't commit to** — yours
6. **A short note on the room** — feelings temperature; yours

## What to edit

Take the model's output. Edit by hand. The biggest edit you'll make is **restoring sharpness** — the model rounds off spiky edges by default. Sharpen them back.

Read the whole write-up aloud with the room in mind. If you stumble on a sentence imagining the team reading it, rewrite. If a paragraph would let a particular team member off the hook for something the room actually addressed, rewrite. If a paragraph would land hard on a particular team member in a way the room didn't intend, rewrite.

## Common failures

- **Model softens minority views.** The constraint is explicit but models slip. Re-prompt: "Where a minority view contradicts, surface both in the same paragraph. Do not put the minority view in a 'footnote' tone."
- **Banned vocabulary sneaks back.** Re-prompt with the explicit list of words and demand a rewrite of any paragraph that uses them.
- **Model paraphrases stickies.** Quoted material should be verbatim. If the model rewrites a sticky for "clarity," restore the original wording.

## License

MIT. See `/LICENSE`.
