# Snip & Search

Landing page for **Snip & Search**, a free macOS Shortcut: select any part of your screen and it's reverse-image-searched on Google Images.

- Live site: https://snip-and-search.netlify.app/
- Install the Shortcut: https://www.icloud.com/shortcuts/0d8c585da8954e35b6407883fbb75221

## Project

A single static page with no build step or dependencies:

```text
index.html      # Page content + meta/Open Graph tags
style.css
images/         # Shortcut icon (512px) + rounded favicon
og-image.png    # Social preview image
```

The header shows the shortcut's icon above its name, set in the page's system font (as on Apple's iCloud page for the shortcut), matching the portfolio project card (`Personal-Site/scripts/images/templates/snipAndSearch.html`).

To preview locally, open `index.html` in a browser (or serve the folder with any static server, e.g. `npx http-server .`). Netlify publishes the repo as-is.

The page's demo video is served from the repo's GitHub Release (`v1.0.0`), not from this folder: the files in `demo/` are gitignored (too large for the repo) and exist only locally.

The shortcut icon is rebuilt at 512px to match the one Shortcuts shows (iCloud only serves a 150px copy): the SF Symbol `scissors` (semibold, rendered with AppKit) on the icon's indigo gradient (`#5C72C2` to `#425BB8`), sized and placed to match Apple's rendered icon. `favicon.png` is the same image with Apple's ~8% corner radius.
