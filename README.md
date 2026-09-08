# fasih_website

Marketing + support site for **Fasih** — a Classical Arabic (Fus-ha) vocabulary
trainer for iPhone, by Nrdyn LLC. Free, fully offline, no account, nothing
collected.

Plain static HTML and one stylesheet. No build step, no dependencies, no
JavaScript. The Arabic text is set in Amiri, loaded from Google Fonts.

Live at **https://fasih.nrdyn.com**.

## Pages

| File | URL | Purpose |
|---|---|---|
| `index.html` | `/` | Landing page — features, screenshots, privacy, App Store CTA |
| `support.html` | `/support.html` | FAQ and troubleshooting |
| `privacy.html` | `/privacy.html` | Privacy policy |

Netlify also resolves extensionless paths, so `/support` and `/privacy` serve
the same pages. The `<link rel="canonical">` tags point at the `.html` form.

## Other files in the root

| File | Purpose |
|---|---|
| `netlify.toml` | Publish root, security headers, cache policy |
| `robots.txt` | Allows all crawlers; points at the sitemap |
| `sitemap.xml` | The three pages, with the `fasih.nrdyn.com` host |
| `.nojekyll` | Leftover from GitHub Pages — inert on Netlify, safe to delete |

## Deploying (Netlify)

The site is deployed on Netlify from this repo: no build command, the publish
directory is the repo root, and `netlify.toml` sets the security and cache
headers. Pushing to `main` deploys.

DNS: `fasih.nrdyn.com` is a CNAME to the site's `*.netlify.app` hostname,
managed at Namecheap.

## Assets

- `assets/site.css` — the one stylesheet
- `assets/icon-512.png`, `assets/apple-touch-icon.png`, `assets/favicon-64.png` — app icon sizes
- `assets/og-image.png` — social card
- `assets/screens/` — the six App Store screenshots
- `assets/app-store-badge.svg` — Apple's official download badge

## Notes on the copy

The entry and sentence counts on the landing page (1,107 entries, 3,321 example
sentences) describe the shipped lexicon. Update them if the dataset changes.

© 2026 Nrdyn LLC.
