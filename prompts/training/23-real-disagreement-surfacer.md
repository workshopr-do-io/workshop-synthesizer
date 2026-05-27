# Prompt #23 — Real-disagreement surfacer

> **From:** *The Synthesis Playbook*, prompt appendix, #23.
> **Recipe:** Training debrief (Ch 9) — Cross-functional alignment ADAPT sidebar.
> **Used at:** After prompt #22 in the cross-functional alignment variant.

## The prompt

```
Here are the position maps for each function: [paste].

For each apparent disagreement, evaluate whether the stated disagreement
is the real disagreement or a surface version of a deeper one.
Specifically:

1. If two functions disagree on timing, is the real disagreement about
   scope or about ownership?
2. If two functions disagree on approach, is the real disagreement
   about whose KPI is being prioritized?
3. If a function expresses concern about "the customer," is the concern
   about the customer or about how the function is going to look if
   the customer reacts badly?

For each disagreement: name the stated version, the likely real version,
and what evidence in the discussion notes supports your read.
```

## What to customize

- `[paste]` — output from prompt #22 (position maps per function)

## Why stated disagreements aren't always real disagreements

Cross-functional rooms often have *stated* disagreements that aren't the real disagreements:

- Engineering says "we don't have time" → the real disagreement is about scope
- GTM says "the customer won't accept it" → the real disagreement is about positioning
- Product says "we need more data" → the real disagreement is about who has authority to make the call

Surfacing the real disagreement enables a follow-up conversation that actually resolves it. Surfacing only the stated disagreement traps the team in proxy wars.

## What to do with the output

For each real-disagreement surfaced, decide:

- **Reconvene the room** — schedule a 30-minute follow-up explicitly to address the real disagreement
- **Surface in the synthesis deliverable** — name it in the parked-disagreement appendix so the convener can address it asynchronously
- **Park for now** — when the real disagreement is bigger than the current session can resolve, flag it and recommend who needs to weigh in

## Common failures

- **Model defaults to the stated disagreement.** If the output just rewords what the room said, re-prompt: "Look beyond the stated disagreement. What does the evidence suggest is the deeper conflict?"
- **Model invents the real disagreement.** Spot-check: if the model claims the real disagreement is X but you don't see evidence in the notes, it's pattern-matching from training data, not your room. Reject.
- **Model collapses all disagreements to "KPI conflict."** Some are. Not all. Re-prompt with the specific dimensions (timing, approach, customer-concern) and demand the model use them.

## License

MIT. See `/LICENSE`.
