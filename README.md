# Subgym — marketing site

The public website for Subgym: **https://nutifafakpodo.github.io/subgym-site/**

A single, self-contained static page, `index.html`. It sells Subgym to **gyms** (SubGym) and
**fitness sellers** (SubVendor) — the paying customers — with SubFit presented as where their
customers are. No build step, no dependencies, no external requests (inline SVG icons,
CSS-gradient art, data-URI favicon) — it works offline and deploys anywhere.

This repo is the website's only home. The product apps live in the private
`nutifafakpodo/subgym` repo.

## Publish

GitHub Pages serves the `main` branch as-is (`.nojekyll` turns off Jekyll processing). To
publish a change, commit it and push:

```bash
git push origin main
```

The live site updates within a minute or two.

## Preview locally

Open the file:

```bash
open index.html
```

Or serve it, so smooth-scroll and links behave exactly as in production:

```bash
python3 -m http.server 4186
# → http://localhost:4186
```

## Editing

Everything is in `index.html` — content, styles (a `<style>` block), and a little vanilla JS
(mobile menu, scroll reveal, footer year, the decorative QR). To change:

- **Copy / sections** — edit the HTML directly.
- **Brand colours** — the CSS variables in `:root`. They match SubFit (lime `--em` on
  near-black `--bg`), with SubGym blue (`--gym`) and SubVendor orange (`--shop`) for the
  gym and seller sections.
- **Contact buttons** — the `mailto:hello@subgym.app` links ("Book a demo", "List your gym",
  "Become a seller") → your real address or a form URL.
- **Pricing** — deliberately gives no numbers ("commission-based, ask for your rate"); add
  rates once they're final.

## Other hosts

The page is one file, so it also works on Cloudflare Pages, Netlify or Vercel (point them at
this repo, no build command, output directory `/`), or any static bucket or CDN.

## Notes

- Responsive down to phones; dark theme matching the product.
- Scroll-reveal is progressive: with JS off, all content still shows.
- Claims on the page should match what the product does today — check before adding new ones.
