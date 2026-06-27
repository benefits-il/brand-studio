# BUILD YOUR BRAND — a Cowork plugin

Install it, answer three easy questions, and build your brand step by step — window after window. Each step reads and writes the same working folder, so the brand stays coherent: a rich set of base documents, a marketing email, a polished design system, a branded carousel, and an animated landing page, with nothing to download. This repo is the marketplace and the landing page.

> Built for the Benefits AI course plugin-building unit. The learner installs one plugin and runs its skills as a chain — each in its own new window — on their own brand. The internal engine is brand-agnostic and stays named `brand-studio`; the learner-facing name is **BUILD YOUR BRAND**.

## What's here

- `index.html` — the landing page (also the GitHub Pages site).
- `.claude-plugin/marketplace.json` — the marketplace registry. Add this repo as a marketplace in Cowork.
- `plugins/brand-studio/` — the plugin: five chain skills (`start-here`, `write-marketing-email`, `design-system`, `make-branded-carousel`, `make-landing-page`); two sub-agents (`content-writer`, `visual-producer`); slash commands; and an image connector.
- `dist/` — the packaged plugin download.

## Install in Cowork — through the UI

Plugins install from the **interface**, not by typing a command:

1. Open **Customize → Plugins**.
2. Under **Personal plugins**, click the **+**, choose **Add marketplace**, enter `benefits-il/brand-studio`, then **Browse plugins**.
3. Install **BUILD YOUR BRAND**.

> **If "Personal plugins" looks empty and there's no "Add marketplace":** a marketplace only appears once at least one plugin is already installed. Install any plugin first (or add the packaged `.zip` from the download page), and the **Add marketplace** option shows up. Known first-time snag, not a plugin problem.

Then add the two connectors once, in your Connectors list. **Higgsfield** (images): **Add custom connector** → name it `Higgsfield` → paste `https://mcp.higgsfield.ai/mcp` → **Connect** → sign in with a free account (the plugin already points to this URL in its `.mcp.json`). **Gmail** (email drafts): turn on the built-in connector and sign in. To begin, run **`/start-here`**.

## The chain — five steps, window after window

Each step runs in its own new window and reads the working folder the previous step wrote.

| Step | Command | What it does | Output in your folder |
|---|---|---|---|
| 1 | `/start-here` | three easy questions → all the base documents | `brand-sheet.md`, `brand-voice.md`, `social-seed.md`, `welcome-points.md`, `visual-brief.md`, `outreach-context.md`, `carousel-outline.md`, `raw/` |
| 2 | `/marketing-email` | a marketing email in your voice | `marketing-email.md` (+ optional Gmail draft) |
| 3 | `/design-system` | auto-picks a polished design system, renders it, exports tokens | `design-system.html` + `design-tokens.css` |
| 4 | `/carousel` | a branded carousel locked to those tokens | `carousel/` |
| 5 | `/landing-page` | a self-contained, animated landing page | `landing-page.html` |

Each step ends by telling you to open a new window and run the next one. The working folder *is* the handoff — no copy-pasting between windows.

## Package the plugin

```
pwsh ./scripts/package.ps1 -Src "plugins/brand-studio" -Name "brand-studio"
```
