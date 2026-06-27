# BUILD YOUR BRAND

Install it, answer three easy questions, and build your brand step by step — window after window — with nothing to download.

This is a Claude plugin. A plugin is the box: it wraps several skills, a couple of sub-agents, slash commands, and a connector, and you install the whole set at once. That packaging is the point of the lesson — and here the skills run as a **chain**, each in its own new window, passing state through a working folder.

## How it works — a five-step chain

You run **start-here**. It asks which folder to work in, asks three easy questions (who you are · what you do · your role), and then generates a **rich set of brand base-documents** into that folder — and stops. From there, each step runs in its **own new window** and reads the folder the previous step wrote:

1. **start-here** → `brand-sheet.md`, `brand-voice.md`, `social-seed.md`, `welcome-points.md`, `visual-brief.md`, `outreach-context.md`, `carousel-outline.md`, and a `raw/` counter-example.
2. **write-marketing-email** → `marketing-email.md` (and optionally a Gmail draft).
3. **design-system** → a rendered `design-system.html` showcase plus a machine-readable `design-tokens.css`.
4. **make-branded-carousel** → a `carousel/` whose slides are locked to those tokens.
5. **make-landing-page** → a self-contained, animated `landing-page.html`.

You never attach or download anything. The working folder is the handoff between windows, so there is no copy-pasting — and everything stays coherent because steps 3–5 all read the same `design-tokens.css`. Everything is about your own world, not a demo brand. If you have no business, the plugin invents a fitting one and fills it in.

## The parts (this is what "a plugin" means)

- **Skills** — `start-here`, `write-marketing-email`, `design-system`, `make-branded-carousel`, `make-landing-page`.
- **Sub-agents** — `content-writer` (the email) and `visual-producer` (the design system, carousel, and landing page).
- **Commands** — `/start-here`, `/marketing-email`, `/design-system`, `/carousel`, `/landing-page` — one per step.
- **Connector** — Higgsfield (images) is bundled in `.mcp.json`; Gmail (email drafts) is a first-party connector you turn on once.

## Install in Cowork — through the UI

Plugins install from the **interface**, not by typing a command. In Cowork:

1. Open **Customize → Plugins**.
2. Under **Personal plugins**, click the **+**.
3. Choose **Add marketplace** and enter `benefits-il/brand-studio`, then **Browse plugins**.
4. Install **BUILD YOUR BRAND**.

> **If "Personal plugins" looks empty and there's no "Add marketplace":** a marketplace only shows up once you already have at least one plugin installed. Install any plugin first (or add the packaged `.zip` from the download page), and the **Add marketplace** option appears. This is a known first-time snag, not a problem with the plugin.

Then turn on the two connectors once, in your Connectors list (claude.ai: **Settings → Connectors** · Cowork: **Customize → Connectors**):
- **Higgsfield** (images): **Add custom connector** → name it `Higgsfield` → paste `https://mcp.higgsfield.ai/mcp` → **Connect** → sign in with a free Higgsfield account (no card, no API key). The plugin already points to this URL in its `.mcp.json`; this sign-in is what authorizes it.
- **Gmail** (email drafts): turn on the built-in connector and sign in. Emails are always saved as a **draft**, never sent.

To start: run **`/start-here`** (or just say "תתחיל"). Each step tells you when to open a new window and run the next one.

## Package the plugin

```
pwsh ./scripts/package.ps1 -Src "plugins/brand-studio" -Name "brand-studio"
```
