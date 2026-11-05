# egy.one — Egypt gateway (static landing site)

The Egypt gateway for Egyptian brands, part of the **influUGC** network: one
door to UGC campaigns, influencer relations, content production, performance
marketing and social media management. Built Nov 6, 2026 (owner activation
order Nov 6 — first of three: egy.one → riyadheventshub.com → aistore.design).

## Identity (owner rule for ALL network satellites)

**ALL network satellite sites use the main influUGC identity:**

- Black background `#000`, neon lime accent `#C8FF00`, dark panels `#0A0A0A`,
  IBM Plex Sans Arabic (AR pages) / Sora + Inter (EN pages). Lime buttons
  always carry **black** text.
- Brand lockup: `egy.one` wordmark with the subline "The gateway for
  Egyptian brands" (Arabic: «بوابة البراندات المصرية»).
- Real company data only: Egyptian team in this market since 2020, Arab
  League St, Agouza (Giza 12651), Egypt-first market. **No portfolio or
  works sections anywhere on the site** (owner order, Nov 6, 2026), no
  prices, no invented figures, no testimonials, no stock imagery
  (CSS/text only).

## Layout system (restructure, Nov 6, 2026)

The v1 design was rejected by the owner (loose big text, no defined frames,
no organized sections) and the site was fully restructured:

- Fixed 1200px container; **every content block sits inside a framed panel**
  (1px solid `#1E1E1E`, `#0A0A0A` background, 16px radius). No unframed text.
- Uniform section anatomy: lime eyebrow label + H2 (≤40px) + one short lead
  line (≤68ch); sections separated by hairlines; 8pt spacing scale; body
  16–17px; hero headline ≤56px.
- Hero = two framed columns: text panel (badge chip, H1, lead, dual CTA,
  fact chips) + a pure-CSS **request-path visual panel** (4 mini steps +
  stat tiles). No images.
- Coverage = framed city grid. Services = bordered card grid. Guides =
  article cards (category chip + title + excerpt + key points). FAQ =
  framed rows. CTA = framed lime-glow panel.
- Composition deliberately differs from the other satellites: egy.one leads
  with its Egypt coverage grid, has no process section, and carries its own
  copy written for the Egyptian market only.

## Pages built (3 HTML pages, 2 languages)

| File | What |
|---|---|
| `index.html` | Arabic-first landing (RTL): hero with request-path panel → 01 Coverage (framed grid of 10 cities/districts: Cairo · Giza · 6th of October · New Cairo · Obour · Maadi · Nasr City · Alexandria · Mansoura · Tanta + a framed market note) → 02 Services (5 cards: UGC campaigns, influencer PR, content production, performance marketing, social media management) → 03 Egypt market guides (3 cards: choosing an agency in Egypt, UGC that works in Egypt, Cairo vs Alexandria vs the Delta) → 04 FAQ (6 questions) → CTA panel → network footer. |
| `en.html` | Full English mirror (LTR), same composition. |
| `404.html` | Framed not-found panel (Arabic) with booking + WhatsApp CTAs. |

Plus: `styles.css`, `favicon.svg` (black + lime E1 mark), `sitemap.xml`
(hreflang-annotated), `robots.txt`, `llms.txt`.

## SEO / GEO

- Canonical base `https://egy.one/`; OpenGraph + Twitter cards; hreflang
  ar/en both ways.
- JSON-LD: `Organization` (with `parentOrganization: influUGC`, postal
  address, areaServed Egypt, the four real social profiles), `WebSite`, and
  `FAQPage` matching each page's visible FAQ exactly.
- `llms.txt` carries the services, coverage, the 4-step request path and
  guide summaries.

## CTAs (all carry the satellite UTM set)

- Booking → `https://www.influugc.com/book?utm_source=egyone&utm_medium=satellite&utm_campaign=network`
- WhatsApp (client line) → `https://wa.me/201029979797?utm_source=egyone&utm_medium=satellite&utm_campaign=network`
- The only influUGC references on the site: the footer network line
  («جزء من شبكة influUGC» / "Part of the influUGC network") + these CTAs.

## What remains (not done here)

1. **Domain attach** — egy.one DNS records are recorded in
   `../DNS-BATCH.md`; they are set in the new-account (`influugc`) registrar
   session, after which Render verifies + issues the certificate.
2. After go-live on the real domain: dedicated Google Search Console
   property + submit `sitemap.xml`.

## Deploy status (Nov 6, 2026)

- **Repo**: https://github.com/mostafaabaas/egyone (public, branch `main`).
- **Hosting**: LIVE — Render Static Site (free tier), auto-deploys from
  `main`: https://egyone.onrender.com (verified live).
- **Domain attach**: pending the DNS batch above.
