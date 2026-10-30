# Testimonials

A section of customer review cards, each with a star rating, the quote, the reviewer's initials and name, and the product reviewed.

## When to use

- Homepage social proof, below the hero or after a product feature.
- Product pages, filtered to reviews of that product.
- Use real, verified reviews only. The quotes in the preview are sample copy.

## Anatomy

- `.ah-testimonials__head`: centred eyebrow and `heading-1`.
- Section background `surface-200`. `.ah-quote`: card on `surface-100` with a `border` outline, `radius-md`, `space-6` padding.
- `.ah-quote__stars`: 5 stars, filled in `brand`, empty as an `ink-muted` outline (class `is-empty`). Give the wrapper an `aria-label` such as "4 out of 5 stars".
- `.ah-quote__text`: 18px Plus Jakarta Sans 600. Keep quotes to 1–2 sentences (about 160 characters).
- `.ah-quote__by`: initials avatar on `accent`, name in `small` 700, product in `small` `ink-muted`.

## Layout

One column on mobile, three equal columns from 750px. Show 3 cards; for more, use a horizontal scroll or slider on mobile rather than a long stack.

## What the consumer provides

Rating (1–5), quote, reviewer name (first name and last initial), product name. A photo can replace the initials avatar at 40 × 40px, `radius-pill`.

## Shopify

Build as `sections/testimonials.liquid` with one block per review (rating range setting, quote, name, product). If a reviews app (Judge.me, Loox) is used, apply these classes to its widget output instead of duplicating data.
