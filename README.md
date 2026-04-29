# Ryse Direct

Marketing site for **Ryse Creative · Direct Booking Website Service**.

🌐 **Live:** _coming soon — Cloudflare Pages_
📅 **Book a call:** [calendly.com/rysecreative/host-camp-x-ryse-direct-booking-website-call](https://calendly.com/rysecreative/host-camp-x-ryse-direct-booking-website-call)

---

## What this is

Single-page static marketing site. One HTML file, no build step, no framework, no dependencies.

```
ryse-direct/
├── index.html      ← the entire site (HTML + CSS + JS inline)
└── README.md
```

That's the whole thing. Drop it on any static host and it works.

---

## Deployment

This repo is connected to **Cloudflare Pages**. Every push to `main` automatically rebuilds the live site in ~60 seconds.

**Workflow:**
1. Change request comes in (via chat with Claude)
2. Claude edits `index.html` and commits
3. Cloudflare Pages detects the push, rebuilds, ships live
4. No action needed on your end

---

## Editing copy / links

All CTA links live in **one config block** at the top of `index.html`:

```js
window.RYSE = {
  calendly:    "https://calendly.com/rysecreative/host-camp-x-ryse-direct-booking-website-call",
  stripe_lite: "https://buy.stripe.com/28oaF9cBb3p41EI288",
  stripe_dfy:  "https://buy.stripe.com/fZe4gL0St2l0bfi8wx",
};
```

Change a URL in one place → every button using it updates everywhere.

To change anything else (headlines, prices, FAQs, photos, sections), just message Claude — describe the change in plain English and it'll handle the edit + commit.

---

## Tech notes

- Pure HTML + CSS + a few lines of vanilla JS (no React, no build)
- Google Fonts: Inter, JetBrains Mono, Instrument Serif (loaded via CDN)
- Mobile breakpoints at 960px and 560px
- All CTAs open in new tabs with `noopener`
- No analytics yet — easy to add Google Analytics, Plausible, or Fathom later

---

© Ryse Creative
