---
description: Step 4 — make a multi-slide branded carousel locked to your design tokens
argument-hint: [optional — the working folder, e.g. "my-brand/"]
---

Make the branded carousel for this learner:

$ARGUMENTS

Hand this to the visual-producer agent. Use the make-branded-carousel skill: confirm which working folder we're in, read `brand-sheet.md`, `carousel-outline.md`, and `design-tokens.css` from it, lock ONE visual system built from the tokens, and produce every slide in that exact same look by calling the image connector once per slide. If `design-tokens.css` is missing, point the learner back to the design-system step. If Higgsfield isn't connected, save the precise per-slide prompts and say how to connect; don't block. When done, tell the learner to open a new window and run the last step: `make-landing-page` (`/landing-page`).
