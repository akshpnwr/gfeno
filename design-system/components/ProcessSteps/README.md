# ProcessSteps

Numbered white cards on a `surface-200` band, showing how something is made or done, in order.

## When to use

- About page or any page that explains a sequence.
- Three to six steps, where the order matters. For reasons without an order, use ValueProps.
- Name a test or certification in a step only if it has been done.

## Anatomy

- SectionHead: optional eyebrow and heading.
- `.ah-steps__list`: an `ol`, so the order is real for screen readers.
- `.ah-steps__item`: card on `surface-100`, `radius-md`, no border. Padding `space-4` on mobile, `space-6` from 750px. Contents stack with a `space-3` gap.
- `.ah-steps__number`: 48px circle, `brand` fill, number in `surface-100`, 20/28 weight 800.
- `.ah-steps__title`: `heading-3` in `ink`, no tracking.
- `.ah-steps__text` (optional): `body` in `ink-muted`.

## Layout

Mobile: one column, `space-4` gap. From 750px: as many columns of at least 240px as fit, `space-6` gap. The section is a band (`ah-section--band`).

## What the consumer provides

Eyebrow and heading (optional). Per step: a title of a few words and one or two sentences. The number comes from the block order, so reordering blocks renumbers the steps.

## Shopify

`sections/ah-process-steps.liquid`. Settings: colour scheme (default scheme 2), eyebrow, heading. One block per step (title, text), up to 6.

## Notes

Card padding and gaps follow the brand book (`space-4` on mobile, `space-6` from 750px). The About design showed 24px on mobile.
