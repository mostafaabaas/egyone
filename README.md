# egy.one — Egypt gateway of influUGC (static landing site)

The Egypt gateway brand of **influUGC**: the dedicated entry point for Egyptian
brands to all of the agency's services. Built Nov 6, 2026 (owner activation
order Nov 6 — first of three: egy.one → riyadheventshub.com → aistore.design).
**Files only — not deployed.**

## Design direction (owner rule, Nov 5, 2026 — 23:57)

**ALL network satellite sites use the main influUGC identity** — no distinct
per-site designs:

- Black background `#000`, neon lime accent `#C8FF00`, dark panels, bold heavy
  typography — the www.influugc.com feel. Design system mirrored from the
  prinfluencer.net satellite.
- Brand lockup: `egy.one` wordmark with the subline "The Egypt gateway of
  influUGC" (Arabic: «بوابة مصر من influUGC»).
- Only real company data: est. 2020, Arab League St Agouza (Giza 12651),
  Egypt-first market, real client names (Riyadh Season, Saudi Tourism
  Authority, flynas, Saudia, realme, Domino's, TikTok Live, Zanussi). No
  prices, no invented figures, no testimonials, no stock imagery (CSS/text only).

## Pages built (3 HTML pages, 2 languages)

| File | What |
|---|---|
| `index.html` | Arabic-first landing (RTL): hero, client proof strip, 5-service gateway (UGC campaigns, influencer PR, content production, performance marketing, social media management — each tied back to the hub, with editorial links to prinfluencer.net and filmorax.com), Egypt coverage strip (Cairo · Giza · 6th of October · New Cairo · Obour · Maadi · Nasr City · Alexandria · Mansoura · Tanta), why influUGC (with editorial links to influugc.com and explorinfluencer.com), 4-step process, 6-question answer-first FAQ, contact/CTA band, network footer. |
| `en.html` | Full English mirror (LTR), same structure and FAQ. |
| `404.html` | Branded not-found page (Arabic). |

Plus: `styles.css`, `favicon.svg` (black + lime E1 mark), `sitemap.xml`
(hreflang-annotated), `robots.txt`, `llms.txt`.

## SEO / GEO

- Canonical base `https://egy.one/` (the real domain — if this site is first
  deployed to an `onrender.com` URL before the domain attaches, switch all
  canonical/OG/sitemap/robots/llms bases in one pass, same as the ugccompany
  rule in `../DEPLOY.md` §2).
- Title/meta target UGC + influencer marketing + Egypt in both languages;
  OpenGraph + Twitter cards; hreflang ar/en both ways.
- JSON-LD: `Organization` (with `parentOrganization: influUGC`, postal address,
  areaServed Egypt, the four real social profiles), `WebSite`, and `FAQPage`
  matching each page's visible FAQ word for word.

## CTAs (all carry the satellite UTM set)

- Booking → `https://www.influugc.com/book?utm_source=egyone&utm_medium=satellite&utm_campaign=network`
- WhatsApp (client line) → `https://wa.me/201029979797?utm_source=egyone&utm_medium=satellite&utm_campaign=network`
- Footer legal line: "Part of the influUGC network" linking to the hub.

## What remains (not done here)

1. **Pull the $200 sale listing** — egy.one is currently designated for sale at
   $200 in the new Namecheap account; remove that listing in the new-account
   session so the domain is a network asset, not sale stock.
2. **Deploy** — static folder; any static host or a Render Static Site (free
   tier per the network rule). No server/admin in this build: the brief scoped
   a static landing.
3. **Domain attach** — point `egy.one` DNS at the host (same checklist pattern
   as `../DEPLOY.md` §4: apex A + www CNAME from the host's screen; no MX
   changes — mail stays on influugc.com).
4. After go-live: dedicated Google Search Console property + submit
   `sitemap.xml`; verify both pages return 200 and the FAQ renders.

## Deploy status (Nov 6, 2026)

- **Repo**: https://github.com/mostafaabaas/egyone (private, branch `main`) — source pushed Nov 6, 2026.
- **Hosting**: PENDING-DASHBOARD — the Render Static Site service has **not** been created yet.
  Creating it requires the Render dashboard (no Render API key is available to the
  automation): Render Dashboard → New → Static Site → connect this repo — the repo's
  `render.yaml` blueprint pre-fills the service name (`egyone`) and publish path (`.`).
  Expected live URL once created: https://egyone.onrender.com
- **Domain attach**: separate later batch (see "What remains" item 3 above).
