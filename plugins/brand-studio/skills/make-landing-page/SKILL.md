---
name: make-landing-page
description: The final step of BUILD YOUR BRAND. Build a self-contained, animated, RTL-correct HTML landing page for a brand from its design-tokens.css, brand-voice.md, and brand-sheet.md, and save it as landing-page.html. The page inherits the brand's exact tokens and voice, with tasteful entrance and scroll-reveal motion — no external CSS, no build step. Use inside BUILD YOUR BRAND after the design system and carousel, when someone runs /landing-page, or whenever someone wants a one-file animated landing page in their own brand.
---

# Make a landing page

You build a **single self-contained HTML landing page** that looks and sounds like the brand's own — every color, font, radius, and shadow comes from the brand's design tokens, every line of copy comes from the brand's voice, and the page enters with tasteful, GPU-only motion. It is one `.html` file the learner can open in a browser immediately: no external stylesheet, no framework, no build step. This is the last and most tangible output of BUILD YOUR BRAND — the moment the brand becomes a real, living page.

## First — confirm the working folder

You run in a **new window** and don't have the earlier conversation. Open by confirming the working folder ("באיזו תיקייה אנחנו עובדים? אני קורא משם את `design-tokens.css`, `brand-voice.md` ו-`brand-sheet.md`"), then read those files from it. If `design-tokens.css` is missing, point the learner back to the `design-system` step (or `/design-system`) — the page must inherit real tokens, never a generic look.

## Read three files first — do not invent

1. **`design-tokens.css`** — the exact tokens the design-system step exported: colors, the two `--font-*` families with the Google Fonts URL, the radius scale, and the shadow ramp. The page must use these values, not your own taste.
2. **`brand-voice.md`** — how every headline and sentence should sound.
3. **`brand-sheet.md`** — the facts: what the business does, for whom, the promise, the name, the mark.

If any of the three is missing, ask for it (or run the earlier steps). Never fall back to a generic look or generic copy.

## How to work

1. **Read the three files** and hold the tokens, the voice, and the facts.
2. **Start from the template** `templates/landing-page.template.html` (in this skill's folder). It is RTL-first (`dir="rtl"`), token-driven, animated, and has placeholders for the tokens and the copy.
3. **Copy the token values from `design-tokens.css` into the page `:root`** — keep them inline so the page stays one self-contained, shareable file. Map `--bg`, `--surface`, `--ink`, `--muted`, `--accent`, `--accent-strong`, `--border`, `--radius`, `--radius-lg`, the shadow ramp `--shadow-1/2/3`, the two font families, `--maxw`, and the Google Fonts `<link>`. The motion is already in the template — leave it intact.
4. **Write the copy in the brand's voice** — a hero headline and sub-line, one "what we do" section with three short benefit cards, and a closing call-to-action. Use only facts the brand sheet supports. Keep it Hebrew and RTL-correct; force any Latin text or code to LTR with `class="ltr"`. Never mix a Hebrew and an English sentence together. No emojis.
5. **Keep it self-contained and the motion GPU-only.** All CSS stays inline; the only external request is the Google Fonts link. The page already animates `transform`/`opacity`/`filter` only, staggers the hero entrance, reveals sections on scroll via IntersectionObserver, and disables all motion under `prefers-reduced-motion: reduce` — do not add motion that animates layout properties.
6. **Save** as `landing-page.html` in the learner's folder and offer to open it.

## RTL and motion are not optional

The course is Hebrew. The page ships `lang="he" dir="rtl"`, text aligns to the start (right), and the layout mirrors correctly. The only LTR islands are explicit `.ltr` spans for URLs, code, or Latin brand names. The entrance and scroll-reveal motion is part of what makes the page feel finished — but it must always honor `prefers-reduced-motion`. A page that breaks RTL, or that janks because it animates width/height/top/left, is a failed page — check it before reporting done.

## This is the last link — close the chain

This is the final step of BUILD YOUR BRAND. When the page is saved, there is no next window. List the full brand pack now in the folder — `brand-sheet.md`, `brand-voice.md`, the base documents, `design-system.html`, `design-tokens.css`, the carousel, and `landing-page.html` — and tell the learner in plain Hebrew that the brand is built: they can open the landing page, edit any file and re-run a single step, and everything will stay consistent because it all reads the same tokens and voice.

## Why one self-contained file

A non-developer can open, share, or host a single HTML file with zero setup. Because it inherits `design-tokens.css`, it matches the carousel and the email automatically — one coherent brand across all three. Because the copy comes from the voice profile, it sounds like them, not like a template.

## Example

The design tokens are `editorial-warm` (warm neutrals, Lora headings, soft radius, whisper shadow ramp) and the brand is a neighborhood bakery. You copy those tokens into `:root`, load Lora + Inter from Google Fonts, write a warm Hebrew hero ("אפייה ביתית, טרייה כל בוקר") that fades in, three benefit cards that reveal on scroll, and a gentle CTA — then save `landing-page.html` and offer to open it.
