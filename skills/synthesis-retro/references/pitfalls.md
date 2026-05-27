# Retro & Post-Mortem Recipe — Pitfalls

Five ways a retro synthesis fails.

## 1. The false-consensus cluster

**Symptom:** The model finds the "majority" theme and frames it as if the room agreed. Three quiet people who actually disagreed get folded in. The write-up reads consensus. The team reads it and feels invisible.

**Fix:** Every theme that touches a disagreement gets a minority-view subsection, **even when the minority is one voice.** The lone voice with 1-of-33-dots may be the most important sticky in the room.

## 2. Minority views grouped into "miscellaneous"

**Symptom:** The model creates a "miscellaneous" bucket and dumps the dissent there. The dissent reads as random rather than as a pattern.

**Fix:** Prompt explicitly against the miscellaneous bucket. Force the model to either fit the sticky to an existing theme or surface it as its own theme.

## 3. Action items that read good but have no owner

**Symptom:** *"We will improve cross-team communication."* No owner. Won't happen.

**Fix:** Every action item names a person. *"The EM will run a cross-team handoff working session within 30 days."* That's an action item. *Improve communication* is a wish.

## 4. Polishing the loudest theme

**Symptom:** The room talked about "communication" for 45 minutes. You spend Sunday polishing the communication theme into a beautiful paragraph. The trust sticky from the quiet engineer gets a one-line mention. The team reads the write-up and the EM nods at the communication paragraph and skips the trust line.

**Fix:** **Word count is a tell.** If the most-discussed theme has five times more words than the dissent, the synthesis has flattened. Aim for proportional weight, not proportional to room time.

## 5. Action items disconnected from themes

**Symptom:** Twelve action items in the room. Three of them connect to no theme — they're floating wishes ("we should adopt feature flags," with no context). They get into the write-up because someone wrote them on a sticky and dot-voted.

**Fix:** Every action item ties explicitly back to a theme. If it doesn't, it goes in the "discussed but didn't commit" appendix.

## Post-mortem-specific pitfalls

- **AI-generated timelines that read crisp but lose the messy-but-true sequence of decisions under pressure.** Hold the line on "do not impose retrospective clarity" — see [`post-mortem-variant.md`](post-mortem-variant.md).
- **Blame-cause confusion.** Even after running the cause-vs-blame check, sometimes the rewrites lose meaning. Read each rewrite carefully; the goal isn't to dodge accountability, it's to put accountability where it can do good.

## Source

*The Synthesis Playbook*, Chapter 8 "Retro & post-mortem synthesis," pitfalls section.
