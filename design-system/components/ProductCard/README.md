# ProductCard

The storefront's product tile: image with an optional badge, ingredient-led title, hero ingredients, rating, price and an add to cart button.

## When to use

- Every product list: featured products on the home page, collection grids, related products, search results.
- One primary action per card. In a grid every card has the same action row, so the row lines up.

## Anatomy

- `.ah-card`: column, 1px `border` hairline, `radius-md`, `surface-100`, clips its corners. Fills the grid row height so action rows align.
- `.ah-card__media`: square image area on `surface-200`. The image links to the product but is hidden from screen readers (the title link is the accessible one).
- `.ah-card__badge` (optional, top left, `space-2` inset on mobile, `space-4` from 750px): `label` style pill. One badge at most, by priority:
  1. Sale: "15% off" (percent from the compare-at price) on `offer` (`ah-card__badge--offer`).
  2. New: product tagged `new`, on `accent`.
  3. Bestseller: product in the bestseller collection, on `accent`.
- `.ah-card__body`: `space-2` gap, padding `space-4` on mobile, `space-6` from 750px.
- `.ah-card__title`: product title, 16/24 weight 700 on mobile, 18/26 from 750px, `ink`, underlines on hover. Titles lead with the hero ingredient: "Neem & Tulsi Handwash, 250 ml".
- `.ah-card__meta` (optional): hero ingredients in `small` `ink-muted`, e.g. "Neem, tulsi, aloe vera".
- `.ah-card__rating` (optional): 14px stars (see Testimonials: partial fills), the rating to one decimal, and the review count in brackets, all `small` `ink-muted`.
- `.ah-price`: current price in `heading-3` (20/28, weight 700) `ink`. On sale (`ah-price--sale`) the current price is `offer-strong` and the compare-at price follows, struck through, in `small` `ink-muted`. Screen readers hear "Sale price" and "Regular price". Products with varying prices read "From ₹…".
- `.ah-card__actions`: pinned to the bottom of the card. A full-width `ah-btn--primary` (with `space-2` side padding so the label fits two columns on mobile):
  - Single-variant product: "Add to cart" (adds without leaving the page; shows a spinner while adding).
  - Product with options: "Choose options", a link to the product page.
  - Sold out: a disabled "Sold out" button (50% opacity).
  - Errors from adding show below the button in `small` `danger`.

## Layout

In a grid: two columns on mobile with a `space-4` gap; from 750px, as many columns of at least 220px as fit with a `space-6` gap; four columns from 990px.

## What the consumer provides

Product image (square, on a pale ground), title, price and compare-at price; optionally hero ingredients, rating and review count, a `new` tag, and membership of the bestseller collection. Badge texts ("[percent]% off", "New", "Bestseller") are settings.

## Shopify

`snippets/ah-product-card.liquid`, rendered by `sections/ah-featured-products.liquid`; price from `snippets/ah-price.liquid`, stars from `snippets/ah-rating-stars.liquid`.

- Hero ingredients: product metafield `custom.hero_ingredients` (single line text). Hidden when empty.
- Rating: product metafields `reviews.rating` and `reviews.rating_count`, written by a reviews app. Hidden when empty.
- Add to cart uses Dawn's `product-form` element; the section loads `product-form.js` when add to cart is on.
