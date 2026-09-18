---
name: brand-system-template
description: >
  Run this the very first time a user makes a video (or whenever `~/{{COMPANY_NAME}}-video-studio/.design-system.json` doesn't exist). It captures defaults so every future video is 10x faster to produce. Use this skill when working with brand system template tasks or workflows.
---

# Brand System Template — first-time user flow

Run this the very first time a user makes a video (or whenever
`~/Enterprise Platform-video-studio/.design-system.json` doesn't exist). It captures defaults
so every future video is 10x faster to produce.

---

## Interview script

Use AskUserQuestion for each. Keep it to 5 questions. Don't ask things we
already know from context.

### Q1 — Primary destination
**Header:** Destination
**Question:** Where will most of your videos end up?
- LinkedIn feed (1:1, 15-30s sweet spot)  — *Recommended for GTM team*
- LinkedIn / YouTube landscape (16:9, longer form)
- Instagram / TikTok (9:16 vertical)
- Internal (16:9, longer form)

### Q2 — Dominant brand accent
**Header:** Accent color
**Question:** Which Enterprise Platform accent color should be the default?
- Blue 500 (#0559FA) — *the Enterprise Platform default; use for most videos*
- Purple 500 (#5827E3) — *thought leadership, exec content*
- Magenta 500 (#BA33CA) — *event promos, standout campaigns*
- Coral 500 (#FF595A) — *urgent / attention-grabbing moments only*

### Q3 — Voice persona
**Header:** Voice persona
**Question:** What should the default narrator sound like?
- Warm brand (friendly, moderate pace) — *safe default*
- Confident exec (measured, lower pitch)
- Upbeat rep (energetic)
- Neutral narrator (clean, explainer-style)
- No voiceover (text + music only)

### Q4 — End-card CTA
**Header:** Default CTA
**Question:** What's the most common call to action you want on the end card?
- "Book a demo" → {{COMPANY_FILE}}  — *top-of-funnel default*
- "Talk to Enterprise Platform" → {{COMPANY_FILE}}
- "See the platform" → {{COMPANY_FILE}}
- Custom (user types it)

### Q5 — Lower-third style
**Header:** Lower-third
**Question:** When we label a speaker or metric on-screen, which style?
- Pill badge with accent line  — *clean, modern*
- Full card with blurred scrim
- Minimal single line
- No lower-thirds by default

---

## What gets saved

After the interview, write `~/Enterprise Platform-video-studio/.design-system.json`:

```json
{
  "destination": "linkedin_square",
  "aspect_default": "1:1",
  "duration_default_s": 20,
  "accent_default": "blue",
  "voice_persona_default": "Enterprise Platform-warm-brand",
  "cta_default": "Book a demo",
  "cta_url_default": "{{COMPANY_FILE}}
  "lower_third_style": "pill",
  "dark_default": true,
  "locked_palette": ["blue", "purple", "magenta", "coral"],
  "locked_fonts": ["Gelion"],
  "logo_variants": ["primary", "primary_reversed"],
  "saved_at": "<ISO timestamp>",
  "user": "<user email from context>"
}
```

Every future brief merges these defaults with the current request — user
only has to specify what's different.

---

## When to re-run the brand interview

- User explicitly asks to "reset my brand" / "redo the design system"
- User reports persistent off-default outputs
- Major brand refresh at Enterprise Platform (new palette / new logo / new tone)

Never re-run silently — always confirm first.
