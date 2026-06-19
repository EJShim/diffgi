# DiffGI — Project Page

Static project page for **DiffGI: Differentiable Geometry Images for High-Fidelity Thin-Shell 3D Generation** (ECCV 2026).

No build step. It is a single `index.html` with self-contained CSS plus static assets.

## Structure
```
site/
├── index.html              # the page (all CSS inline)
├── .nojekyll               # tells GitHub Pages to serve files as-is
└── static/
    ├── images/             # figures (PNG) + teaser poster
    ├── videos/teaser.mp4   # hero video
    └── pdfs/               # paper + supplementary
```

## Local preview
```bash
cd site
python -m http.server 8000
# open http://localhost:8000
```

## Deploy on GitHub Pages
Option A — serve from the repo root:
1. Push the **contents of this `site/` folder** to the repo root (so `index.html` is at the top level).
2. Repo → Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)`.
3. Page URL: `https://<user>.github.io/<repo>/`

Option B — keep this `site/` folder and serve from `/docs`:
1. Rename `site/` to `docs/`.
2. Settings → Pages → Branch: `main` / `/docs`.

## TODO before going public
- [ ] Replace **Anonymous Author(s) / Anonymous Institution** with real names, affiliations, links.
- [ ] Fill in the **arXiv** link (currently disabled).
- [ ] Enable the **Code** button when the repo is released.
- [ ] Update the **BibTeX** entry with final author list / proceedings info.
