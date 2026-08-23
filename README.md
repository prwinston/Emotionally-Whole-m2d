# Emotionally Whole — website (static, two pages)

A static marketing site for *Emotionally Whole* by Winston H.K. Chew.
No backend, no build step, no configuration — just files. Deploys anywhere
that hosts static sites (Cloudflare Pages, Netlify, GitHub Pages).

## Files

```
index.html          main book page (hero, five domains, excerpt,
                    endorsements, author, contact, buy)
seminar.html        19 Oct 2026 teach-in page (hosted by Marketplace Mission)
sitemap.xml         lists both pages for search engines
robots.txt          allows crawlers, points to the sitemap
images/
  cover.png         book cover
  author.png        author portrait
  marketplace-mission.jpg   seminar host logo
```

All files sit at the repository ROOT (same level), with images inside the
`images/` folder. `index.html` links to `seminar.html` (announcement bar at the
top, buttons in the footer and buy section); `seminar.html` links back to
`index.html`.

## Key links baked in

- Buy button → https://www.amazon.com/dp/B0HDDK3DB3
- Contact email → thrivemindxmento@gmail.com
- Seminar registration → WhatsApp 014-348 0134 (as wa.me/60143480134)

## Deploy (Cloudflare Pages via GitHub — current setup)

Commit these files to the repo root. Cloudflare auto-redeploys on each push.
No KV, no Functions, no bindings required — this is pure static.

## SEO notes

- Both pages have title tags, meta descriptions, keywords, canonical URLs,
  Open Graph tags, and JSON-LD structured data (Book schema on index,
  Event schema on seminar).
- sitemap.xml and robots.txt are included. After deploying, submit the sitemap
  in Google Search Console: Sitemaps > enter `sitemap.xml` > Submit.
- All canonical/URL tags assume the live domain is https://emotionallywhole.com
  — if the final domain differs, update those URLs in index.html, seminar.html,
  sitemap.xml, and robots.txt.

## Still to confirm

- Seminar VENUE: currently "Penang · venue details to be confirmed" in
  seminar.html — replace with the full venue name and address when known.
- WhatsApp country code: links use 60 (Malaysia). Confirm this is correct.
