# Sierra Summit — Speaker Image Tool

A browser tool that turns a speaker photo into a Sierra Summit image:

- Automatic **background removal** + **black & white** conversion
- Four **color overlays** (soft-light 20%): purple, blue, green, yellow — each with a matching pastel background
- **Zoom** slider + drag-to-reposition, adjustable **film grain**
- **Background color** picker
- Export as **1:1 (2400×2400)** or **16:9 (3840×2160)** PNG
- A **saved-images library** (rename, re-download, delete) stored in your browser

Everything runs in the browser. Speaker photos are never uploaded to any server.
Background removal loads an AI model from a CDN the first time (needs internet); it's cached afterward.

## How it's hosted

This is a static site. `index.html` is the whole app.
It is served with **GitHub Pages** → Settings → Pages → Deploy from a branch → `main` / `(root)`.

Live once Pages is enabled:
`https://<your-username>.github.io/sierra-summit-speaker-tool/`

## Notes

- Must be served over `http(s)` (GitHub Pages, or a local web server) — opening `index.html` directly as a `file://` path won't load the background-removal model.
- `.nojekyll` tells GitHub Pages to serve the files as-is.
