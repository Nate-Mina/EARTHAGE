# Earth Age — Dark-Mode Geochronology Explorer

**Empirical Evidence for a Short-Timescale Earth** — a dark-mode, single-page
data explorer that lays out why physical, genomic, and chronometric
measurements fit a planet only **~6,000 years old (or less)**.

🔗 **Live site:** https://nate-mina.github.io/EARTHAGE/

---

## What the site argues

The page is built around one claim: current "deep time" dating assumptions
break down under physical measurement, and the same numbers keep landing on a
young age. It's organized as five quick-read graphics plus deeper sections,
each backed by cited research.

### The five "quick tips" (shareable graphics)

1. **Zircon Helium Won't Stay** — Helium leaks out of the Fenton Hill zircons
   fast. If Earth were 1.5 billion years old, **0% should remain** — yet
   **58%** is still there. That only fits a ~6,000-year clock.
2. **C-14 in "Ancient" Diamonds** — Carbon-14 decays away in ~100,000 years,
   yet it shows up **inside diamonds** claimed to be 1–3 billion years old.
3. **Dating Clocks Disagree** — Same Grand Canyon rock, four methods, ages off
   by **hundreds of millions of years**. Settled dating would make them match.
4. **Soft Tissue in Dino Bone** — *Science* (2005) found flexible blood
   vessels in *T. rex* bone. Organic matter can't survive 65+ million years,
   but fits thousands.
5. **Magnetic Field Is Fading** — Earth's field decays ~5%/century. Go back
   only ~6,000–10,000 years and it would have been impossibly strong — a
   young-Earth signature.

> **Bottom line (from the page):** helium, C-14, discordant clocks, soft
> tissue, and the magnetic field all converge on the same number — an Earth
> roughly **6,000 years old, or less.**

### The deeper sections

- **Physical Anomalies — The Zircon Helium "Leaky Clock"** — the 58% paradox
  and a diffusion age of ~6,000 years (vs. a 100,000× error in the
  deep-time prediction), shown in an interactive chart.
- **Catastrophic Plate Tectonics (CPT)** — runaway subduction, continental
  megasequences, and oceanic heat sinks as mechanisms for rapid, global
  deposition.
- **Tandem Repeats & Genetic Entropy** — non-coding "junk DNA" that actually
  functions as regulatory tuning knobs, structural anchors, and adaptive
  switches, pointing to engineered design and genetic decay.
- **The Carbon Reservoir Illusion** — how a pre-flood biosphere and stronger
  magnetic field dilute the C-14 ratio, making a 6,000-year sample *look*
  far older (with a live slider simulation).
- **Comprehensive Research Library** — 11 cited sources (RATE project,
  Baumgardner, Snelling, Vardiman, Humphreys, Austin, Schweitzer, Clarey,
  Tomkins, and more).

### Design

- **Dark / light toggle** — defaults to dark mode (near-black `#0c0a09` background, amber accents) with a sun/moon button in the nav that flips to a warm-paper light theme; the choice is remembered in `localStorage`.
- All five tip graphics are **inline SVG** — no image files to host.
- Tailwind + Chart.js loaded from CDNs; the page carries its own styling and
  uses `layout: none`, so no Jekyll theme is needed.

---

## Install / build options

The site is a single static `index.html`. You don't need to build anything to
view it — just open the file or visit the live URL above. The options below
are only if you want to host or modify it yourself.

### Option A — Just view it (no install)

Open `index.html` in any browser, or visit the live GitHub Pages site:
https://nate-mina.github.io/EARTHAGE/

### Option B — Run locally with Jekyll

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

### Option C — Deploy your own GitHub Pages (GitHub Actions)

1. Fork/clone this repo and push to your `main` branch.
2. In your repo: **Settings → Pages → Build and deployment → Source:
   GitHub Actions**.
3. The `Deploy Jekyll site to Pages` workflow in
   `.github/workflows/jekyll.yml` builds and deploys automatically on push
   (~1 min). Watch it with:
   ```bash
   gh run list --repo <you>/<repo>
   gh run watch <run-id> --repo <you>/<repo>
   ```

### Files

| File | Purpose |
|------|---------|
| `index.html` | The page itself (dark mode + tip graphics). Wrapped in `{% raw %}` so Jekyll passes the markup through untouched. |
| `_config.yml` | Jekyll/GitHub Pages config — metadata + `jekyll-feed`. No `theme:` (self-styled). |
| `Gemfile` | Bare `jekyll` dependency for local + Actions builds. |
| `.github/workflows/jekyll.yml` | GitHub Actions build & deploy workflow. |
| `README.md` | This file. |

Content authored by **Nathaniel Mina** (mechanical engineering, RIT);
presented as a research synthesis.

MIT No Attribution — reuse freely.
