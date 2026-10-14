# US-EU AI SaaS Arbitrage

A daily research routine that tracks US application-layer AI SaaS rounds, tests hypotheses about structural EU gaps, and shows how conviction changes over time.

- `ROUTINE.md`: the prompt the scheduled routine runs.
- `data/`: state the routine reads and updates (`theses.json`, `candidates.json`, `runs/`).
- `site/`: static dashboard that renders `data/`.
- `.github/workflows/pages.yml`: deploys the site to GitHub Pages on every push to `main` that touches `site/` or `data/`.

One-time setup: in the repo settings, set Pages source to "GitHub Actions".
Local preview: `python3 -m http.server` from the repo root, then open `/site/index.html`.
