# Snip & Search

Landing page for **Snip & Search**, a free macOS Shortcut: select any part of your screen and it's reverse-image-searched on Google Images.

- Live site: https://snip-and-search.netlify.app/
- Install the Shortcut: https://www.icloud.com/shortcuts/b5897ea6db59406a80dbd3e58228abb7

## Project

A single static page with no build step or dependencies:

```text
index.html      # Page content + meta/Open Graph tags
style.css
images/         # Shortcut icon
og-image.png    # Social preview image
```

To preview locally, open `index.html` in a browser (or serve the folder with any static server, e.g. `npx http-server .`). Netlify publishes the repo as-is.

The page's demo video is served from the repo's GitHub Release (`v1.0.0`), not from this folder: the files in `demo/` are gitignored (too large for the repo) and exist only locally. The page's second `<source>` (`demo/snip-and-search-demo.mov`) therefore 404s on the live site; browsers only fall back to it if the Release URL fails.
