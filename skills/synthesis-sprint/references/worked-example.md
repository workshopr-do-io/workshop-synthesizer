# Design Sprint Recipe — Worked Example

*Composite — drawn from a couple of dozen design sprints between 2017 and 2025. Tester quotes are paraphrased from typical patterns across sessions, not transcribed from a single sprint. The pattern is real; the specific session isn't.*

The full worked example — *the swipe-or-not call* — is in the book, Chapter 6. Summary below.

## Setup

Four-day design sprint at a mid-size B2B. Team is rebuilding manager approval of expense reports. Sprint goal: *land on a flow that reduces manager time-to-decision while still feeling defensible at audit.*

Decide vote: **4-1** for a swipe-style review interface with a "delegate up" escalation rail. The "1" was the engineering lead, who wanted a simpler list view.

Friday user tests, five managers:

- **Tester 1:** swipe in 90 seconds. Used delegate-up correctly.
- **Tester 2:** swipe works, but kept tapping line items reflexively. *"Have to retrain her thumb."*
- **Tester 3:** liked the interface. Asked to view the receipt without leaving the screen. Currently can't.
- **Tester 4:** missed the delegate-up rail entirely. Approved every expense, including one that would have been an audit issue. *"Wait, was I supposed to send some of these somewhere?"*
- **Tester 5:** refused the swipe interface. *"Her team would never trust an approval that took a thumb swipe."* Asked for an explicit "approve" button.

## Mapping against hypothesis

Hypothesis: *swipe-based approval reduces manager review time without compromising audit defensibility.*

- Tester 1: Supports
- Tester 2: Complicates (swipe works, but tap habit is real)
- Tester 3: Complicates (workflow blocker on receipt view)
- Tester 4: **Broke** (audit-defensibility fails — missed escalation)
- Tester 5: **Broke** (trust in mechanism fails)

**Tally: 1 supports, 2 complicate, 2 break.**

40% of testers failed the audit-defensibility leg. Hypothesis was a conjunction (speed *and* defensibility). Two breaks on defensibility is a hypothesis-level break.

## The recommendation

Draft 1: *iterate before shipping.* Stumbled aloud — the iteration involved adding a parallel mode that essentially admitted the swipe pattern wasn't trusted, which is a structural concession.

Draft 2 (shipped):

> *Iterate before shipping. The swipe interface tests well on speed but fails the audit-defensibility leg of the hypothesis in 2 of 5 sessions. We recommend adding an explicit-approve mode in parallel to swipe and re-testing with five more managers. If the parallel mode resolves the audit issue, ship the winner. If not, reconsider the list-view alternative voted down on Thursday.*

The fallback to list-view honored the engineering lead's original push. Gave the team a real off-ramp.

## What changed our mind

> *The room voted on a hypothesis that swipe would reduce time-to-decision. The testing supported that. The room did not vote on whether swipe would maintain audit defensibility — that leg of the hypothesis was implicit. In testing, two of five managers failed the audit-defensibility leg in ways the Decide vote couldn't have surfaced: one missed an escalation, one refused the pattern entirely. The room could see speed; the room could not see trust.*

This section honored the room's vote — the team wasn't wrong; they voted on the question they could see. The testing surfaced a question they couldn't.

## The result

Sent Sunday at 7 p.m. By Monday morning, the engineering lead replied:

> *"Thank you for not dismissing my list-view comment from Thursday. I think the parallel-mode test is the right next move and I'll build it this week."*

Two weeks later, re-tested with parallel mode. Three of five managers used delegate-up correctly without swipe-only pressure. Hypothesis cleared. They shipped.

## What this example teaches

- **The tally is mechanical, on purpose.** Doing the supports/complicates/breaks count in writing prevents the bias of re-coding breaks as complications.
- **The "what changed our mind" section honors the room.** Same content, different politics — without it the recommendation reads as a verdict.
- **The fallback matters.** Recommending iteration without naming the off-ramp leaves the team without a real choice.
- **Sunday-night send beat Monday-morning send.** The engineering lead had hours to process before the standup.

## Source

*The Synthesis Playbook*, Chapter 6, worked example. Composite per the book's disclosure convention.
