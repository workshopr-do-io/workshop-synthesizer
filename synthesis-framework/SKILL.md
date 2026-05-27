---
name: synthesis-framework
description: >
  The foundational framework for workshop synthesis. Defines the four moves
  (cluster, interpret, prioritize, narrate), the AI in/out line through each
  move, the synthesis stack, the synthesis-ready file template, the Stakes ×
  Politics matrix, and the "human-authored, machine-assisted" principle.
  Every other synthesis-* skill in this plugin depends on this one. Use this
  skill when a user is new to the framework, or when a downstream recipe
  needs to surface a definition (e.g., "what's [PRIORITIZE] mean again?").
  Triggers on: "four moves", "synthesis framework", "what is synthesis",
  "human-authored machine-assisted", "Stakes Politics matrix", "synthesis-
  ready file", "consent and data".
---

# Synthesis Framework

The foundational skill. Read this first; every recipe depends on it.

## The four moves

Every workshop synthesis you'll ever do is some arrangement of four moves:

| Tag | Move | What it does |
|---|---|---|
| `[CLUSTER]` | Cluster | Group the raw pile into candidate themes. Hands-off — the model leads, you verify. |
| `[INTERPRET]` | Interpret | Name what each cluster means. Hands-on — the model assists, you author the sentence. |
| `[PRIORITIZE]` | Prioritize | Decide which interpretations matter most. Hands-only — model closed or sparring partner. |
| `[NARRATE]` | Narrate | Shape the whole into the story the client receives. Co-writing — model drafts, you shape. |

You'll see these bracket tags throughout the recipe chapters. When you see a tag, it tells you which posture to take.

For full definitions: see [`references/four-moves.md`](references/four-moves.md).

## The synthesis stack (five layers)

Most facilitators have all five already, mostly by accident. The point of naming them is to stop reinventing the stack every weekend.

1. **Capture** — Miro, sticky exports, photos, vote results, decision logs
2. **Transcript** — Granola, Fireflies, Otter, Zoom embedded, human, or your notebook
3. **Synthesis** — a Notion page, a markdown file, sometimes a Miro board for clustering
4. **Model** — Claude or ChatGPT, vanilla, no special setup
5. **Output** — deck, brief, one-pager, note — usually two or three per engagement

## The synthesis-ready file

Build this **before the workshop ends** to save your weekend. Template structure (capture / transcript / reference / workspace) lives in [`references/synthesis-ready-file.md`](references/synthesis-ready-file.md).

## The Stakes × Politics matrix

Pin yourself on this matrix at the start of every engagement, in writing.

|  | Low politics | High politics |
|---|---|---|
| **Low stakes** | AI on for everything | AI on for [CLUSTER] and [NARRATE]; off for [INTERPRET] and [PRIORITIZE] |
| **High stakes** | AI on for [CLUSTER] and [NARRATE] drafts; you author [INTERPRET] and [PRIORITIZE] | AI on for [CLUSTER] only; everything else by hand |

Full matrix with examples: [`references/stakes-politics-matrix.md`](references/stakes-politics-matrix.md).

## The principle

> **Human-authored, machine-assisted.**

The model assists. The human authors. Your name is on the deck. The interpretation comes out of your head. The ranking comes out of your judgment. The story comes out of your relationship with the room.

Full operationalization: [`references/human-authored-machine-assisted.md`](references/human-authored-machine-assisted.md).

## Consent and data (read before you paste)

The recipes recommend pasting client material — interview transcripts, sticky exports, decision logs — into a commercial LLM. That's workable. It is also a privacy and IP move that has to be handled before you paste.

Four questions: consent, data retention, jurisdiction (GDPR/HIPAA/FERPA), anonymization bar.

Full discipline: [`references/consent-and-data.md`](references/consent-and-data.md).

## Reference files

| File | Load when... |
|---|---|
| [`references/four-moves.md`](references/four-moves.md) | A recipe references CLUSTER/INTERPRET/PRIORITIZE/NARRATE and you want the full definition |
| [`references/synthesis-ready-file.md`](references/synthesis-ready-file.md) | Building the working file before a workshop ends |
| [`references/stakes-politics-matrix.md`](references/stakes-politics-matrix.md) | Deciding when AI is on or off for a given engagement |
| [`references/human-authored-machine-assisted.md`](references/human-authored-machine-assisted.md) | Defining what "authorship" means in practice, or handling client disclosure |
| [`references/consent-and-data.md`](references/consent-and-data.md) | Before pasting any client material into the model |

## How this skill is used

Other skills in this plugin reference this one. When `/ws-discovery` runs and the workflow says "now do [CLUSTER]", that bracket tag points back to the four-moves definition here. When a user asks "what does the stack look like for an offsite", the offsite skill defers to [`references/synthesis-ready-file.md`](references/synthesis-ready-file.md) here.

This skill rarely runs standalone. It's the foundation other recipes stand on.

## Source

Lifted from *The Synthesis Playbook* chapters 1–3 (the four moves, the synthesis stack) plus the front-matter "Consent and data" section. Verbatim where possible; condensed where the book's prose was scene-setting rather than load-bearing.

Book chapters → reference files map:
- Ch 1 "Synthesis is a craft, not a summary" → woven into [`references/four-moves.md`](references/four-moves.md) intro
- Ch 2 "The four moves" → [`references/four-moves.md`](references/four-moves.md)
- Ch 3 "Your synthesis stack" → [`references/synthesis-ready-file.md`](references/synthesis-ready-file.md), [`references/stakes-politics-matrix.md`](references/stakes-politics-matrix.md), [`references/human-authored-machine-assisted.md`](references/human-authored-machine-assisted.md)
- Front matter (added in r1) → [`references/consent-and-data.md`](references/consent-and-data.md)
