# Image References & Sourcing Guide

> Direct links to image sources. The agent should fetch these into `/images/` at build time, OR embed live (Instagram feed) where possible. Most are public — verify usage rights before final launch.

---

## Primary source: Instagram (@akeenhouse)

The 47K-follower IG feed is the visual identity. Pull from here first.

- **Profile URL:** https://www.instagram.com/akeenhouse/
- **Approach:** Use the Instagram **oEmbed** endpoint for live embedding (preserves rights and freshness):
  ```
  https://api.instagram.com/oembed/?url=https://www.instagram.com/p/{POST_ID}/
  ```
- **Or use a free embed widget:** [LightWidget](https://lightwidget.com/) generates a clean Instagram feed embed with no backend.
- **Or scrape statically (one-time):** When auth-walled, use a free tool like [SocialBu's IG viewer](https://socialbu.com/tools/free-instagram-viewer) or pull from Google Image Search results (see below).

## Google Image Search — bulk visuals

Direct URLs to image search result pages — the search results contain dozens of public photos of all four locations:

- **All locations:** https://www.google.com/search?q=%22A+KEEN+HOUSE%22+%22One+Bangkok%22&udm=2
- **One Bangkok specifically:** https://www.google.com/search?q=%22A+KEEN+HOUSE%22+%22One+Bangkok%22+interior&udm=2
- **Paragon location:** https://www.google.com/search?q=%22A+KEEN+HOUSE%22+Paragon&udm=2
- **Emsphere location:** https://www.google.com/search?q=%22A+KEEN+HOUSE%22+Emsphere&udm=2
- **Sukhumvit 40 location:** https://www.google.com/search?q=%22A+KEEN+HOUSE%22+Sukhumvit+40&udm=2
- **Signature drinks:** https://www.google.com/search?q=%22A+KEEN+HOUSE%22+%22Burnt+Caramel+Latte%22&udm=2
- **Open sandwiches:** https://www.google.com/search?q=%22A+KEEN+HOUSE%22+sandwich+brekkie&udm=2

## Google Maps — customer photos

Each location's Google Maps listing has a "Photos" tab with hundreds of customer-submitted images, including menu boards and dishes:

- **One Bangkok photos:** Search "A KEEN HOUSE One Bangkok" on Google Maps → click the listing → "Photos" tab
- These are perfect for: menu items, ambient interior, exterior, queue/foot traffic shots

## Wongnai

Thai food review platform with structured listings and photos:

- https://www.wongnai.com/businesses?keyword=A+KEEN+HOUSE

## Trip.com / TripAdvisor / Wanderlog

Tourist-facing aggregators with editorial photos:

- https://wanderlog.com/place/details/a-keen-house

## Logo asset

- **Source:** Their Instagram profile picture is the cleanest version of the monogram-only logo.
  https://www.instagram.com/akeenhouse/ → profile pic
- **Linktree:** https://linktr.ee/akeenhouse → also has the monogram as the avatar
- **Workflow:** Open the IG profile in Chrome, right-click the profile picture → "Open image in new tab" → save. Or use a free IG profile pic downloader (search "instagram profile picture viewer").
- **Format needed:** SVG ideally (recreate by tracing in Figma if needed). Failing that, 512×512 PNG with transparent background.

## Required image inventory for the demo

What the build needs at minimum:

| Slot                          | Quantity | Notes                                                |
|-------------------------------|---------:|------------------------------------------------------|
| Hero (homepage)               | 1        | Wide interior or counter shot, dramatic lighting     |
| Location cards (one per)      | 4        | Distinct hero per location, each landscape           |
| Signature drink showcase      | 2-3      | Burnt Caramel Latte close-up + 1-2 others            |
| Sandwich showcase             | 2        | Classic Brekkie + one mushroom variant               |
| About page narrative          | 2-3      | One interior, one product, one barista-at-work       |
| Footer / texture background   | 1        | Subtle wood-grain or bokeh interior shot             |
| Favicon (logo monogram)       | 1        | 512×512 transparent PNG or SVG                       |
| Open Graph / social share     | 1        | 1200×630, the most striking interior shot            |

**Total:** ~14-17 images.

## Stretch — short video clips

If you want extra polish:
- TikTok user-generated content has slow-mo coffee pours: https://www.tiktok.com/search?q=akeenhouse
- 3-5 second loops embedded in hero sections feel premium

## Image optimization checklist for production

- [ ] Compress all hero images to <300KB JPEG or <150KB AVIF
- [ ] Generate 3 sizes per image (mobile / tablet / desktop) using Next.js Image or Astro `<Image>`
- [ ] Lazy-load below-the-fold imagery
- [ ] Use `loading="eager" fetchpriority="high"` on the hero image only

## ⚠️ Rights / fair use note

For the **demo / pitch**, using their public photos is reasonable — it's their own brand content being used to sell them a website. Flag this in the pitch: *"the demo uses your existing Instagram photos as placeholders — we'll commission new shoots if you'd like."*

Once the contract is signed, the production site should use:
- Photos provided directly by A KEEN HOUSE, OR
- A new commissioned photoshoot, OR
- Continued use of their IG content with explicit permission documented in the contract.
