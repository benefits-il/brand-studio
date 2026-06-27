---
name: make-branded-carousel
description: Step 4 of BUILD YOUR BRAND. Create a multi-slide branded Instagram carousel — several images that share one exact look — from the brand's files and its design-tokens.css, so the carousel matches the design system. Use inside BUILD YOUR BRAND, whenever someone asks for a carousel, or when they run /carousel. Reads the brand from the working folder and calls the image connector once per slide.
---

# Make a branded carousel

You make a multi-slide Instagram carousel: several images that read as one set because they share the exact same look — **and that look is locked to the brand's design tokens**, so the carousel matches the design system, the landing page, and the email. You read the brand sheet (colors, type, mark, mood), the carousel outline (the content of each slide), and the **design tokens** (`design-tokens.css`, the exact colors and type the design-system step chose). You lock one visual system from the tokens, build a precise prompt per slide so every slide matches, call the image connector once per slide, and return the set.

## First — confirm the working folder

You run in a **new window** and don't have the earlier conversation. Open by confirming the working folder ("באיזו תיקייה אנחנו עובדים? אני קורא משם את `brand-sheet.md`, `carousel-outline.md` ו-`design-tokens.css`"), then read those files from it. If `design-tokens.css` is missing, point the learner back to the `design-system` step (or `/design-system`) so the carousel can match the system.

## Work from the brand's files — do not invent a brand

- **`brand-sheet.md`** — the brand's mood, mark, and facts.
- **`carousel-outline.md`** — the per-slide content: what each slide says and shows.
- **`design-tokens.css`** — the exact colors and type the design system locked. Use these values verbatim; they are what keeps the carousel coherent with the rest of the pack.
- **`brand-voice.md`** — for any on-image wording, so the words sound like the brand.
- If the brand files aren't there, point the learner back to `start-here`; do not fall back to a generic look or guess a brand.

## How to work

1. Read the brand sheet, the carousel outline, the brand voice, and `design-tokens.css`.
2. **Lock ONE precise visual system for the whole set, built from the tokens.** Pull the exact background, the exact accent color, the type feel, and a fixed slide layout straight from `design-tokens.css` (the `--bg`, `--accent`, font families). Add the mark and where it sits from the brand sheet. Write this system down so it is identical for every slide.
3. For each slide, build a **fully-precise image prompt** that reuses that exact same system and adds only the slide's own content and on-image text in quotes. The background, accent, type, mark placement, and layout stay constant across all slides; only the words and any per-slide focal element change. Spell every choice out, and name the exact hex values from the tokens.
4. Call the image connector — the image/video connector bundled in this plugin's `.mcp.json` (Higgsfield) — once per slide, in order.
5. Return the full set in slide order plus one short line, and offer one variation (for example a different layout applied consistently across all slides).

## Consistency is the whole point

A carousel only works if the slides look like siblings. Lock the visual system once — from the tokens — and repeat it word-for-word in every slide prompt: same background, same accent, same type, same mark placement, same layout. If you let any of these drift between prompts, the slides will not match and the set falls apart. Vary the content, never the system. Because the system comes from `design-tokens.css`, the carousel also matches the design system and the landing page automatically.

## Why each prompt has to be precise

The bundled image connector runs on a free tier by default — a basic model with a watermark and mediocre output unless you steer it hard. A complete, exact prompt per slide is the only lever for good, consistent output on the free tier: every visual choice named, repeated identically across slides. The learner can optionally upgrade to a paid Higgsfield subscription (around fifteen dollars a month) for clean, high-definition output.

## Then — hand off to the last window

When the set is produced (or the precise per-slide prompts are saved if Higgsfield isn't connected yet), **stop**. Give the transition in plain Hebrew: "הקרוסלה מוכנה, באותה מערכת-חזותית של מערכת-העיצוב. השלב האחרון — **פתח שיחה חדשה והרץ את `make-landing-page`** (או `/landing-page`) — הוא יבנה עמוד-נחיתה יפה עם אנימציות, על אותם טוקנים." If the image connector isn't on, say so in one line and point the learner to connect Higgsfield later; do not block.

## Example

If the tokens say near-black background `#08090A` with one indigo accent `#5E6AD2` and a heavy geometric type, and the outline has three slides ("THE PROBLEM", "WHAT WE BUILT", "TRY IT"), you lock one system — *square slide, `#08090A` background, one `#5E6AD2` accent, heavy geometric uppercase headline, the brand mark in the lower-right corner, centered layout, no gradients, no stock photography* — and send the connector that exact system three times, changing only the headline text in quotes per slide.
