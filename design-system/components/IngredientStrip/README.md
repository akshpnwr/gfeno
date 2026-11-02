# IngredientStrip

A label and a row of ingredient chips, each with a small line icon, that names what goes into the products.

## When to use

- Directly under the hero on the home page, to back up the "made with natural ingredients" claim.
- Collection pages, listing the hero ingredients of that range. Chips can link to a filtered collection or an ingredient page.

## Anatomy

- `.ah-ingredient-strip__label`: `label` style in `ink-muted`, e.g. "What goes in".
- `.ah-ingredient-strip__chip`: pill, `radius-pill`, `leaf-tint` fill, `ink` text 14/20 weight 700, `space-2` × `space-4` padding, `space-2` between icon and text. Never wraps its text.
- Icon: 16px Lucide line icon in `brand` (leaf, droplet, citrus; see Iconography).
- Linked chips underline on hover.

## Layout

Mobile: label above, then one horizontal scroll row of chips that bleeds to the screen edges, `space-3` gap, no visible scrollbar. From 750px: label and chips on one centred, wrapping row. Top padding `space-6` on mobile, `space-8` on desktop; it sits close to the hero rather than taking full section spacing.

## What the consumer provides

Label text; per chip, the ingredient name, an icon choice and an optional link. Six chips or fewer fit one row on desktop.

## Shopify

`sections/ah-ingredient-strip.liquid`, one block per chip (name, icon select, link).
