# AGENTS.md

## Cursor Cloud specific instructions

This repository is a single static landing page (`index.html`) for the "Tell Me How You Really Feel" podcast, plus image assets under `images/`. There is no build system, package manager, framework, or backend — all CSS is inlined in `index.html`.

### Running the site (development)
Serve the repo root over HTTP from `/workspace`:

```
python3 -m http.server 8000
```

Then open `http://localhost:8000/`. Opening `index.html` via the `file://` protocol also works, but a static server is preferred so relative image paths (e.g. `images/director chairs.jpg`) resolve consistently.

### Notes
- There are no dependencies to install and nothing to compile, so there is no update/install step.
- There is no lint, test, or build tooling configured in this repo. "Build" is a no-op; the deliverable is the static `index.html` served as-is.
- Edits to `index.html` are picked up on browser refresh (the static server does not cache aggressively); no hot-reload tooling is present.
