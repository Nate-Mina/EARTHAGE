# Earth Age — Dark-Mode Geochronology Explorer

A single-page, **dark-mode** data explorer presenting physical, genomic, and
chronometric arguments for an Earth roughly **6,000 years old (or less)**.
Built from a Tailwind + Chart.js HTML page and wrapped so it deploys on
**GitHub Pages** using a **Jekyll theme** (currently `jekyll-theme-cayman`).

## What's in here

| File | Purpose |
|------|---------|
| `index.html` | The page itself (dark mode + graphic "tips" infocards). Wrapped in `{% raw %}` so Jekyll passes the markup through untouched. |
| `_config.yml` | Jekyll / GitHub Pages config — sets the theme and metadata. |
| `Gemfile` | Ruby dependency pin for local builds and GitHub Pages. |
| `README.md` | This file. |

## Deploy to GitHub Pages (the easy way)

1. Create a new repo on GitHub (e.g. `earth-age`).
2. Push these files to the **default branch** (`main`):
   ```bash
   git init
   git add .
   git commit -m "Add dark-mode earth-age explorer"
   git branch -M main
   git remote add origin git@github.com:YOURNAME/earth-age.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root)**.
4. Wait ~1 minute, then visit `https://YOURNAME.github.io/earth-age/`.

GitHub Pages runs Jekyll automatically, applies the Cayman theme, and serves
your `index.html`. No build step required on your machine.

## Change the Jekyll theme

Edit `theme:` in `_config.yml`. Gem-based themes you can use out of the box
on GitHub Pages include:

- `jekyll-theme-cayman`  (current — clean, single column) **← recommended for this layout**
- `jekyll-theme-minimal`
- `jekyll-theme-leap-day`
- `jekyll-theme-merlot`
- `jekyll-theme-midnight`  (dark background — also a good fit for dark mode)
- `jekyll-theme-slate`     (dark, documentation-style)
- `jekyll-theme-tactile`
- `jekyll-theme-architect`
- `jekyll-theme-primer`

> Note: because `index.html` is a standalone `layout: none` page, the Cayman
> (or other) theme's default styling is *not* injected into the content — it
> only affects 404/auto-generated pages. The page carries its own dark styling,
> so it looks the same on every theme. Cayman is chosen so the site's default
> favicon/header stay consistent with a single-page project.

## Build locally (optional)

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

## Notes

- The page loads Tailwind and Chart.js from CDNs, so it needs internet access
  when viewed.
- All five "tip" graphics are inline SVG — no image files to host.
- Content authored by Nathaniel Mina; presented as a research synthesis.

MIT No Attribution — reuse freely.
