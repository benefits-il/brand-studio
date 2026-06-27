---
name: start-here
description: BUILD YOUR BRAND — the first link in the chain. Ask the learner three easy questions about themselves, then generate a complete, rich set of brand base-documents into a folder they choose, and stop. The later skills (marketing email, design system, carousel, landing page) each run in their own new window and read these files. Use whenever someone installs BUILD YOUR BRAND, runs /start-here, or says "start here" / "תתחיל" / "בוא נתחיל".
---

# BUILD YOUR BRAND — start here

This is the first link in a five-step chain. Your one job here is to take the learner from zero to a **rich set of brand base-documents** — written into a folder they choose, all about **their own world**, never a foreign demo brand. You ask three easy questions, generate the base files, and **stop**. You do not build the email, the design system, the carousel, or the landing page — each of those is a separate skill the learner runs in its **own new window**, and each one reads the files you create here from the working folder.

This window-after-window flow is the point of the lesson: a plugin packages several skills, and they pass state to each other through the **working folder**, not through the conversation. That is cleaner than copy-pasting between windows — the folder *is* the handoff.

The default language of the whole conversation and every output is **Hebrew** (the course is Hebrew), and everything you write must be RTL-correct. If the learner writes to you in English, switch to English. Never mix a Hebrew and an English sentence together. No emojis in the deliverables.

## Step 1 — pick the working folder

Tell the learner, warmly and in one line, what is about to happen: "אני אשאל אותך שלוש שאלות קצרות, ואז אבנה לך את כל קבצי-הבסיס של המותג לתוך תיקייה שתבחר — דף-מותג, קול, ועוד. בשלבים הבאים, כל אחד בחלון נפרד, נהפוך אותם למייל, מערכת-עיצוב, קרוסלה ועמוד-נחיתה."

Then ask **which folder to work in**. Everything you create goes there, and every later skill in the chain reads from there — so the path matters. If they don't have one in mind, offer to create a new folder named after their business (you'll have a name after Step 2) — for example `my-brand/`. Confirm the path before writing anything. Never require a download or upload; you build the files yourself.

## Step 2 — three easy questions (intake)

Ask **three short, easy, general questions** — one at a time, in plain Hebrew. Keep them light; they are not a business interrogation:

1. **מי אתה?**
2. **במה אתה עוסק?**
3. **מה התפקיד שלך?**

Whoever knows what they want — puts it in. **Whoever has no idea — the plugin invents and fills everything automatically, without demanding anything from them.** The generic fallback is a smooth default, not an extra step that adds friction:

- If the learner has no business or is unsure, do not push back and do not make them work for it. Say one easy line — "אין בעיה, אני אמציא לך כיוון שלם ואתה תוכל לערוך אחר כך" — invent a coherent, fitting brand (a name, a field, an audience, a mood) and move straight on.
- If they give you a thin answer ("מורה", "סטארטאפ", "מאפייה"), that is enough — infer a rich, specific world from it. Never stall to collect more.

Three answers — or zero, with you filling in — are enough to build everything. Do not interrogate.

## Step 3 — generate the base-document set, in order

Write the files below into the chosen folder. Each one reads the earlier ones, so the set stays consistent. The starting templates live in this skill's `templates/` folder — read each one and **rewrite it into the learner's own brand** (drop the `.template` from the filename when you save). Make every file genuinely rich and specific to the learner's world — the target depth is the Tuesday brand pack, not thin placeholders. Announce each file in one short line as you create it ("בניתי לך את דף-המותג ←"), so the learner sees the set grow.

1. **`brand-sheet.md`** — the source of truth the rest of the chain reads. From `templates/brand-sheet.template.md`: who they are, what they do and for whom, the brand promise, three or four mood words, a first guess at colors, a simple mark, and a short list of real facts that may be stated in content.
2. **`brand-voice.md`** — a full, reusable voice profile (this folds in what used to be a separate brand-voice skill). From `templates/brand-voice.template.md`: the defining "we sound like ___" sentence, three or four personality adjectives that follow from the mood, tone when explaining / selling / welcoming, vocabulary the brand uses and clichés it avoids, rhythm and structure, two or three do/don't rules, and two short example lines actually written in the voice. The mood words are the anchor — a warm bakery and a precise B2B consultancy must not sound the same. This is the contract every later content skill matches.
3. **`social-seed.md`** — from `templates/social-seed.template.md`: this week's topic, why it fits the brand, three sample post lines that show the voice in action (not finished copy), and a tone cue.
4. **`welcome-points.md`** — from `templates/welcome-points.template.md`: who gets a welcome message, what to welcome them for, the one first step, what NOT to over-promise, a tone cue, and a sign-off. Name the reader's real situation, not just a generic benefit.
5. **`visual-brief.md`** — from `templates/visual-brief.template.md`: the context for one visual asset and a one-line design mandate in the brand's spirit.
6. **`outreach-context.md`** — from `templates/outreach-context.template.md`: who the brand writes to (their real skepticism, not a caricature), the ask, the one key message, a tone cue, and which counter-example it pairs with.
7. **`carousel-outline.md`** — from `templates/carousel-outline.template.md`: a 3-slide arc (the pain → what we offer → how to start), each slide with an on-image headline and a short visual idea, plus a tone cue. The carousel skill reads this later.
8. **`raw/`** — create the folder and write **one counter-example** from `templates/raw/counter-example.template.md`: an intentionally off-voice, corporate-jargon draft about the brand. Every later content skill reads it to extract **facts only, never tone** — it teaches the voice by negative example. (Do not create `character-brief` — there is no video step.)

### What makes the set rich (match this, don't thin it out)
- **Counter-example threading** — the `raw/` draft is referenced by the briefs so later skills know what to rescue from.
- **Psychological framing** — `welcome-points.md` and `outreach-context.md` say *why*, naming the reader's actual situation, not only *what*.
- **Constraints in priority order** — when a brief lists constraints, order them by importance.
- **Right-sized documents** — keep most files under ~30 lines; `brand-voice.md` may run longer because it is the comprehensive reference.

## Step 4 — stop and hand off to the next window

When the base set is written, **stop**. Do not start the email, the design system, the carousel, or the landing page — those are separate skills. List what you created in the folder, then give the learner the transition in plain Hebrew, for example:

"זהו — כל קבצי-הבסיס של המותג שלך בתיקייה. עכשיו **פתח שיחה חדשה והרץ את הסקיל הבא — `write-marketing-email`** (או הפקודה `/marketing-email`). הוא יקרא את התיקייה הזאת וימשיך מאליו. אחר-כך, כל אחד בחלון חדש: `design-system` ← `make-branded-carousel` ← `make-landing-page`."

Tell them why a new window: each step starts fresh and reads the folder, so the context stays clean and nothing gets crowded — that is the chaining principle the plugin is teaching.

## Boundaries

- Build **for** the learner — never make them author a brief, attach a file, or download anything. You generate everything from the three answers, or invent it when they have none.
- Everything is about **their** world, not a demo brand. Do not fall back to a foreign example brand.
- Generate the base set **only**, then stop. The later outputs belong to the later skills, each in its own window.
- Stay consistent: every file reads the brand sheet and the files before it; do not let the voice, colors, or mark drift.
- Hebrew-first, RTL-correct, no emojis in the deliverables, full sentences in one language, directional arrows point left (←).
