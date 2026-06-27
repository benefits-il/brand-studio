---
name: select-design-system
description: Auto-select the closest polished design-system preset for a brand and write it as the brand's own design-system.md (colors, typography, radius, shadows, spacing). Ships six generic, pre-polished presets and picks one from the brand sheet and voice — the learner never designs or chooses tokens. Use inside BUILD YOUR BRAND, or whenever a brand needs a complete, safe token set without building one from scratch.
---

# Select a design system

You give a brand a complete, polished **design system** without designing one from scratch and without asking the learner to choose. You ship **six pre-built presets** — each a finished token set lifted from production-grade design languages — and you pick the one that best fits the brand, then write it as the brand's own `design-system.md`. Because every preset is already polished, the result is always clean; there is no risk of an ugly from-scratch token set.

## The presets

The six presets live in this skill's `presets/` folder. Read them — each documents its archetype, the kind of brand it fits, and a full token set:

| file | archetype | fits |
|---|---|---|
| `presets/01-minimal-light.md` | minimal-light | clean, premium, restrained — consultants, studios, productivity |
| `presets/02-dark-developer.md` | dark-developer | technical, modern, products — dev tools, AI, infrastructure |
| `presets/03-editorial-warm.md` | editorial-warm | human, calm, considered — writers, coaches, wellness, boutique |
| `presets/04-enterprise-trust.md` | enterprise-trust | reliable, institutional — finance, B2B, services that sell trust |
| `presets/05-playful-colorful.md` | playful-colorful | friendly, energetic, creative — makers, kids, community, events |
| `presets/06-premium-fintech-purple.md` | premium-fintech-purple | confident, high-end, tech-forward — fintech, SaaS, premium apps |

## How to work

1. **Read `brand-sheet.md` and `brand-voice.md`.** Pull the audience, the promise, and the mood/personality words. If neither exists yet, ask for the three intake answers and infer from those.
2. **Match to one preset.** Use the brand's mood and field as the signal — a warm bakery → editorial-warm; a B2B consultancy → enterprise-trust or minimal-light; a dev tool → dark-developer; a kids' brand → playful-colorful; a fintech app → premium-fintech-purple. Pick exactly one. When two are close, let the mood words break the tie (warm/human vs precise/technical vs playful/energetic).
3. **Write `design-system.md`** by filling the design-system template with that preset's exact token values — colors, typography (with the Google Fonts link), radius, shadows, spacing. At the top, name the chosen archetype and write one sentence on why it fit this brand.
4. **Do not invent or blend tokens.** Use the preset as-is so quality stays guaranteed. You may swap only the accent hue if the brand sheet already names a specific brand color — keep the rest of the preset (type, shadows, spacing, structure) intact.
5. **Stay generic and brand-safe.** These presets are generic production-design archetypes. Never pull tokens from any specific client, course, or personal design system; the only source is this `presets/` folder.

## Why auto-select beats free choice

A non-designer asked to choose colors and fonts will usually produce something inconsistent. By selecting a finished preset, every learner's brand looks deliberate, and the whole pack — email, carousel, landing page — inherits one coherent system. Variety comes from which preset fits, not from improvising tokens.

## Example

The brand sheet says: a one-person bakery, neighbors, mood "warm, homemade, no pretense". You select `03-editorial-warm`, write its warm-neutral palette, serif-leaning type, soft radius, and whisper shadows into `design-system.md`, and note "נבחר editorial-warm כי המותג חם, אישי ולא-יומרני".
