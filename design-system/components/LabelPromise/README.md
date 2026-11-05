# LabelPromise

An intro beside two cards: what the brand says about its products and what it refuses to say.

## When to use

- About page, once, to set out the claims policy.
- List only claims you can prove under "We say". See Content fundamentals in the brand book.

## Anatomy

- `.ah-promise__intro`: `.ah-eyebrow`, `.ah-heading.ah-heading--section` and `.ah-body`, stacked with a `space-4` gap. It does not use SectionHead.
- `.ah-promise__card--say`: `leaf-tint` fill, `radius-md`, no border. `ink` text only.
- `.ah-promise__card--wont-say`: `surface-100` with a 1px `border` hairline, `radius-md`.
- Card padding `space-4` on mobile, `space-6` from 750px; contents stack with a `space-4` gap.
- `.ah-promise__title`: `heading-3` in `ink`, no tracking.
- `.ah-promise__item`: 22px icon beside `body` text in `ink`, `space-3` gap, items `space-3` apart. `check` in `brand` on the "We say" card, `x` in `ink` on the other.

## Layout

The intro and the cards wrap at a shared `space-12` gap: intro on a 360px basis, cards on a 560px basis at twice the growth. Cards sit in as many columns of at least 260px as fit, `space-4` gap on mobile, `space-6` from 750px. On mobile everything stacks.

## What the consumer provides

Eyebrow, heading, one or two sentences, two card titles, and one short line per item. A card with no items does not show.

## Shopify

`sections/ah-label-promise.liquid`. Settings: colour scheme (default scheme 1), eyebrow, heading, text, first and second card titles. Two block types, "We say item" and "We won't say item" (text only), up to 12 in total.

## Notes

- Check and x icons use the system's 2px stroke. The About design showed 2.5px.
- Card padding follows the brand book (`space-4` on mobile, `space-6` from 750px). The About design showed 24px on mobile.
