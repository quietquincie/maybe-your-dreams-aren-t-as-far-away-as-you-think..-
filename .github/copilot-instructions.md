# Copilot / AI Agent Instructions for this repository

Purpose: Help AI coding agents be immediately productive working on this small static site.

Big picture
- Single-page static marketing site (landing page) served from `index.html` with styling in `style.css` and static assets in the `assets/` folder.
- No build tool, package manager, or server config present — changes are previewed by opening `index.html` in a browser or using a Live Server extension.
- External integration: Font Awesome is included via CDN (`https://kit.fontawesome.com/...`) in the head.

Key files/locations
- [index.html](index.html#L1-L400) — main content and structure (BEM-like class names). 
- [style.css](style.css) — site styles (single stylesheet).
- [assets/](assets/) — images and SVGs (e.g., Library.svg, Undraw_Books.svg).

Project-specific conventions and patterns
- Class naming follows a BEM-like pattern: examples include `nav__container`, `nav__link--primary`, `header__img--wrapper`. Preserve these patterns when adding markup or CSS.
- Asset referencing is relative to the HTML file: use `./assets/YourImage.svg`.
- Icons use Font Awesome classes inside `<i>` elements (e.g., `<i class="fas fa-bolt"></i>`). Keep the CDN script tag in the head unless you intentionally change how icons are loaded.
- Keep markup semantic and simple: the site is a static landing page — avoid introducing complex frameworks without adding a build step and documentation.

Developer workflows (discovered)
- Preview: open `index.html` directly in a browser or run a Live Server in the project root.
- Add images: place optimized SVG/PNG files into `assets/` and reference with `./assets/filename.ext` in `index.html`.
- Add scripts: if adding JS, include a `<script src="./path/to.js"></script>` just before `</body>` and update README with new dev steps.

Examples (copy-and-adapt)
- Image: `<img src="./assets/Undraw_Books.svg" alt="Books">` (see [index.html](index.html#L1-L400)).
- Icon: `<i class="fas fa-book-open"></i>` (Font Awesome CDN present in head).
- Nav link with modifier: `<a href="#" class="nav__link nav__link--primary">Books</a>`

What AI agents should do (concrete, repo-specific)
- Make small content or style edits directly in `index.html` and `style.css` and validate by opening `index.html` in a browser.
- When adding assets, update paths to `./assets/` and ensure file names do not contain spaces.
- If you add build tooling (npm, bundler, etc.), add a short README section describing new commands and update this instructions file.

What not to change without asking
- Do not change relative asset paths or remove the Font Awesome CDN link without documenting the replacement.
- Avoid introducing a build step unless you also add clear instructions and a `package.json`/`README` updates.

If something is unclear
- Tell me which additional workflows or conventions you'd like documented (branch/commit message style, deploy steps, testing approach), and I will extend this file.

---
Generated from inspection of [index.html](index.html#L1-L400) and the project root.
