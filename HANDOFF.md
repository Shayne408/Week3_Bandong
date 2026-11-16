Wickd — HANDOFF

1. Project proposal
Brand: Wickd (hand-poured candles). 
Audience: everyone who loves to relax, whatever their age, background or how they browse. 
Theme: calm, warm, soft purple and amber. 
Goals: easy browsing, clear checkout, readable and keyboard-friendly pages.

2. Architecture
What: one `index.html` with five `<section class="page">` views (Home, Products, Cart, Contact, Help) switched by URL hash, plus a shared `<header>`, `<main>` and `<footer>`; `style.css` holds all styling.
Why: one landmark structure keeps the document outline valid, skip link and `aria-current="page"` work on every view, and no framework is needed.

3. Layout
What: the header is `position: fixed` so it stays visible while scrolling or using the product slider. Pages use CSS Grid (`auto-fit` / `minmax`) and Flexbox with `clamp()` and `rem` units; the mobile menu is a toggle button with `aria-expanded`.
Why: fluid units avoid horizontal scrolling from 320px to 1920px; media uses `max-width: 100%` and `object-fit`.

4. Tokens
What: all colors, spacing, type sizes, radii and shadows are variables in `:root` (`--color-*`, `--space-*`, `--fs-*`). Class names follow BEM (`.nav__link--active`).
Why: one place to change the theme and no hard-coded values in components.

5. Accessibility
What: ink `#2E2A33` on white (about 14:1), muted `#5A5360` (about 7:1) and accent `#8A4E0A` (about 6:1) meet WCAG AA; visible focus ring; labels on every field; `role="status"` toasts; reduced-motion hides videos; FAQ uses native `<details>`.
Why: the site should be comfortable for every visitor, on any device or input method. Run Lighthouse on the live link and embed the screenshot (90+ target).