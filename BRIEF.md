# A KEEN HOUSE — Website Build Brief

> Master brief for building a website for **A KEEN HOUSE**, a premium specialty coffee + open-sandwich café chain in Bangkok. This file is the entry point — everything else lives in `/data`, `/content`, `/design`, and `/images`.

---

## TL;DR for the AI agent

You are building a marketing website for **A KEEN HOUSE**, a small but premium coffee chain with **4 Bangkok locations** and **47K Instagram followers**. They currently have no real website — only Instagram, Facebook, and a Linktree. The site you build will be presented as a **gift demo** to win them as a paying client (Trojan Horse approach), so quality matters more than completeness. **70% complete and stunning beats 100% complete and mediocre.**

**Goal:** A site that makes the owner think *"this is already better than what we have — we want to launch it."*

---

## Site goals (in priority order)

1. **Show the brand at full strength.** Visuals first. The brand is premium, minimalist, warm. Match that.
2. **Capture pre-visit traffic.** People Googling "best coffee One Bangkok / Paragon / Emsphere" should find them.
3. **Make it easy to visit.** Hours, address, map, and phone for each location must be one tap away.
4. **Funnel to delivery.** LineMan + Grab links per location.
5. **Funnel to social.** Live IG feed embed (their content engine) keeps the site fresh without manual updates.
6. **Sell beans / gift cards / events** (stretch goal — Phase 2).

---

## Recommended sitemap

```
/                       — Home (hero, brand story, locations preview, IG feed, CTA to visit)
/menu                   — Full menu with categories (Coffee, Sandwiches, Desserts)
/locations              — All 4 locations with addresses, hours, maps, delivery links
/locations/one-bangkok  — Per-location landing pages (good for SEO)
/locations/paragon
/locations/emsphere
/locations/sukhumvit40
/about                  — Brand story, philosophy, sourcing
/contact                — LINE, IG, FB, phone, contact form
```

---

## Recommended tech stack

Pick one — both work:

**Option A (recommended for demo speed):**
- Next.js 14 (App Router) + TypeScript
- Tailwind CSS for styling
- Framer Motion for subtle scroll animations
- Deployed on Vercel (preview URL: `akeenhouse.yourdomain.com`)
- Instagram embed via `react-instagram-embed` or oEmbed API
- Google Maps embed (free, no API key needed for `<iframe>`)

**Option B (lower friction for handoff):**
- Astro (faster, less JS, easier to hand to a non-dev later)
- Tailwind CSS
- Same deployment

---

## File map

```
A_KEEN_HOUSE_brief/
├── BRIEF.md                      ← you are here
├── data/
│   ├── brand.json                ← structured brand data (single source of truth)
│   ├── locations.json            ← all 4 locations with addresses, hours, phone, lat/lng
│   └── menu.json                 ← full menu with prices and categories
├── content/
│   ├── about.md                  ← brand story copy in their voice
│   ├── menu.md                   ← menu in human-readable markdown
│   ├── locations.md              ← detailed location info
│   └── reviews.md                ← customer testimonial quotes (sentiment + samples)
├── design/
│   ├── design-system.md          ← colors, type, spacing, voice guidelines
│   └── image-references.md       ← URLs and search queries for sourcing imagery
└── images/                       ← drop downloaded photos here (.gitkeep for now)
```

---

## Build order (suggested)

1. **Read `data/brand.json` first.** Single source of truth for everything.
2. **Read `design/design-system.md`** before writing any CSS — establish the look.
3. Wire up the **homepage** with hero + IG embed + locations grid. Get something gorgeous on screen fast.
4. Build the **menu page** from `data/menu.json`.
5. Build the **locations page** with map embeds from `data/locations.json`.
6. Build the **about page** from `content/about.md`.
7. Polish, mobile QA, deploy to preview URL.

---

## What to source at build time

These weren't downloaded — fetch fresh when building:

- **Photos:** Their Instagram (@akeenhouse) is the design system. Use Instagram oEmbed API or download 8–10 best shots manually. See `design/image-references.md` for direct image search URLs.
- **Live IG feed embed:** Use `<blockquote class="instagram-media">` widget with their handle.
- **Map embeds:** `<iframe>` from Google Maps using each location's address. No API key needed.

---

## What NOT to build (yet)

- Online ordering — they already use LineMan/Grab. Link out to those instead.
- Loyalty program — premature.
- Blog — premature.
- E-commerce (beans, gift cards) — Phase 2 upsell, save for after they sign.

---

## Tone of voice (in 1 sentence)

**Premium but warm. Confident, not pretentious. Crafted, not corporate.** Their existing IG captions are a mix of English and Thai with phrases like "Brewed to Perfection" and "#AKEENSIGNATURE" — read 10–15 of those before writing copy. See `design/design-system.md` for more.

---

## The pitch context (why this matters)

The user is a small Bangkok web agency targeting A KEEN HOUSE as their first paying client. They will send the demo URL via Instagram DM with a note: *"We made you a preview website. Yours to keep. If you'd like us to finish and launch it, let's talk."* The site must look like something the brand owner would be embarrassed to NOT launch.

---

## Source freshness

- **Data scraped:** May 2026
- **Sources:** Google knowledge panel, menustic.com, linktr.ee/akeenhouse, Google Image Search, Wongnai/Trip.com listings
- **Verify before launch:** prices and hours change. Cross-check `data/menu.json` and `data/locations.json` against current sources before pitching.
