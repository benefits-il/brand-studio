---
name: start-here
description: BUILD YOUR BRAND — the one-step start of the plugin. Ask the learner three short questions about themselves, then build a complete personal brand pack (brand sheet, brand voice, design system, marketing email, carousel, landing page) into a folder they choose, with nothing to download. Use whenever someone installs BUILD YOUR BRAND, runs /start-here, or says "start here" / "תתחיל" / "בוא נתחיל".
---

# BUILD YOUR BRAND — start here

This is the front door. The learner just installed the plugin and has nothing prepared. Your job is to take them from zero to a finished, personal brand pack in one guided run, **about their own world** — not a foreign demo brand. You ask three short questions, then you build everything for them into a folder they choose. They never have to attach or download anything; you generate it all.

This run is also the point of the lesson: a plugin packages several skills together. Here you orchestrate five of them in sequence — voice, design system, email, carousel, landing page — from one start.

The default language of the whole conversation and every output is **Hebrew** (the course is Hebrew), and everything you write must be RTL-correct. If the learner writes to you in English, switch to English. Never mix a Hebrew and an English sentence together.

## Step 1 — pick the working folder

Tell the learner, warmly and in one line, what is about to happen: "אני אשאל אותך שלוש שאלות קצרות, ואז אבנה לך חבילת-מותג שלמה — קול, עיצוב, מייל, קרוסלה ועמוד-נחיתה — הכול על העסק שלך, לתוך תיקייה שתבחר."

Then ask **which folder to work in**. Everything you create goes there. If they don't have one in mind, offer to create a new folder named after their business (you'll have the name after Step 2) — for example `my-brand/`. Confirm the path before writing anything. Do not require any download or upload; you build the files yourself.

## Step 2 — three short questions (intake)

Ask **three short, factual questions** — one at a time, in plain Hebrew. Keep them concrete, never psychological:

1. **מי אתה ומה העסק או התפקיד שלך?**
2. **מה אתה עושה, ובשביל מי?**
3. **(לא חובה) פרויקט או הישג אחד שאתה גאה בו?**

Handle the no-business case gracefully:
- If the learner has no business, **offer to invent a fitting business name** for them (propose one or two and let them pick), **or** ask for the name they'd like to use.
- If they're unsure or in a hurry, offer the fallback: **"רוצה שנתקדם עם מידע גנרי? אני אמלא בשבילך וניתן לך לערוך אחר כך."** Then fill reasonable, generic-but-coherent details and move on.

Keep it light. Three answers are enough to build everything; do not interrogate.

## Step 3 — build the brand pack, in order

Now write the files into the chosen folder, in this exact order. Each step reads what the earlier steps produced, so the pack stays consistent. The generic starting templates live in this skill's `templates/` folder — read each one and **rewrite it into the learner's own brand**, saving the result in their folder (drop the `.template` from the name).

1. **`brand-sheet.md`** — fill `templates/brand-sheet.template.md` from the three answers: company facts, what they do and for whom, mood, and a first guess at colors and a mark. This is the source of truth the rest of the chain reads.
2. **`brand-voice.md`** — invoke the **build-brand-voice** skill on the brand sheet (it derives the voice from the answers; the learner has no writing samples). The result captures how their brand sounds.
3. **`design-system.md`** — invoke the **select-design-system** skill. It reads the brand sheet and voice, **auto-selects** the closest of the bundled polished presets, and writes a complete personal token set (colors, type, radius, shadows, spacing). The learner does not choose or design anything.
4. **`marketing-email.md`** — auto-draft a short brief from the brand sheet (what to promote, to whom, one ask), then invoke the **write-marketing-email** skill. It writes a marketing email in their voice into the folder, and offers to also save it as a Gmail draft if Gmail is connected.
5. **`carousel/`** — auto-draft a `carousel-outline.md` (3 slides: the problem, what they offer, how to start) from the brand sheet, then invoke the **make-branded-carousel** skill, pointing it at `brand-sheet.md`, `design-system.md`, and the outline. It locks one visual system and produces the slides. (Live image generation needs the Higgsfield connector; if it isn't connected yet, save the precise per-slide prompts and tell the learner how to connect.)
6. **`landing-page.html`** — invoke the **make-landing-page** skill. It builds a self-contained, RTL-correct HTML landing page from `design-system.md`, `brand-voice.md`, and `brand-sheet.md`.

Announce each file as you create it in one short line ("בניתי לך את הקול ←"), so the learner sees the pack growing.

## Step 4 — offer to peek inside

When the pack is built, list what's in their folder and **offer to peek**: "רוצה להציץ במה שיצרנו? אני יכול לפתוח לך את עמוד-הנחיתה, או להראות לך את הקול שלך." Open or show whatever they ask for. Close with one line on what they can do next (edit any file, re-run a single step, or connect Higgsfield to render the carousel images).

## Boundaries

- Build **for** the learner — never make them author a brief, attach a file, or download a pack. You generate everything from the three answers.
- Everything is about **their** world, not a demo brand. Do not fall back to a foreign example brand.
- Stay consistent: every step reads the brand sheet and the files before it. Do not let the voice, colors, or mark drift between outputs.
- Hebrew-first, RTL-correct, no emojis in the deliverables, full sentences in one language.
