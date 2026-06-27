---
description: Step 2 — write an on-brand marketing email from your folder and save it (and optionally a Gmail draft)
argument-hint: [optional — the working folder, e.g. "my-brand/"]
---

Write the marketing email for this learner:

$ARGUMENTS

Hand this to the content-writer agent. Use the write-marketing-email skill: confirm which working folder we're in, read `brand-voice.md` and `brand-sheet.md` from it, auto-draft the brief yourself, write a short marketing email in the brand's voice, and save it as `marketing-email.md` in the folder. Then, when the Gmail connector is on, create the email as a Gmail draft through the connector (subject plus body) — never send; if Gmail isn't connected, point the learner to turn it on (Customize → Connectors → Gmail) and don't block. Gmail is a first-party Cowork connector, not part of this plugin's `.mcp.json`. Hebrew-first and RTL-correct, no emojis. If the brand files aren't in the folder, point the learner back to start-here. When done, tell them to open a new window and run the next step: `design-system` (`/design-system`).
