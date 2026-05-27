# Contributing to The Synthesis Playbook plugin

Thanks for being here. The prompts and recipes in this plugin are designed to be copied, adapted, and improved. If you've built a version that works better than mine, send it — I'll steal it back, and credit you for the steal.

## Three kinds of contribution

### 1. Prompt improvements

If you've tightened a prompt, added a constraint that prevents a real failure mode, or fixed a hallucination pattern, open a pull request against the prompt file in [`prompts/`](./prompts).

Rules:

- The prompt must still follow the **four-part grammar** (role and stakes, input and constraints, process, anti-patterns). See [`prompts/README.md`](./prompts/README.md).
- Don't add language that flatters the user or the model. The whole book is engineered against generic AI prose.
- If the change is structural (not just wording), include a one-paragraph note in the PR explaining what failure mode you're addressing.
- Open an issue first if you're not sure.

### 2. New workshop-type recipes

The book covers six workshop types. There are more. Customer Advisory Boards, vendor selections, hiring loops, board meetings — all candidates.

If you want to add a new recipe:

1. Open an issue first with the workshop type, the move mix (cluster/interpret/prioritize/narrate weights), and the proposed prompts.
2. Once scoped, follow the structure of `skills/synthesis-discovery/` as your template.
3. Include: SKILL.md, references/workflow.md, references/prompts.md, references/pitfalls.md, references/worked-example.md, and one slash command in `commands/`.
4. The worked example should be a composite, not a real engagement — and disclose that in the file, the way the book does.

### 3. Bug reports and clarifications

- Plugin loads incorrectly in Claude Code → open an issue with your Claude Code version and the error.
- A prompt doesn't work in a specific model → open an issue naming the model and what failed. The book is platform-neutral, but prompts decay across model versions. If yours broke, others' will too.
- Wording in a SKILL.md or reference file is unclear → open a PR with the fix.

## What I won't accept

- New "where AI hurts" lists without a paired "where AI helps." The book's discipline is to keep both visible. PRs that only document failure modes will be asked to balance the framing.
- Generic "best practices" prose. The book's voice is first-person, time-stamped, and specific. If a contribution reads as anonymous LinkedIn-shaped prose, I'll ask for a rewrite.
- Workshopr.io-specific functionality. This plugin is platform-neutral by design (see Chapter 11 of the book). Hosted-platform integration is downstream and not part of this repo.

## Voice

If you write a new recipe or SKILL.md, the voice should match the book. A few markers:

- First person where it earns its place. Time-stamped failures over abstract advice.
- Kitchen, craft, or working-tradesperson metaphors where they fit, not as filler.
- Short fragments for emphasis. Long paragraphs only when the idea needs them.
- No "leverage," "comprehensive," "robust," "key," "critical," "streamline," "empower," "elevate." Strip them.
- Read it aloud before you submit the PR. If you stumble, rewrite.

## Code of conduct

Be a decent collaborator. Punching down isn't useful. Punching up at AI hype is encouraged.

---

*Pick up the pan.*
