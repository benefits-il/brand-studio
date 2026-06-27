# BUILD YOUR BRAND

Install it, answer three short questions about yourself, and get a full personal brand pack — built for you, into a folder you choose, with nothing to download.

This is a Claude plugin. A plugin is the box: it wraps several skills, a couple of sub-agents, slash commands, and a connector, and you install the whole set at once. That packaging is the point of the lesson — and **start-here** shows it live by running five of those skills in sequence.

## What it does

You run **start-here**. It asks which folder to work in, asks three short questions (who you are · what you do and for whom · a project you're proud of), and then builds your brand pack into that folder, in order:

1. `brand-sheet.md` — your facts, filled from your answers.
2. `brand-voice.md` — how your brand sounds (built from your answers, no writing samples needed).
3. `design-system.md` — a polished design system, auto-picked from six presets to fit you.
4. `marketing-email.md` — a short marketing email in your voice (optionally also a Gmail draft).
5. `carousel/` — a branded multi-slide carousel.
6. `landing-page.html` — a self-contained landing page in your design and voice.

You never attach or download anything. Everything is about your own world, not a demo brand.

## The parts (this is what "a plugin" means)

- **Skills** — `start-here` (the orchestrator) plus `build-brand-voice`, `select-design-system`, `write-marketing-email`, `make-branded-carousel`, `make-landing-page`, and the original `write-outreach-email`, `write-welcome-email`, `make-social-post`, `make-character-video`.
- **Sub-agents** — `content-writer` and `visual-producer`.
- **Commands** — `/start-here` is the front door. `/outreach`, `/welcome`, `/post`, `/carousel`, `/reel` stay available as individual jobs.
- **Connector** — Higgsfield (images and video) is bundled in `.mcp.json`; Gmail (email drafts) is a first-party connector you turn on once.

## Install in Cowork — through the UI

Plugins install from the **interface**, not by typing a command. In Cowork:

1. Open **Customize → Plugins**.
2. Under **Personal plugins**, click the **+**.
3. Choose **Add marketplace** and enter `benefits-il/brand-studio`, then **Browse plugins**.
4. Install **BUILD YOUR BRAND**.

> **If "Personal plugins" looks empty and there's no "Add marketplace":** a marketplace only shows up once you already have at least one plugin installed. Install any plugin first (or add the packaged `.zip` from the download page), and the **Add marketplace** option appears. This is a known first-time snag, not a problem with the plugin.

Then turn on the two connectors once, in your Connectors list (claude.ai: **Settings → Connectors** · Cowork: **Customize → Connectors**):
- **Higgsfield** (images and video): **Add custom connector** → name it `Higgsfield` → paste `https://mcp.higgsfield.ai/mcp` → **Connect** → sign in with a free Higgsfield account (no card, no API key). The plugin already points to this URL in its `.mcp.json`; this sign-in is what authorizes it.
- **Gmail** (email drafts): turn on the built-in connector and sign in. Emails are always saved as a **draft**, never sent.

To start: run **`/start-here`** (or just say "תתחיל").

## Package the plugin

```
pwsh ./scripts/package.ps1 -Src "plugins/brand-studio" -Name "brand-studio"
```
