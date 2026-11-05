# Hero

<!-- Before the about page build: The top of the home page: an inset `surface-200` panel with a label tag, the page's one `display` heading, a line of copy, two buttons and a product image. -->
The top of a main page: an inset `surface-200` panel with a label tag, the page's one `display` heading, a line of copy, up to two buttons and an image.

## When to use

<!-- Before the about page build: - Home page only, once, directly under the header. -->
- Home page and About page, once per page, directly under the header.
<!-- Before the about page build: - For other landing pages, use ImageWithText instead; keep one `display` heading per site entry point. -->
- For other landing pages, use ImageWithText instead; keep one `display` heading per page.

## Anatomy

- `.ah-hero__panel`: inset panel inside `ah-container`, `radius-md`, background `surface-200` (in the theme, the section's colour scheme, default scheme 2). Padding `space-6` on mobile, 64px on desktop.
- `.ah-hero__leaf` (optional, on by default): one leaf in `accent` at 90% opacity, bleeding off the top right. 200px on mobile, 420px on desktop. Lens path: `M10 90 C10 40 40 10 90 10 C90 60 60 90 10 90 Z` in a 100 × 100 viewBox.
- `.ah-hero__panel--leaf-bottom` (leaf position option): moves the leaf to bleed off the bottom left, 460px at every width, `bottom: -220px; left: -160px`.
- `.ah-tag.ah-tag--label`: one short provable claim, e.g. "Made with natural ingredients" (see Tag).
- `.ah-hero__heading`: `display` style, 56/60 weight 800 on desktop, 40/44 on mobile, `-0.03em` tracking. It is the page's `h1`.
- `.ah-hero__text`: 18/28 in `ink-muted`, up to 520px wide.
- Actions: `ah-btn--primary` then `ah-btn--outline`. Stacked full width with a `space-3` gap on mobile; side by side from 750px.
- `.ah-hero__media`: image frame, 20:17, `radius-md`, `surface-100` behind the image.
- `.ah-hero__media--landscape` (image shape option): 5:4 frame instead of 20:17.

## Layout

Mobile: one column, text above image, `space-8` gap. From 750px: two columns, 1.1fr text to 1fr image, `space-12` gap, vertically centred. The section has 24px top padding on mobile and 48px on desktop (not the usual section spacing).

## What the consumer provides

Tag text, heading (one sentence, ingredient or benefit led), one or two sentences of copy, two button labels and links, an image (bright daylight, product with fresh ingredients) and its alt text.

## Shopify

`sections/ah-hero.liquid`. Settings: colour scheme, leaf motif toggle, tag, heading, text, image, image alt, two button labels and links. The image loads eagerly with high fetch priority (it is above the fold).

Added for the About page: leaf position (top right by default, or bottom left) and image shape (wide 20:17 by default, or landscape 5:4). Buttons show only when they have a label, so a page can leave them out, as About does.

## Notes

The mobile heading's 44px line height is tighter than `heading-1` (46px); it was set from the mockup.
