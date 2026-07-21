# Atlas Commercial Consulting — Website

Single-page site (vanilla HTML/Tailwind CDN/Leaflet) for Atlas Commercial Consulting.

## Structure

```
index.html          Main site (all pages are sections toggled via JS — no routing/build step)
assets/              Logo files
  atlas-icon.png     Icon mark used in the nav and footer
  atlas-logo.png     Full logo (icon + wordmark), not currently used on the site — kept as a spare asset
clients/             Client logo images shown in the "Our Clients" marquee/grid
```

## Running locally

No build step. Just open `index.html` in a browser, or serve the folder with any static server, e.g.:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deploying to GitHub Pages

1. Push this folder as the root of a GitHub repo.
2. In the repo: **Settings → Pages → Source → Deploy from branch → `main` → `/ (root)`**.
3. Site goes live at `https://<username>.github.io/<repo-name>/` within a couple of minutes.
4. (Optional) To use a custom domain, add a `CNAME` file at the repo root containing the domain, and point a DNS `CNAME`/`A` record at GitHub Pages.

## External dependencies

The site loads three libraries from CDNs at runtime (no local copies, no build step required):

- Tailwind CSS — `cdn.tailwindcss.com`
- Leaflet.js (coverage map) — `unpkg.com`
- Font Awesome (icons) — `cdnjs.cloudflare.com`

The site requires internet access to these three domains to render correctly.

## Notes on filenames

All asset filenames are lowercase with hyphens (no spaces, no mixed case) to avoid case-sensitivity
mismatches between local development (Windows/macOS, case-insensitive) and GitHub Pages (Linux,
case-sensitive). If you add new images, please follow the same convention.
