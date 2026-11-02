# ImageWithText

A two-column section pairing a product or ingredient image with a heading, short copy, ingredient tags and up to two buttons.

## When to use

- Homepage feature blocks ("Why neem?"), product story sections on a product page, About page.
- One per screen height. Alternate `ah-image-text--reverse` when stacking several so the image switches sides.

## Anatomy

- `.ah-media`: image frame, 4:5, `radius-md`, `surface-200` behind it while loading. Put an `<img>` inside; the SVG in the preview is a placeholder.
- `.ah-eyebrow`: product or ingredient name, `label` style in `brand`.
- `.ah-heading`: one benefit, `heading-1` (Plus Jakarta Sans 700). Keep it under 8 words.
- `.ah-body`: 1–3 sentences, `body` in `ink-muted`.
- `.ah-tag` (optional): up to 4 hero ingredients on `leaf-tint`.
- Actions: one `ah-btn--primary`, optionally one `ah-btn--outline` (`ink` outline).

## Home page variant

Wrap the section in `.ah-iwt` (in the theme the section root carries it, on a `surface-200` band: `ah-section--band`). Differences from the default:

- Image frame: shape option, 5:4 (default) or 4:5. The frame behind the image is `surface-100`, so it shows as a white frame on the band.
- Heading: `heading-2` on mobile, `heading-1` from 750px (`ah-heading--section`). Content stacks with a `space-4` gap (`space-6` from 750px).
- **Ingredient cards** (optional, one per ingredient): title in 16/24 weight 700 `ink`, text in `small` `ink-muted`, on `surface-100`, `radius-md`, `space-4` padding (`space-6` from 750px). One column with a `space-3` gap on mobile; from 750px as many columns of at least 220px as fit, `space-4` gap.
- Ingredient tags stay available alongside the cards.
- Buttons: up to two, each with a style choice (primary or outline). Full width on mobile, natural width from 750px.
- Columns: `space-8` gap on mobile, `space-12` from 750px; no padding of its own (the section and container provide it).

## Layout

Stacks below 750px (Shopify's tablet breakpoint), image first. Above it, two equal columns with `space-12` gap.

## What the consumer provides

Image (at least 1000 × 1250px, natural light, real ingredients in frame), alt text, copy, button links.

## Shopify

Build as a section (`sections/image-with-text.liquid`) with settings for image, eyebrow, heading, text, tags (comma-separated text), button labels and links, and a "Image on right" checkbox that adds `ah-image-text--reverse`.

Built as `sections/ah-image-with-text.liquid` (home page variant), adding a colour scheme setting, the image shape option, a style select per button and one block per ingredient card.
