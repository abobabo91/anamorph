# anamorph

Two interactive in-browser demos of anamorphic mirror reflections (conical + elliptical torus). Pure client-side HTML/canvas. Deployed to GitHub Pages at `https://abobabo91.github.io/anamorph/`.

## Critical rules

- NEVER introduce a build step, bundler, or dependency. The project is **intentionally single-file-per-demo** with zero build pipeline — that's the design.
- Each demo (`conical.html`, `elliptic.html`) must remain self-contained. No shared JS / CSS files.
- Pages are deployed as-is via GitHub Pages on push to `main` — no CI, no build artifacts. Anything that touches Pages config affects the live URL.

## Stack & run

- Pure HTML + canvas + vanilla JS — no framework, no bundler
- Run locally: open the .html files directly in a browser (no server needed)
- Deploy: push to `main` → GitHub Pages serves from repo root

## Where things live

- `index.html` — landing page linking to the two demos
- `conical.html` — conical mirror demo (adjust cone half-angle, default 87°)
- `elliptic.html` — elliptical torus demo (adds horizontal-stretch ellipse factor)
- `screenshots/` — README images

## Gotchas

- All files load directly from the repo root via GitHub Pages — paths must be relative, not absolute.
- Drag-and-drop image input + pan/zoom math lives inline in each .html file. If you refactor, **don't extract to a shared `.js` file** without a strong reason — keeping each demo standalone is the value proposition.
