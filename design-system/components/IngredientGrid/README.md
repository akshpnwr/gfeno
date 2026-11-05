# IngredientGrid

A grid of the plants the brand works with, each a `surface-200` card with an icon, a name and a short line of text.

## When to use

- About page, or anywhere that introduces the ingredients one by one.
- Use IngredientStrip for a compact row of ingredient chips. Use this when each ingredient needs a sentence.

## Anatomy

- SectionHead: heading, optional text link on the right.
- `.ah-plants__item`: card on `surface-200`, `radius-md`, no border. Padding `space-4` on mobile, `space-6` from 750px. Contents stack with a `space-3` gap.
- `.ah-plants__icon` (optional): 48px circle, `leaf-tint` fill, 22px Lucide icon in `brand`. Leaf, drop or citrus.
- `.ah-plants__name`: `heading-3` in `ink`, no tracking.
- `.ah-plants__text` (optional): `small` in `ink-muted`.

## Layout

One column on mobile, `space-4` gap. Three columns from 750px, `space-6` gap, so six ingredients make two rows of three.

## What the consumer provides

Heading; optionally link label and URL (both needed for the link to show). Per ingredient: icon choice (or none), name, one sentence on what it is there for.

## Shopify

`sections/ah-ingredient-grid.liquid`. Settings: colour scheme (default scheme 1), heading, link label and URL, anchor ID. One block per ingredient (icon select, name, text), up to 12.

The anchor ID (default `ingredients`) becomes the section's `id`, so a menu link can jump to it: `/pages/our-story#ingredients`.

## Notes

- Three columns is an owner decision. The About design showed five columns with one card on a second row.
- Card padding and gaps follow the brand book (`space-4` on mobile, `space-6` from 750px). The About design showed 24px on mobile.
