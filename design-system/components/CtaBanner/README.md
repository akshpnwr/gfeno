# CtaBanner

A bright, rounded band with an eyebrow, headline, one line of copy and a single call to action.

## When to use

- Default `ah-banner` (on `accent` lime): brand promise or category push, e.g. "Shop all products".
- `ah-banner--offer` (on `offer` orange): time-limited offers and discounts only, matching the `offer` token's role.
- At most one banner per page section; never two adjacent.

## Anatomy

- `.ah-eyebrow`: short label in `ink`.
- `.ah-heading`: `display` style (56px, 800) on desktop, `heading-1` on mobile, `ink`. Max about 16 characters per line.
- `.ah-body`: one sentence, `ink`.
- One `ah-btn--ink` button (`ink` fill, `surface-100` text).
- `.ah-banner__leaf`: large leaf motif bleeding off the top right, in `leaf` on lime and `accent` on offer. Optional; hide it if a background image is used.

## Contrast

`ink` on `accent` and on `offer` both pass 4.5:1. Never put white text on either banner; `surface-100` on `offer` is 2.8:1.

## What the consumer provides

Eyebrow, heading, one sentence, button label and link. Offer banners should include the end date.

## Shopify

Build as `sections/cta-banner.liquid` with a select setting for colour (`accent` / `offer`) that toggles `ah-banner--offer`.
