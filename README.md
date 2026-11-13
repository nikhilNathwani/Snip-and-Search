# Snip & Search

Landing page for **Snip & Search**, a free macOS Shortcut: select any part of your screen and it's reverse-image-searched on Google Images.

- Live site: https://snip-and-search.netlify.app/
- Install the Shortcut: https://www.icloud.com/shortcuts/0d8c585da8954e35b6407883fbb75221

## Project

A single static page with no build step or dependencies:

```text
index.html      # Page content + meta/Open Graph tags
style.css
images/         # Shortcut icon (also the favicon)
fonts/          # Self-hosted Lilita One + its license
og-image.png    # Social preview image
```

The header title (Lilita One with a dashed "cut line" outline) matches the portfolio project card, `Personal-Site/scripts/images/templates/snipAndSearch.html`. Both parts are SVG paths in `index.html`: the outline is copied from that template, and the letters are Lilita One's glyph outlines (150px, 2px letter spacing, kerned) rather than live text, so every browser draws them identically inside the outline. If the title's wording or font changes, regenerate both (the outline with the template's trace script).

To preview locally, open `index.html` in a browser (or serve the folder with any static server, e.g. `npx http-server .`). Netlify publishes the repo as-is.

The page's demo video is served from the repo's GitHub Release (`v1.0.0`), not from this folder: the files in `demo/` are gitignored (too large for the repo) and exist only locally.

The Lilita One font is self-hosted in `fonts/` (Latin subset from Google Fonts, under the SIL Open Font License in `fonts/LilitaOne-OFL.txt`).
