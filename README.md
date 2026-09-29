# Subgym — marketing site

A single, self-contained static landing page: `index.html`. No build step, no
dependencies, no external requests (inline SVG icons, CSS-gradient art, data-URI
favicon) — it works offline and deploys anywhere.

## Preview locally

Just open the file:

```bash
open site/index.html
```

Or serve it (so smooth-scroll and relative links behave exactly as in production):

```bash
python3 -m http.server 4186 --directory site
# → http://localhost:4186  (also the `site` entry in .claude/launch.json)
```

## Deploy (pick one)

- **Cloudflare Pages / Netlify / Vercel** — drag the `site/` folder in, or point it
  at this repo with output directory `site`. Free tier is plenty.
- **GitHub Pages** — push and set Pages to serve `/site`.
- **Any bucket / CDN** — upload `index.html`; it's the whole site.

## Editing

Everything is in `index.html` — content, styles (a `<style>` block), and a tiny
vanilla-JS enhancement (mobile menu, scroll reveal, footer year). To change:

- **Copy / sections** — edit the HTML directly.
- **Brand colors** — the CSS variables in `:root`. They match SubFit (lime `--em` on
  near-black `--bg`); each app card uses its own app's brand colour (SubGym blue, SubTrainer
  purple, SubVendor orange, SubSystem violet).
- **Demo CTA** — the `mailto:hello@subgym.app` link (search for it) → your real
  address or a form URL.

## Notes

- Responsive down to phones; dark theme matching the product.
- Scroll-reveal is progressive: with JS off, all content still shows.
- Swap the placeholder email and add real logos / screenshots / traction when ready.
