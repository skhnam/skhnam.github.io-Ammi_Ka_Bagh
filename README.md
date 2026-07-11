# 🌿 Ammi ka Bagh — Website

*"Naturally grown with love."*

A modern, responsive, single-page website for a small family backyard garden in East Brunswick, NJ.

## Files

```
ammi-ka-bagh/
├── index.html      # All content & structure (semantic HTML5 + Tailwind classes)
├── css/style.css   # Custom animations, masonry gallery, form styles, a11y helpers
├── js/main.js      # Menu, FAQ accordion, form validation, scroll-reveal, seasons table
└── README.md
```

## How to view

Just double-click `index.html` — it opens in any browser. No build step or server needed.
(Tailwind loads from a CDN, so an internet connection is required for full styling.)

## Replacing the placeholder images

All photos are royalty-free Unsplash placeholders. To use your own garden photos:

1. Create an `images/` folder next to `index.html`.
2. Drop your photos in (e.g., `images/grapes.jpg`).
3. In `index.html`, replace the Unsplash URL in the matching `<img src="...">` with `images/grapes.jpg`.
4. Update the `alt` text to describe your photo — this helps accessibility and SEO.

If any placeholder URL ever fails to load, the site automatically shows a soft, branded
placeholder (handled in `js/main.js`), so nothing ever looks broken.

## Making the contact form live

The form currently validates input and shows a friendly success message (front-end demo).
To receive real messages, the simplest option is [Formspree](https://formspree.io):

1. Create a free Formspree form and copy its endpoint URL.
2. In `index.html`, add `action="https://formspree.io/f/YOUR_ID" method="POST"` to the `<form>` tag.
3. In `js/main.js`, remove the `event.preventDefault()` line in the submit handler
   (or replace the handler with a `fetch()` POST to the endpoint).

## Editing content

- **Produce cards** — duplicate any `<li class="produce-card">` block in the "Our Fruits" section.
- **Seasonal table** — each row has `data-months="6,7,8"` (1 = Jan … 12 = Dec); edit the numbers and the dots update automatically.
- **Colors** — the palette lives in the small `tailwind.config` block in `index.html` (`leaf`, `earth`, `cream` + fruit accents).
- **FAQ** — copy a `faq-item` block; the accordion behavior applies automatically.

## Built with

HTML5 · Tailwind CSS (CDN) · Vanilla JavaScript · CSS-only animations ·
IntersectionObserver scroll reveals · WCAG-friendly (skip link, focus rings,
aria attributes, reduced-motion support) · SEO meta + JSON-LD structured data
