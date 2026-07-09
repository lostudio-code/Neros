# Neros — Marketing Site

Single-page marketing site for Neros. Static, no build step.

## Deploy (GitHub Pages)

1. Push this repo to GitHub.
2. Settings → Pages → Deploy from branch → `main` / root.
3. `index.html` is the entry point.

Works on any static host (Netlify, Vercel, Cloudflare Pages, S3) — just serve the folder.

## Structure

- `index.html` — the page (entry point)
- `support.js` — runtime; renders the page and loads React from CDN at runtime
- `assets/` — videos, images, logo, blueprint schematics
- `Neros.dc.html` — editable design source (identical to `index.html`; edit here, then copy over `index.html`)

## Notes

- **Runtime dependencies** are loaded from public CDNs (React, Lenis, Motion): the page needs internet access on first load. For a fully self-contained/offline build, inline these.
- **Responsive**: optimized for desktop, tablet, and mobile. Nav collapses to a fullscreen menu ≤820px; the News grid stacks ≤860px.
- **Assets are heavy** (several `.mp4` hero/product videos). If the repo size is a concern, host the videos on a CDN and update the `<source src>` paths, or use [Git LFS](https://git-lfs.com/).
- No API keys, tokens, or credentials are present in the source.
