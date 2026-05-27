# Consent and Data

A short section the author almost left out of the first draft. Read it before pasting any client material into the model.

The recipes recommend pasting raw client material into a commercial LLM — interview transcripts, sticky exports, decision logs, post-mortem chats. That's workable. It is also a privacy and IP move that has to be handled before you paste, not after.

**Four questions. Run them every time.**

## 1. Consent

What did your consent form actually allow?

*"We may record this for internal research"* is not the same as *"we may upload this to a third party that may train on it."*

If the consent form was silent on third-party processing, you have a conversation to have — with the interviewees, with the client who commissioned the work, sometimes both. Have it before the synthesis starts, not after the deliverable ships.

## 2. Data retention

Most commercial models default to logging your inputs. Most also offer a way to opt out:

- **Anthropic's "no training" setting** on enterprise plans
- **OpenAI's data controls** in ChatGPT Settings
- **API-level no-training options** on both Anthropic and OpenAI

Set yours **before** you paste. The defaults change; check on the day you run the recipe, not on the day you read this book.

## 3. Jurisdiction

If your client is in the EU, UK, or any GDPR-shaped jurisdiction, you are likely a **data processor** under the law and the LLM provider is your **subprocessor**. Paperwork follows:

- A Data Processing Agreement (DPA) with the LLM provider
- Notice to the data subjects (interviewees, workshop participants)
- A record of processing activities

Same story for:

- **HIPAA** in U.S. healthcare
- **FERPA** in U.S. education
- **GLBA** in U.S. financial services
- Sector-specific frameworks in regulated industries

If you work in one of these contexts, your synthesis-ready file should include a line stating which framework applies and how you're handling it. The Reference section is the right place for it.

## 4. Anonymization

Strip the things the model doesn't need:

- Full names → use first initial or pseudonym
- Email addresses → remove entirely
- Employee IDs, account numbers, customer IDs → remove or hash
- Internal project codenames if they're identifying → generalize
- Specific dollar figures or revenue if confidential → use ranges

The recipes work on stripped material. They do not work better on un-stripped material.

**The minimum bar:**

- No personally identifying information that wasn't already public
- No client confidential strategy the client hasn't agreed to process externally

## When the answer is "I can't clear all four"

If you can't clear all four for a given engagement, **the recipes are not the right move.** Run the synthesis by hand. Take longer. Charge accordingly. Keep the relationship.

This is rare for most consulting engagements, common for healthcare/legal/education work, and increasingly common in EU-based work as GDPR enforcement tightens.

## Things this section does NOT cover

This is not legal advice. It's a working discipline. If you're in a regulated industry or working with vulnerable populations (minors, healthcare patients, criminal justice contexts), talk to a lawyer before relying on this section. The book's discipline is necessary but not sufficient.

## Source

*The Synthesis Playbook*, front matter "Consent and data" section, shipped in the r1 P0 revision following peer-review feedback that the absence was a publication-blocking gap.
