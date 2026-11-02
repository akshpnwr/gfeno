# Newsletter

A centred sign-up block: heading, one line of copy, and an email field with a visible label and a subscribe button.

## When to use

- The last section before the footer on the home page (it carries the end-of-page padding, `ah-section--end`).
- One per page. Offer something concrete in the heading ("Get 10% off your first order").

## Anatomy

- `.ah-newsletter__inner`: centred column up to 760px, `space-4` gap.
- Heading: `ah-heading--section` (`heading-2` on mobile, `heading-1` from 750px). Copy: `body` in `ink-muted`.
- `.ah-newsletter__form`: up to 520px wide, left-aligned inside the centred column, `space-3` gap.
- `.ah-newsletter__label`: always visible above the input, 14/20 weight 700 `ink`. Never rely on the placeholder as the label.
- `.ah-newsletter__input`: 48px tall, `space-4` side padding, 1px `ink-muted` border (form controls use `ink-muted`, not `border`), `radius-sm`, `surface-100` fill, `body` text. Border turns `danger` when invalid.
- Button: `ah-btn--primary` pill.
- Message: `small` text below the form, `brand` for success, `danger` for errors, announced to screen readers (`role="status"` / `role="alert"`).

## Layout

Mobile: label, input and button stacked full width. From 750px: the field (label plus input, at least 260px) and the button sit on one row, aligned to the input's bottom edge.

## What the consumer provides

Heading, one line of copy, field label, optional placeholder (an example address), button label. Success and error messages come from the theme's locale strings.

## Shopify

`sections/ah-newsletter.liquid`, using Shopify's `customer` form with the `newsletter` tag.
