---
name: design-system
description: Step 3 of BUILD YOUR BRAND. Auto-select the closest polished design-system preset for a brand, render it as a real, beautiful design-system showcase page (design-system.html) — color swatches, type scale, button states, components, spacing, shadow ramp — and export a machine-readable design-tokens.css the carousel and landing-page steps read. Ships six pre-polished presets and picks one from the brand sheet and voice; the learner never designs or chooses tokens. Use inside BUILD YOUR BRAND, when someone runs /design-system, or whenever a brand needs a complete, safe, rendered design system.
---

# Design system

This is the third link in the BUILD YOUR BRAND chain. You give the brand a complete, polished **design system** — without designing one from scratch and without asking the learner to choose anything — and you render it as a **real, beautiful HTML page**, not a list of tokens. You ship **six pre-built presets**, each a finished token set lifted from production-grade design languages, pick the one that fits, and produce two files in the learner's folder:

1. **`design-system.html`** — a rendered showcase the learner can open and admire.
2. **`design-tokens.css`** — a machine-readable `:root{}` block the next two skills (carousel, landing page) read so everything stays one coherent system.

Because every preset is already polished, the result is always clean; there is no risk of an ugly from-scratch token set.

## First — confirm the working folder

You run in a **new window**, so you don't have the earlier conversation. Open by confirming the working folder ("באיזו תיקייה אנחנו עובדים? אני קורא משם את `brand-sheet.md` ו-`brand-voice.md`"), then read those two files from it. If they aren't there, point the learner back to `start-here` (or the `/start-here` command) rather than inventing a brand.

## The presets

The six presets live in this skill's `presets/` folder. Read them — each documents its archetype, the kind of brand it fits, and a full token set (colors, status colors, typography, radius scale, shadow ramp, spacing):

| file | archetype | fits |
|---|---|---|
| `presets/01-minimal-light.md` | minimal-light | clean, premium, restrained — consultants, studios, productivity |
| `presets/02-dark-developer.md` | dark-developer | technical, modern, products — dev tools, AI, infrastructure |
| `presets/03-editorial-warm.md` | editorial-warm | human, calm, considered — writers, coaches, wellness, boutique |
| `presets/04-enterprise-trust.md` | enterprise-trust | reliable, institutional — finance, B2B, services that sell trust |
| `presets/05-playful-colorful.md` | playful-colorful | friendly, energetic, creative — makers, kids, community, events |
| `presets/06-premium-fintech-purple.md` | premium-fintech-purple | confident, high-end, tech-forward — fintech, SaaS, premium apps |

## How to work

1. **Read `brand-sheet.md` and `brand-voice.md`** from the folder. Pull the audience, the promise, and the mood/personality words.
2. **Match to exactly one preset.** Use the brand's mood and field as the signal — a warm bakery → editorial-warm; a B2B consultancy → enterprise-trust or minimal-light; a dev tool → dark-developer; a kids' brand → playful-colorful; a fintech app → premium-fintech-purple. When two are close, let the mood words break the tie (warm/human vs precise/technical vs playful/energetic).
3. **Render `design-system.html`** from `templates/design-system.template.html`. Fill every `{{...}}` from the chosen preset: the Google Fonts link, the font families, all colors (including `--success`/`--warning`/`--danger`), the radius scale, and the full four-level shadow ramp. At the top, name the chosen archetype and write one Hebrew sentence on why it fit this brand. Keep it RTL-correct and in Hebrew, with no emojis. The page must actually render the swatches, the type scale, the button states, the card/input/badge components, the spacing scale, and the shadow ramp.
4. **Export `design-tokens.css`** — a clean `:root{}` block holding the same token values (colors, status colors, the two `--font-*` families with the Google Fonts URL noted in a comment, the radius scale, the shadow ramp, `--maxw`). This is the contract the carousel and landing-page skills read, so the names must match the template exactly.
5. **Do not invent or blend tokens.** Use the preset as-is so quality stays guaranteed. You may swap **only the accent hue** (`--accent` / `--accent-strong`) if the brand sheet already names a specific brand color — keep the rest of the preset (type, shadows, radius, spacing, structure) intact.
6. **Stay generic and brand-safe.** These presets are generic production-design archetypes. Never pull tokens from any specific client, course, or personal design system — not Benefits Memphis, not a client's brand, not any `_ds` folder. The only source is this `presets/` folder.

## Taste rules baked into every preset (keep them; never break them)

- **No pure black.** The darkest ink is an off-black like `#0f172a` / `#08090a` / `#061b31`, never `#000000`.
- **One muted accent.** A single accent hue, never a neon glow or a second loud color competing with it.
- **Multi-layer tinted shadows.** Every shadow level is two or more layers, tinted toward the brand/neutral hue (for example `rgba(50,50,93,0.12)` plus `rgba(6,27,49,0.08)`), never a single flat pure-black drop.
- **Tight type ramp.** Two or three heading steps, negative letter-spacing on the large sizes, body line-height 1.4–1.6.

## Then — hand off to the next window

When both files are written, **stop**. Offer to open `design-system.html`, then give the transition in plain Hebrew: "מערכת-העיצוב מוכנה — `design-system.html` להסתכל עליו, ו-`design-tokens.css` שהשלבים הבאים קוראים. עכשיו **פתח שיחה חדשה והרץ את `make-branded-carousel`** (או `/carousel`) — הוא יבנה קרוסלה שמשתמשת בדיוק בטוקנים האלה. אחרי זה: `make-landing-page`."

## Why auto-select beats free choice

A non-designer asked to choose colors and fonts will usually produce something inconsistent. By selecting a finished preset and rendering it, every learner's brand looks deliberate, and the whole pack — email, carousel, landing page — inherits one coherent system from `design-tokens.css`. Variety comes from which preset fits, not from improvising tokens.

## Example

The brand sheet says: a one-person bakery, neighbors, mood "warm, homemade, no pretense". You select `03-editorial-warm`, render `design-system.html` with its warm-neutral palette, serif-leaning type, soft radius, and whisper shadow ramp, note "נבחר editorial-warm כי המותג חם, אישי ולא-יומרני", and export the matching `design-tokens.css`.
