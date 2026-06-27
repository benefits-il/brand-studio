---
description: Step 3 — auto-pick a polished design system, render it as a page, and export design tokens
argument-hint: [optional — the working folder, e.g. "my-brand/"]
---

Build the design system for this learner:

$ARGUMENTS

Hand this to the visual-producer agent. Use the design-system skill: confirm which working folder we're in, read `brand-sheet.md` and `brand-voice.md` from it, auto-select exactly one of the six bundled presets, render a real, beautiful `design-system.html` showcase (color swatches, type scale, button states, components, spacing scale, shadow ramp), and export a machine-readable `design-tokens.css` the carousel and landing-page steps read. RTL-correct, Hebrew, no emojis. Never pull tokens from any client, course, or personal design system — only the bundled presets. When done, tell the learner to open a new window and run the next step: `make-branded-carousel` (`/carousel`).
