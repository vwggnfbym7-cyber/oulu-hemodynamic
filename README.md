# Oulu Hemodynamics website: mobile hamburger menu update

This package contains a safe, manual update for the static GitHub/Netlify website.

It does **not** replace the full site files. Instead, it contains exact snippets to add to the current GitHub files:

- `index.html`
- `styles.css`
- `script.js`

Reason: the current repository files should remain the source of truth. These snippets add only the mobile hamburger menu and avoid overwriting other content.

## What this change does

- Keeps the desktop navigation unchanged.
- Shows a three-line menu button on mobile/tablet widths.
- Opens the main navigation links in a dropdown-style menu.
- Closes the menu after a navigation link is selected.
- Preserves accessibility attributes: `aria-label`, `aria-expanded`, and `aria-controls`.

## Files in this package

- `index-html-change.html` — exact HTML change.
- `styles-css-addition.css` — CSS to append to the end of `styles.css`.
- `script-js-change.js` — JavaScript to insert inside the existing `setup()` function.
- `mobile-menu.patch` — compact patch-style summary.

## Suggested GitHub workflow

1. Open the repository in GitHub.
2. Edit `index.html`, `styles.css`, and `script.js` one at a time.
3. Apply the changes described in the snippet files.
4. Commit directly to `main` with a message such as:

   `Add mobile hamburger navigation menu`

5. Netlify should deploy automatically after the commit.

## Quick browser test after deployment

- Open the site on a phone or narrow browser window.
- Confirm that the three-line menu appears in the top header.
- Tap it: the menu should open.
- Tap Research, People, Publications, or Contact: the menu should close and the page should scroll to the selected section.
- Switch EN/FI: language switching should still work.
