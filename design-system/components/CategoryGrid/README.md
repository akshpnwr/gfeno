# CategoryGrid

A grid of category tiles, each a square image with the category name and an arrow below, opened by a SectionHead.

## When to use

- Home page, to route shoppers into the main ranges (Handwash, Dishwash, Floor cleaner, Refills).
- Four tiles is the intended count; two to five work.

## Anatomy

- Tile (`.ah-category-grid__item`): the whole tile is one link.
- `.ah-category-grid__media`: square image frame, `radius-md`, `surface-200` behind the image. The image scales to 103% on hover.
- `.ah-category-grid__label`: category name 16/24 weight 700 on mobile, `heading-3` size (20/28) from 750px, `ink`, with a Lucide `arrow-right` at 20px on the right that nudges 4px right on hover. Hover motion is off under `prefers-reduced-motion`.
- Image to label gap: `space-3` on mobile, `space-4` from 750px.

## Layout

Two columns on mobile (`space-4` gap). From 750px, as many columns of at least 200px as fit (four at full width), `space-6` gap.

## What the consumer provides

A SectionHead (heading, optional link); per tile, a collection, an optional label (defaults to the collection title), an optional image (defaults to the collection's featured image) and alt text. Images: square, product on a pale ground.

## Shopify

`sections/ah-category-grid.liquid`, one block per tile (collection, label, image, image alt).
