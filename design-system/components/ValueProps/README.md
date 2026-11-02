# ValueProps

A row of short reasons to buy, each a hairline card with an icon in a `leaf-tint` circle, a title and one sentence.

## When to use

- Home page, after the product story, to answer "why this brand": ingredients, refills, delivery.
- Three or four cards. Each states one concrete, provable fact ("Free shipping above ₹499"), not a slogan.

## Anatomy

- `.ah-value-props__item`: card with a 1px `border` hairline, `radius-md`, no fill. Padding `space-4` on mobile, `space-6` on desktop.
- `.ah-value-props__icon`: 48px circle, `leaf-tint` fill, 22px Lucide icon in `brand`. Optional.
- `.ah-value-props__title`: 18/26 weight 700 on mobile, `heading-3` (20/28) from 750px, `ink`.
- `.ah-value-props__text`: `body` in `ink-muted`.

## Layout

Mobile: cards stack with a `space-4` gap; inside each, the icon sits beside the title (`space-3` gap) and the text runs full width below. From 750px: as many columns of at least 220px as fit, `space-6` gap, and the icon sits above the title (`space-3` stack).

## What the consumer provides

Per card: icon choice (or none), title of a few words, one sentence. A section label for screen readers (e.g. "Why Amrit Herbals").

## Shopify

`sections/ah-value-props.liquid`, one block per card (icon select, title, text). The section is labelled with `aria-label` from its label setting.
