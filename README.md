# Brand Studio — a generic content plugin for Cowork

One plugin, five jobs, any brand. Hand it a brand pack — a brand sheet, voice guidelines, and a brief — and it produces finished, on-brand work: emails, social posts, a carousel, an AI-character video. It carries no brand of its own. This repo is the marketplace and the landing page.

> Built for the Benefits AI course (unit 3.2 — what a plugin is) as the generic engine learners install and point at any brand pack. The Tuesday brand pack and demo page live in a separate repo (`benefits-il/tuesday`).

## What's here

- `index.html` — the landing page (also the GitHub Pages site).
- `.claude-plugin/marketplace.json` — the marketplace registry. Add this repo as a marketplace in Cowork.
- `plugins/brand-studio/` — the plugin: a generic studio that does five jobs. Reads a brand pack you give it. Bundles five skills, two sub-agents (`content-writer`, `visual-producer`), five `/` commands, and an image/video connector.
- `dist/` — the packaged plugin download.

## Install in Cowork

In Cowork, open `/plugin` and run:

```
/plugin marketplace add benefits-il/brand-studio
/plugin install brand-studio@brand-studio
```

The name after `@` is this marketplace's `name` field. For a local test before the repo is public, point `add` at the folder path.

Two connectors. Add each once in your Connectors list. **Higgsfield** (image and video): **Add custom connector** → name it `Higgsfield` → paste `https://mcp.higgsfield.ai/mcp` → **Connect** → sign in with a free account (the plugin already points to this URL in its `.mcp.json`). **Gmail** (email drafts): turn on the built-in connector and sign in. Then attach a brand pack (a brand sheet, voice guidelines, and a brief) before running a command.

## The five jobs

| Command | Job | Agent | Connector |
|---|---|---|---|
| `/outreach` | Outreach email, drafted in Gmail | content-writer | Gmail |
| `/welcome` | Branded welcome email | content-writer | Gmail |
| `/post` | Instagram post or reel — image plus caption | visual-producer + content-writer | Higgsfield |
| `/carousel` | Multi-slide branded carousel | visual-producer | Higgsfield |
| `/reel` | Short AI-character video | visual-producer | Higgsfield |

## Package the plugin

```
pwsh ./scripts/package.ps1 -Src "plugins/brand-studio" -Name "brand-studio"
```
