---
description: Run the Strategic Offsite & Stakeholder Politics recipe — turns an exec offsite into three tiered artifacts (CEO memo, board deck, confidential appendix). The hardest recipe in the book; the model assists with ~15% of the work.
model: opus
---

Trigger the `synthesis-offsite` skill in `full` mode. Honor explicit alternate modes: `founder-board` (founder + board strategy day).

The recipe's 8-step pipeline closes the model at three steps by design (Step 2 political read, Step 6 confidential appendix, Step 7 altitude-leak check). The agent refuses to advance these with model assistance.

Verify the user has written a **Day-One Read brief** before running. Without it, the political read cannot be reconstructed reliably. See `synthesis-offsite/references/day-one-read-brief.md`.

Uses opus per project policy for politics-heavy synthesis.

Mode reference: `MODE_REGISTRY.md` § synthesis-offsite.
Skill entry: `synthesis-offsite/SKILL.md`.
