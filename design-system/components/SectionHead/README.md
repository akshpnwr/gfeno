# SectionHead

The heading row that opens a content section: an optional eyebrow and heading on the left, an optional text link on the right.

## When to use

- At the top of any section that lists things (categories, products, reviews), so every list on the page opens the same way.
- Use the link for "see more" destinations ("View all products"), never for the section's main action.

## Anatomy

- `.ah-section-head`: flex row, bottom-aligned, space between. Margin below `space-6` on mobile, `space-8` from 750px.
- `.ah-eyebrow` (optional): `label` style in `brand`.
- `.ah-heading.ah-heading--section`: `heading-2` (30/36) on mobile, `heading-1` (40/46) from 750px, `ink`, weight 700. An `h2` the section is labelled by.
- `.ah-link` (optional): 16/24 weight 700 in `brand`, underlined with a 3px offset; turns `ink` on hover.

## Layout

The link sits on the heading's baseline row at the right; when the row is too narrow it wraps below the heading (`space-2` row gap, `space-4` column gap).

## What the consumer provides

Heading text; optionally eyebrow text, link label and link URL (both needed for the link to show).

## Shopify

<!-- Before the about page build: `snippets/ah-section-head.liquid`, rendered by `ah-category-grid`, `ah-featured-products` and `ah-testimonials` with `heading`, `eyebrow`, `link_label`, `link_url` and `heading_id` (for the section's `aria-labelledby`). -->
`snippets/ah-section-head.liquid`, rendered by `ah-category-grid`, `ah-featured-products`, `ah-testimonials`, `ah-value-props`, `ah-process-steps` and `ah-ingredient-grid` with `heading`, `eyebrow`, `link_label`, `link_url` and `heading_id` (for the section's `aria-labelledby`).
