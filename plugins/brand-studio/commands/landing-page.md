---
description: Step 5 — build a self-contained, animated, on-brand landing page from your design tokens
argument-hint: [optional — the working folder, e.g. "my-brand/"]
---

Build the landing page for this learner:

$ARGUMENTS

Hand this to the visual-producer agent. Use the make-landing-page skill: confirm which working folder we're in, read `design-tokens.css`, `brand-voice.md`, and `brand-sheet.md` from it, copy the token values into the page `:root` (kept inline so it stays one self-contained file), write the copy in the brand's voice, and save a single animated `landing-page.html` — entrance and scroll-reveal motion, GPU-only, respecting `prefers-reduced-motion`. RTL-correct, Hebrew, no emojis. If `design-tokens.css` is missing, point the learner back to the design-system step. This is the last step — when it's saved, list the full brand pack in the folder and tell the learner the brand is built.
