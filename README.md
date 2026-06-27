# BUILD YOUR BRAND — a Cowork plugin

Install it, answer three short questions about yourself, and get a full personal brand pack — brand voice, a polished design system, a marketing email, a branded carousel, and a self-contained landing page — built for you into a folder you choose, with nothing to download. This repo is the marketplace and the landing page.

> Built for the Benefits AI course (unit 3.2 — what a plugin is). The learner installs one plugin and watches it run several skills in sequence on their own brand. The internal engine is brand-agnostic and stays named `brand-studio`; the learner-facing name is **BUILD YOUR BRAND**.

## What's here

- `index.html` — the landing page (also the GitHub Pages site).
- `.claude-plugin/marketplace.json` — the marketplace registry. Add this repo as a marketplace in Cowork.
- `plugins/brand-studio/` — the plugin: a `start-here` orchestrator plus skills for voice, design-system, email, carousel, video, and a landing page; two sub-agents (`content-writer`, `visual-producer`); slash commands; and an image/video connector.
- `dist/` — the packaged plugin download.

## Install in Cowork — through the UI

Plugins install from the **interface**, not by typing a command:

1. Open **Customize → Plugins**.
2. Under **Personal plugins**, click the **+**, choose **Add marketplace**, enter `benefits-il/brand-studio`, then **Browse plugins**.
3. Install **BUILD YOUR BRAND**.

> **If "Personal plugins" looks empty and there's no "Add marketplace":** a marketplace only appears once at least one plugin is already installed. Install any plugin first (or add the packaged `.zip` from the download page), and the **Add marketplace** option shows up. Known first-time snag, not a plugin problem.

Then add the two connectors once, in your Connectors list. **Higgsfield** (image and video): **Add custom connector** → name it `Higgsfield` → paste `https://mcp.higgsfield.ai/mcp` → **Connect** → sign in with a free account (the plugin already points to this URL in its `.mcp.json`). **Gmail** (email drafts): turn on the built-in connector and sign in. To begin, run **`/start-here`**.

## What start-here builds

| Step | File in your folder |
|---|---|
| brand sheet | `brand-sheet.md` |
| brand voice | `brand-voice.md` |
| design system (auto-picked from 6 presets) | `design-system.md` |
| marketing email | `marketing-email.md` (+ optional Gmail draft) |
| branded carousel | `carousel/` |
| landing page | `landing-page.html` |

The individual jobs stay available as commands: `/outreach`, `/welcome`, `/post`, `/carousel`, `/reel`.

## Package the plugin

```
pwsh ./scripts/package.ps1 -Src "plugins/brand-studio" -Name "brand-studio"
```
