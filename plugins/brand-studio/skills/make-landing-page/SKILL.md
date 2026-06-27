---
name: make-landing-page
description: Build a self-contained, RTL-correct HTML landing page for a brand from its design-system.md, brand-voice.md, and brand-sheet.md, and save it as landing-page.html. The page inherits the brand's exact tokens and voice — no external CSS, no build step. Use inside BUILD YOUR BRAND after the email and carousel, or whenever someone wants a one-file landing page in their own brand.
---

# Make a landing page

You build a **single self-contained HTML landing page** that looks and sounds like the brand's own — every color, font, radius, and shadow comes from the brand's design system, and every line of copy comes from the brand's voice. It is one `.html` file the learner can open in a browser immediately: no external stylesheet, no framework, no build step. This is the last and most tangible output of BUILD YOUR BRAND — the moment the brand becomes a real page.

## Read three files first — do not invent

1. **`design-system.md`** — the exact tokens. Colors, typography (with the Google Fonts link), radius, shadows, spacing. The page must use these values, not your own taste.
2. **`brand-voice.md`** — how every headline and sentence should sound.
3. **`brand-sheet.md`** — the facts: what the business does, for whom, the promise, the name, the mark.

If any of the three is missing, ask for it (or run the earlier steps). Never fall back to a generic look or generic copy.

## How to work

1. **Read the three files** and hold the tokens, the voice, and the facts.
2. **Start from the template** `start-here/templates/landing-page.template.html`. It is RTL-first (`dir="rtl"`), token-driven, and has placeholders for the tokens and the copy.
3. **Fill the tokens** in `:root` from `design-system.md` exactly — including the Google Fonts `<link>` for the chosen fonts. Map `--bg`, `--surface`, `--ink`, `--muted`, `--accent`, `--accent-strong`, `--border`, `--radius`, `--shadow`, the two font families, and the max width.
4. **Write the copy in the brand's voice** — a hero headline and sub-line, one "what we do" section with three short benefit cards, and a closing call-to-action. Use only facts the brand sheet supports. Keep it Hebrew and RTL-correct; force any Latin text or code to LTR with `class="ltr"` (already defined as `direction:ltr;unicode-bidi:isolate`). Never mix a Hebrew and an English sentence together.
5. **Keep it self-contained.** All CSS stays inline in the `<style>` block; the only external request is the Google Fonts link. No JavaScript is required.
6. **Save** as `landing-page.html` in the learner's folder and offer to open it. Mention they can re-run this step after editing any copy or token.

## RTL is not optional

The course is Hebrew. The page ships `lang="he" dir="rtl"`, text aligns to the start (right), and the layout mirrors correctly. The only LTR islands are explicit `.ltr` spans for URLs, code, or Latin brand names. A page that breaks RTL is a failed page — check it before reporting done.

## Why one self-contained file

A non-developer can open, share, or host a single HTML file with zero setup. Because it inherits the design system, it matches the carousel and the email automatically — one coherent brand across all three. Because the copy comes from the voice profile, it sounds like them, not like a template.

## Example

The design system is `editorial-warm` (warm neutrals, Lora headings, soft radius, whisper shadows) and the brand is a neighborhood bakery. You fill those tokens into `:root`, load Lora + Inter from Google Fonts, write a warm Hebrew hero ("אפייה ביתית, טרייה כל בוקר"), three benefit cards, and a gentle CTA — then save `landing-page.html` and offer to open it.
