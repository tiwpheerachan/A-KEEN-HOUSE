# Design System — A KEEN HOUSE

> Visual identity guidelines extracted from their Instagram, storefront photos, and packaging. Build the site to feel like a natural extension of the IG feed.

---

## Color palette

Derived from interior photography and packaging.

```
PRIMARY
--ink-deep:      #0E1116    Near-black with a hint of blue. Use for headlines, navigation, primary text.
--ink:           #1A1D22    Body text on light backgrounds.

WARM NEUTRALS (the heart of the brand)
--cream:         #F4EFE6    Off-white background — softer than pure white.
--sand:          #E8DFD0    Slightly deeper warm neutral, for sections and dividers.
--clay:          #B8946B    Warm wood tone, lifted from interior wood paneling.

ACCENT
--coffee:        #4A2C1F    Deep espresso brown. Use sparingly — outlines, drop caps.
--gold-warm:     #C8923B    Lifted from interior lighting. Reserve for highlights only.

UI / FUNCTIONAL
--success:       #4A6B3A    Muted green — matches the natural palette, not bright.
--line:          #D9CFC0    Subtle dividers and card outlines.
--shadow:        rgba(20, 16, 10, 0.08)
```

**Background hierarchy:** `--cream` is the default page background. White is too clinical. Pure black is too harsh — use `--ink-deep` instead.

## Typography

Build for editorial-meets-modern. Two-font system:

```
HEADLINES & DISPLAY
"Fraunces", serif         (Google Fonts, free)
or "Playfair Display", serif (alternative)
Weight: 600-700 for display, 500 for sub-display
Letter-spacing: -0.01em on large sizes

BODY & UI
"Inter", sans-serif       (Google Fonts, free)
Weight: 400 body, 500 strong, 600 nav
```

**Why Fraunces:** It's modern serif with subtle warmth — matches the premium-but-warm brand. Free on Google Fonts. Variable font keeps the bundle small.

**For Thai content:** Pair with **"IBM Plex Sans Thai"** for body and **"Noto Serif Thai"** for display. Both free on Google Fonts.

## Type scale

```
Display 1:  64-72px    line-height: 1.05    letter-spacing: -0.02em
Display 2:  48-56px    line-height: 1.1     letter-spacing: -0.01em
H1:         36-40px    line-height: 1.2
H2:         28-32px    line-height: 1.25
H3:         22-24px    line-height: 1.3
Body lg:    18px       line-height: 1.6
Body:       16px       line-height: 1.65
Small:      14px       line-height: 1.55
Caption:    12px       line-height: 1.45     letter-spacing: 0.06em (uppercase)
```

## Spacing & layout

- **Base unit:** 8px
- **Section padding (desktop):** 96px top/bottom (12 units)
- **Section padding (mobile):** 56px top/bottom
- **Container max-width:** 1280px (with 32px gutter)
- **Reading column:** 680px max for body copy
- **Generous whitespace** is the brand. Don't crowd elements.

## Visual motifs

These show up consistently in their interiors and content. Pull them into the site design:

1. **Vertical lines / striated textures** — backgrounds, dividers, image overlays. The shop walls have vertical wood/metal slats; mirror this with subtle vertical hairline rules.
2. **Dramatic warm lighting** — use generous warm-tinted gradients on hero sections; avoid cool blues anywhere.
3. **Counter / bar-style imagery** — wide horizontal photos work better than vertical. Use 16:9 or wider crops.
4. **Coffee-cup-as-hero** — close-up product shots are their best content. Build at least one section that frames a single drink as the focal point.
5. **Type-on-photo** — they use text overlays on dark interior shots. Build a hero treatment that supports this.

## Imagery direction

- **Avoid stock photos at all costs.** Use only their own IG content, customer photos from Google reviews, or commission shots.
- **Warm tones only.** Anything cool-blue should be color-graded warmer.
- **Negative space.** A coffee cup with two-thirds dark background is more on-brand than a cluttered shot.
- **People rarely featured.** Their content focuses on product and space, not customer faces. Match this.

## Logo usage

- The logo is "A KEEN" wordmark + a triangular/angular "K" monogram.
- Use the full wordmark in nav and footer.
- Use the monogram alone for favicon, small spaces, and as a watermark on hero images.
- Always reproduce in `--ink-deep` on light backgrounds, or `--cream` on dark.
- Source the actual logo from their Instagram profile picture or Linktree.

## Motion & interactivity

- **Subtle.** Slow fade-ins on scroll, no bouncy springs.
- **Framer Motion settings:** `duration: 0.6`, `ease: "easeOut"`, `delay: 0.05–0.15` on staggered items.
- **Parallax:** Light parallax on hero images is acceptable — keep it under 30% movement.
- **Hover states:** Underline on nav, slight scale (1.02) on cards, color shift to `--coffee` on links. No flashy hover effects.

## Accessibility checklist

- [ ] Color contrast ≥ 4.5:1 for body text, 3:1 for large text — verify `--clay` on `--cream` (probably needs adjustment for body)
- [ ] All images have alt text describing the content
- [ ] Map embeds have a text fallback (the address)
- [ ] All interactive elements are keyboard-navigable
- [ ] Focus states visible — use a 2px outline in `--coffee`
- [ ] Thai language attribute set on Thai content blocks

## Voice in microcopy

| Element              | Avoid                          | Prefer                                |
|----------------------|--------------------------------|---------------------------------------|
| Order delivery CTA   | "Order Now!"                   | "Order via LineMan →"                 |
| Visit CTA            | "Find a location"              | "Find your nearest →"                 |
| 404 page             | "Oops, page not found!"        | "This shelf is empty. Browse coffee →"|
| Newsletter           | "Subscribe for updates!"       | "Quiet emails about new menus."       |
| Loading state        | "Loading..."                   | "Brewing..."                          |
