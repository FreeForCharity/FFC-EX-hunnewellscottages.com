# FFC-EX-hunnewellscottages.com

Hunnewell's Cottages — lakefront cottage rentals in Avon Park, FL (static, GitHub Pages).

This repository holds a fully localized static capture of the former WordPress site at
`hunnewellscottages.com`, migrated as part of the FFC Wave-1 WordPress-to-Pages program
([FFC-Cloudflare-Automation#702](https://github.com/FreeForCharity/FFC-Cloudflare-Automation/issues/702)).

> **Note:** this is a for-profit property (sites-list classification: For-Profit),
> migrated as a host-exit necessity. The footer carries the minimal
> "Site hosted by Free For Charity" credit, not charity attribution.

## Hosting

- Deployed to GitHub Pages on the default URL:
  <https://freeforcharity.github.io/FFC-EX-hunnewellscottages.com/>
- Deployment runs from `.github/workflows/static.yml` on every push to `main`.
- No custom domain and no DNS changes are configured at this stage.

## Structure

Plain static HTML capture — no build step. Main pages: home, `/about/`, `/rooms/`,
`/amenities/`, `/nearby-attractions/`, `/blog/` (+ 10 posts), `/contact-us/`,
`/terms-conditions/`, plus category/author archives.

## Migration notes

- Google Fonts (Source Sans Pro) localized to `wp-content/ffc-local-fonts/`.
- Booking stays on the external Cloudbeds reservation engine (working provider, kept).
- Contact Form 7 form replaced with the phone numbers published on the same page.
- Mangled `tel:` links (capture-tool artifact) repaired — 54 occurrences.
- Stripped: Cloudflare rocket-loader, UserWay widget loader, GA4/gtag, analytics
  beacons, WP runtime cruft (wp-json/, feeds, xmlrpc, wp-login, `?p=` duplicates,
  `sample-page`, `rooms-old`).
- Known pre-existing broken ref: `gallery-by-supsystic` CSS points at a
  `loading.gif` that 404s on the origin site too.

## Maintenance

- Edit the HTML in place; every push to `main` redeploys.
- `linkcheck.yml` runs lychee weekly and on pushes/PRs to catch link rot.

---

Site hosted by [Free For Charity](https://freeforcharity.org).
