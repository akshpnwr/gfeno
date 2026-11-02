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

## Compact variant (home page)

A shorter band for the end of a page, where the heading and button sit on one row. Wrap the banner in `.ah-cta` (in the theme the section root carries it).

- `.ah-heading`: `heading-1` size (30/36 on mobile, 40/46 from 750px, `ah-heading--section`) at weight 800, with no 16ch cap. `.ah-body` has no width cap either.
- Content (eyebrow, heading, text) stacks with a `space-3` gap; `.ah-cta__content` wraps it.
- Button: full width below the text on mobile; on desktop the band becomes a row with the button right-aligned and vertically centred (wraps under the text when space runs out).
- Padding: `space-8` × `space-6` on mobile, 64px all round on desktop. No outer margin; the band sits in `ah-container` inside an `ah-section`.
- Leaf motif: optional and **off by default** (a "Show leaf motif" setting).

## Contrast

`ink` on `accent` and on `offer` both pass 4.5:1. Never put white text on either banner; `surface-100` on `offer` is 2.8:1.

## What the consumer provides

Eyebrow, heading, one sentence, button label and link. Offer banners should include the end date.

## Shopify

Build as `sections/cta-banner.liquid` with a select setting for colour (`accent` / `offer`) that toggles `ah-banner--offer`.

Built as `sections/ah-cta-banner.liquid` (the theme prefixes custom sections with `ah-`). It renders the compact variant, with settings for style (lime / offer), leaf motif, eyebrow, heading, text, button label and link.
