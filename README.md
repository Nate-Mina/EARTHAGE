# Earth Age — Dark-Mode Geochronology Explorer

A single-page, **dark-mode** data explorer presenting physical, genomic, and
chronometric arguments for an Earth roughly **6,000 years old (or less)**.

The page is a self-contained Tailwind + Chart.js HTML file. It deploys to
**GitHub Pages** via a **GitHub Actions** workflow (no Jekyll theme required —
the page carries its own dark styling and uses `layout: none`).

## What's in here

| File | Purpose |
|------|---------|
| `index.html` | The page itself (dark mode + graphic "tips" infocards). Wrapped in `{% raw %}` so Jekyll passes the markup through untouched. Footer links to the [GitHub README](https://github.com/Nate-Mina/EARTHAGE#readme). |
| `_config.yml` | Jekyll / GitHub Pages config — metadata + `jekyll-feed` plugin. No `theme:` key (the page is self-styled). |
| `Gemfile` | Bare `jekyll` dependency for local builds and the Actions build. |
| `.github/workflows/jekyll.yml` | GitHub Actions workflow that builds with Jekyll and deploys to GitHub Pages. |
| `README.md` | This file. |

## Deploy to GitHub Pages (GitHub Actions)

This repo deploys automatically on every push to `main` using the
`Deploy Jekyll site to Pages` workflow in `.github/workflows/jekyll.yml`.

1. Push to the `main` branch — the workflow builds the site with Jekyll and
   deploys it to GitHub Pages.
2. On GitHub, ensure **Settings → Pages → Build and deployment → Source:
   GitHub Actions**. (This is already set on the `Nate-Mina/EARTHAGE` repo.)
3. After the Actions run finishes (≈1 min), visit
   `https://Nate-Mina.github.io/EARTHAGE/`.

To watch a run:

```bash
gh run list --repo Nate-Mina/EARTHAGE
gh run watch <run-id> --repo Nate-Mina/EARTHAGE
```

To deploy a fresh copy to your own account: fork/clone, push to your `main`,
and set the same **Pages → Source: GitHub Actions** setting on your repo.

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
