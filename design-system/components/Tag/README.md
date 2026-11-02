# Tag

A small pill on `leaf-tint` that marks ingredient information: an ingredient name, or a short uppercase claim.

## When to use

- `ah-tag`: ingredient names, e.g. in ImageWithText ("Neem", "Tulsi"). Up to 4 in a row.
- `ah-tag ah-tag--label`: one short provable claim above a heading, e.g. the hero's "Made with natural ingredients". One per view.
- Not for discounts or "New" (those are product card badges on `offer` and `accent`), and not clickable. For a row of linkable ingredients use IngredientStrip.

## Anatomy

- Pill, `radius-pill`, `leaf-tint` fill, `ink` text, 6px × 14px padding.
- `ah-tag`: 14/20 weight 600, sentence case.
- `ah-tag--label`: `label` style (12/16, weight 700, `0.06em` tracking, uppercase).

## Contrast

`ink` on `leaf-tint` passes 4.5:1. Never put `brand` or white text on it.

## What the consumer provides

The text: one to three words for an ingredient, up to about 30 characters for a label. Claims must be provable (see the brand book).
