# Brand Studio

One plugin. Five jobs. Any brand.

`brand-studio` is a Claude plugin that turns a brand's raw drafts and rough briefs into finished, on-brand work. You give it a brand pack — a brand sheet, a set of voice guidelines, and the messy "before" materials — and it produces the polished "after": emails, social posts, a carousel, a character video.

It carries no brand of its own. Point it at one brand pack and it works for that brand; swap in another and it works for that one instead. The brand is data you attach, never anything baked into the code.

## The four parts (this is the whole point)

A plugin is the box. It wraps the other three.

- **Skills** — five of them, one per job. The method.
- **Sub-agents** — two of them. The personas that do the work: `content-writer` and `visual-producer`.
- **Commands** — five slash commands. The buttons you press.
- **Connector** — the door to an outside service. This plugin bundles one (Higgsfield, for images and video) and uses one you already have (Gmail).

## The five jobs

| Command | Job | Agent | Connector |
|---|---|---|---|
| `/outreach` | An outreach email, drafted in the brand's voice | content-writer | Gmail (draft) |
| `/welcome` | A branded welcome email | content-writer | Gmail (draft) |
| `/post` | An Instagram post or reel — image plus caption | visual-producer + content-writer | Higgsfield (image) |
| `/carousel` | A multi-slide branded carousel | visual-producer | Higgsfield (image) |
| `/reel` | A short AI-character video | visual-producer | Higgsfield (video) |

## Install

In Cowork: **Customize → Personal plugins**.

- From this marketplace: `/plugin marketplace add benefits-il/brand-studio` then `/plugin install brand-studio@brand-studio`.
- Or add the packaged plugin folder directly (the `.zip` from the download page).

## The two connectors

This plugin has two connectors, wired two different ways — that difference is itself worth seeing.

- **Higgsfield (images and video)** — the plugin points to it in `.mcp.json` (`https://mcp.higgsfield.ai/mcp`). Add it once as a connector: **Settings → Connectors** (claude.ai) or **Customize → Connectors** (Cowork) → **Add custom connector** → name it `Higgsfield` → paste `https://mcp.higgsfield.ai/mcp` → **Connect** → sign in with a free Higgsfield account (no card, no API key; your account credits apply). The free tier gives a basic model with a watermark. The lever for good output on the free tier is a fully precise prompt — exactly what `visual-producer` builds for you from the brand sheet. Clean, watermark-free, HD output is an optional Higgsfield subscription (~$15/month).
- **Gmail (email drafts)** — not in the plugin. Gmail is a first-party connector you turn on once in **Customize → Connectors → Gmail** (a normal sign-in). The email commands always create a *draft* — they never send.

## How the brand gets in

The plugin reads what you attach, never a brand baked into the code:

- `brand-voice.md` — the voice guidelines. The writing voice comes from here. (Create it from your own materials with a voice plugin such as `brand-voice`, or write it by hand.)
- `brand-sheet.md` — colors, mark, and company facts.
- the raw "before" materials and per-job briefs — what each command turns into a finished piece.

Attach the relevant files for the job, then run the command. The same plugin works for any brand whose pack you hand it.
