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

## Layout

Stacks below 750px (Shopify's tablet breakpoint), image first. Above it, two equal columns with `space-12` gap.

## What the consumer provides

Image (at least 1000 × 1250px, natural light, real ingredients in frame), alt text, copy, button links.

## Shopify

Build as a section (`sections/image-with-text.liquid`) with settings for image, eyebrow, heading, text, tags (comma-separated text), button labels and links, and a "Image on right" checkbox that adds `ah-image-text--reverse`.
