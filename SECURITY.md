# Security and Privacy

This plugin handles workshop synthesis material — interview transcripts, sticky exports, decision logs, post-mortem chats. That material is often confidential. A few things you should know, and one thing to report.

## What the plugin does with your data

- The plugin reads files from your local disk via the standard Claude Code Read tool.
- The plugin sends those files to whichever LLM you've configured Claude Code to use.
- The plugin does **not** send your data to me, to Workshopr.io, to a tracking endpoint, or to any third-party service beyond your configured model provider.
- The plugin does **not** retain your data after the session. Any persistence is on you and on Claude Code.

## What you should do with your data

Before pasting client material into the plugin, run the four-question check from Chapter 3 of the book:

1. **Consent** — does your interview/workshop consent form actually allow third-party model processing?
2. **Data retention** — is your model provider's no-training setting on?
3. **Jurisdiction** — does GDPR, HIPAA, FERPA, or sector-specific law apply? If yes, the LLM provider becomes your subprocessor under the law. Paperwork follows.
4. **Anonymization** — strip full names, email addresses, employee IDs, account numbers. The recipes work on stripped material.

If you can't clear all four for a given engagement, the recipes are not the right move. Run the synthesis by hand.

## Reporting a security issue

If you find:

- A prompt injection that escapes the human-authorship pauses (an agent runs through [INTERPRET] or [PRIORITIZE] without stopping for you),
- A path-traversal or file-access issue in any pipeline agent,
- A way the plugin sends data anywhere other than your configured model provider,

email me directly at **bill@workshopr.io** with `[synthesis-playbook security]` in the subject. Don't open a public issue for security reports.

I will respond within 7 days. I am one person; please be patient and don't disclose publicly before we've had time to fix.

## What is not a security issue

- The model produced a bad cluster, an awkward interpretation, or a slop-flavored deliverable. That's a recipe-quality issue. Open a regular issue and tell me what failed and how.
- The model refused to engage with workplace-friction content. That's an LLM-policy thing, not a plugin thing. Try a different model.

---

*The recipes are yours. The work is yours. The data is yours. Handle it like it is.*
