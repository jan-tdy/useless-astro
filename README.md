# Useless Astro

A small, static, no-login toolbox of astronomy converters — plus a few things that exist
purely because they're funny. Built with [Astro](https://astro.build/), deployed to
GitHub Pages, nothing to sign up for.

This is the little sibling of [Visual Astro](https://github.com/jan-tdy/visual-astro),
which handles the heavier, login-required side of things (session logging, AAVSO/VSNET
exports, night planning). Useless Astro stays deliberately simple: everything here runs
client-side in the browser, with no accounts and no backend.

## Tools

- **RA/Dec Converter** — sexagesimal (HMS/DMS) ↔ decimal degrees.
- **Magnitude ↔ Flux Ratio** — Pogson relation, either direction.
- **Telescope FOV & Magnification** — magnification, true field of view, exit pupil.
- **Astronomical Distance Converter** — km, AU, light-time, light-years, parsecs.
- **Clear Sky Checker** — cloud cover forecast via the free [Open-Meteo](https://open-meteo.com/) API.
- **Catalog Converter for JapyScope** — turns a 3-column, AAVSO-style, or any other
  delimited target list into a `name,ra,dec,type,note` CSV ready to import into
  [japyscope-remote](https://github.com/jan-tdy/japyscope-remote)'s catalog importer.

## Fun & useless

- **Cloudy Night Excuse Generator**
- **Star & Exoplanet Namer**
- **Telescope Horoscope**

## Development

```sh
npm install
npm run dev       # dev server
npm run build     # production build to dist/
npm run preview   # preview the production build
```

No TypeScript build step, no framework beyond Astro itself — plain HTML/CSS/JS per page.

## Deployment

Pushing to `main` builds the site and deploys it to GitHub Pages via
`.github/workflows/deploy.yml`. The site is configured for a project page at
`https://jan-tdy.github.io/useless-astro/` (see `astro.config.mjs`); enable GitHub Pages
in the repo settings with source "GitHub Actions" for this to take effect.

## License

MIT — see [LICENSE](./LICENSE).
