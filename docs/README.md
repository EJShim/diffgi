# DiffGI — Project Page

Static project page for **DiffGI: Differentiable Geometry Images for High-Fidelity Thin-Shell 3D Generation** (ECCV 2026).

No build step. It is a single `index.html` with self-contained CSS plus static assets.
Served from this `docs/` folder via GitHub Pages.

## Structure
```
docs/
├── index.html              # the page (all CSS inline)
├── .nojekyll               # tells GitHub Pages to serve files as-is
├── demo/                   # browser on-device image-to-3D demo (WebGPU)
│   └── index.html
└── static/
    ├── images/             # figures (PNG) + teaser poster
    ├── videos/teaser.mp4   # hero video
    └── pdfs/               # paper + supplementary
```

## Local preview
```bash
cd docs
python -m http.server 8000
# open http://localhost:8000
```

## Deploy on GitHub Pages (serve from /docs)
1. Commit and push (the `docs/` folder lives at the repo root).
2. Repo → Settings → Pages → Source: `Deploy from a branch`.
3. Branch: `main` (or `master`) · Folder: `/docs` → Save.
4. Page URL: `https://<user>.github.io/<repo>/`

`.nojekyll` is included so GitHub serves the files as-is (no Jekyll processing).

## TODO before going public
- [x] Replace anonymous authors with real names / affiliation / links.
- [x] Update the **BibTeX** entry with the author list.
- [ ] Fill in the **arXiv** link (currently disabled).
- [ ] Add the full **Video** (currently disabled); the hero `teaser.mp4` is in place.
- [ ] Wire up the in-browser inference in `demo/index.html` (see the INTEGRATION POINT) and host weights on Hugging Face.
