# A KEEN HOUSE — Website Build Brief

A complete, structured brief for an AI agent (Claude Code, Cursor, etc.) to build a marketing website for **A KEEN HOUSE**, a premium specialty coffee chain with 4 locations in Bangkok.

## Quick start

1. Read `BRIEF.md` first — it's the master overview.
2. Read `design/design-system.md` before writing CSS.
3. Pull structured data from `data/*.json` — single source of truth.
4. Pull copy from `content/*.md`.
5. Source imagery using `design/image-references.md`.

## File index

```
.
├── README.md                   ← you are here
├── BRIEF.md                    ← master brief (start here)
│
├── data/                       ← structured data (machine-readable)
│   ├── brand.json
│   ├── locations.json
│   └── menu.json
│
├── content/                    ← human-authored copy
│   ├── about.md
│   ├── menu.md
│   ├── locations.md
│   └── reviews.md
│
├── design/                     ← visual identity & sourcing
│   ├── design-system.md
│   └── image-references.md
│
└── images/                     ← drop image files here as you fetch them
    └── .gitkeep
```

## Recommended prompt to start an AI agent build

> Read `BRIEF.md`, `data/brand.json`, and `design/design-system.md` first. Then build a Next.js + Tailwind marketing site for A KEEN HOUSE. Start with the homepage — hero, brand story, locations grid, IG embed, footer. The site is a Trojan Horse demo to win them as a paying client, so quality matters more than completeness. Use their cream + ink-deep + warm wood palette per the design system. Do not invent facts — if data isn't in the JSON, mark it as TBD or omit it.

## Source freshness

Brief generated: **2026-05-11**. Verify menu prices and hours against current sources before pitching the demo.
# A-KEEN-HOUSE
