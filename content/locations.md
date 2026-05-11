# Locations — Human-Readable

> Mirrors `data/locations.json` for content authoring. Four locations across Bangkok.

---

## A KEEN HOUSE — One Bangkok *(flagship)*

The newest and most prominent location, on the 3rd floor of the Parade Building inside the One Bangkok mega-development.

- **Address:** One Bangkok, 3rd Floor, Parade Building, 1877 Rama IV Rd, Lumphini, Pathum Wan, Bangkok 10330
- **Phone:** 085 909 0770
- **Hours:** Daily, 10:00 AM – 8:00 PM
- **Google rating:** 4.9 ★ (544 reviews)
- **Best for:** Pre/post shopping coffee, business meetings, premium afternoon
- **Delivery:** LineMan, Grab

---

## A KEEN HOUSE — Paragon

Inside Siam Paragon's Nextopia zone on the 5th floor — heart of the Siam shopping district.

- **Address:** Nextopia, 5th Floor, 991 Rama I Rd, Pathum Wan, Bangkok 10330
- **Phone:** *Verify before launch*
- **Hours:** Likely 10:00 AM – 9:00 PM (matches mall hours — verify)
- **Best for:** Tourists, shoppers, BTS-accessible meetings
- **Delivery:** LineMan

---

## A KEEN HOUSE — Emsphere

Inside the new Emsphere development on Sukhumvit Road, EM District.

- **Address:** Emsphere, 628 Sukhumvit Rd, Khlong Tan, Khlong Toei, Bangkok
- **Phone:** *Verify before launch*
- **Hours:** Likely 10:00 AM – 10:00 PM (matches mall hours — verify)
- **Best for:** Sukhumvit professionals, dinner-adjacent crowd, post-Emsphere shopping
- **Delivery:** LineMan

---

## A KEEN HOUSE — Sukhumvit 40 *(original)*

The original standalone shop on Soi Sukjai. Different feel from the mall locations — more "home café" per customer reviews. Likely the most loyal regular crowd.

- **Address:** 4 Soi Sukjai, Sukhumvit 40, Phra Khanong, Khlong Toei, Bangkok 10110
- **Phone:** +66 99 436 6535
- **Hours:** Daily, 9:00 AM – 5:30 PM
- **Best for:** Quiet weekday work, brunch, the regulars
- **Delivery:** LineMan, Grab

---

## Map embed pattern

For each location, use this iframe (no API key required):

```html
<iframe
  src="https://www.google.com/maps?q={URL_ENCODED_FULL_ADDRESS}&output=embed"
  width="100%"
  height="400"
  style="border:0;"
  allowfullscreen=""
  loading="lazy"
  referrerpolicy="no-referrer-when-downgrade">
</iframe>
```

## Click-to-call pattern

```html
<a href="tel:+66859090770">085 909 0770</a>
```

## Directions pattern

```html
<a href="https://www.google.com/maps/dir/?api=1&destination={URL_ENCODED_FULL_ADDRESS}">
  Get directions
</a>
```

## Hours data — schema.org snippet (per location)

```json
{
  "@context": "https://schema.org",
  "@type": "CafeOrCoffeeShop",
  "name": "A KEEN HOUSE — One Bangkok",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "3rd Floor, Parade Building, 1877 Rama IV Rd",
    "addressLocality": "Pathum Wan",
    "addressRegion": "Bangkok",
    "postalCode": "10330",
    "addressCountry": "TH"
  },
  "telephone": "+66859090770",
  "openingHours": "Mo-Su 10:00-20:00",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": 4.9,
    "reviewCount": 544
  }
}
```

Add this in `<head>` as `<script type="application/ld+json">` for SEO. Repeat per location.
