# Amrit Herbals

Fresh home care, made from plants. Amrit Herbals makes handwash and household cleaning products with natural ingredients. The storefront should feel bright, energetic and modern: clean like a freshly wiped counter, not like an old apothecary.

This is a starter system built without existing brand guidelines or photography. A placeholder logo is in the Logos group. Every value here is a proposal to confirm or replace.

## Positioning against look-alikes

Herbal and Ayurvedic stores commonly use cream backgrounds, deep forest green, copper or brown accents and a classical serif (amritherbal.com is one). This system deliberately avoids all four: white ground, vivid leaf green, lime and orange accents, and a single geometric sans. Keep it that way when adding to it.

## Content fundamentals

- **Voice:** plain, upbeat, specific. Say what is in the bottle and what it does. "Neem and aloe handwash. Cleans without drying." beats "Experience the magic of nature."
- **Lead with ingredients.** Product titles name the hero ingredient first: "Neem & Tulsi Handwash, 250 ml".
- **Claims must be provable.** Use "made with natural ingredients" or list them; avoid "chemical-free" or "100% natural" unless the formula supports it.
- **Sentence case** for headings and buttons: "Add to cart", "Shop handwash".
- No emoji in product copy or navigation.

## Visual foundations

- **Ground:** pages sit on `surface-100` (white). Alternate sections, image backgrounds and the footer use `surface-200` (a faint green tint).
- **Colour roles:** `brand` (deep leaf green) is the only fill for primary buttons and the colour for links. `leaf` is the logo green, used for illustration and large display accents. `accent` (lime) carries promotional bands and badges with `ink` text. `offer` is for discounts only, with `ink` text; sale prices are set in `offer-strong`. `leaf-tint` marks ingredient information. `danger` is for errors only.
- **One primary action per view.** Add to cart is a `brand` pill (`radius-pill`, text `surface-100`, 16px weight 700). Secondary buttons are an `ink` outline. On a lime or offer band, the action is an `ink` pill with `surface-100` text.
- **Type:** one family, Plus Jakarta Sans (Google Fonts). Headings are bold (700–800) with tight tracking (`display` to `heading-3`); text uses `body`, `small`, `label`. `label` is uppercase. Load it in the Shopify theme's `theme.liquid` head.
- **Space:** an 8px base. `space-4` inside cards on mobile, `space-6` on desktop and between cards, `space-12` between homepage sections on mobile and 96px on desktop.
- **Shape:** round and friendly. Cards, images and banners `radius-md` (20px), buttons and chips `radius-pill`, inputs `radius-sm`. Separation comes from `surface-200` fills and `border` hairlines, not shadows.
- **Motif:** the leaf from the logo, drawn as a simple lens shape in `leaf` or `accent`, used large and sparingly (one per section at most).
- **Photography (guidance):** bright daylight, white or pale green backgrounds, bottles with fresh ingredients (neem sprigs, lemon halves, aloe), hands mid-wash. Avoid wooden tables, brass and dark moody setups.

## Contrast

All text pairings named in token usage notes meet 4.5:1. `accent`, `offer` and `leaf-tint` take `ink` text only. `leaf` does not meet 4.5:1 for small text on white; use it only at 24px+ or as a fill without text. `border` is decorative; form controls use `ink-muted` for their border (3:1).

## Iconography

Line icons, 2px stroke, rounded caps, 24px grid, coloured `ink` (or `brand` when active). Lucide fits. Ingredient callouts may use leaf or drop icons in `brand` on `leaf-tint`.

## Logo

A temporary logo is in the Logos group (`placeholder-logo.png`, 426 × 419 PNG). It reads "G-Feno Cleanz", not "Amrit Herbals", and is in use only until the final mark is supplied.

- Use it in the Shopify header (Theme settings > Logo) at 48–64px tall on desktop, 40px on mobile, on `surface-100` or `surface-200`.
- Keep clear space of at least `space-4` on every side. Do not recolour, stretch or place it on `brand`, `accent` or `offer`.
- If a text-only mark is needed, set "Amrit Herbals" in Plus Jakarta Sans 800 in `ink`.
- When the final logo arrives, request an SVG plus a transparent PNG and replace this file.

## Shopify mapping

Map tokens to the theme's colour schemes (Dawn and other Online Store 2.0 themes): Scheme 1 background `surface-100`, text `ink`, solid button `brand`, button label `surface-100`, outline button `ink`; Scheme 2 background `surface-200`; Scheme 3 background `accent`, text `ink`, solid button `ink`, button label `surface-100` for the announcement bar and promo bands. Set both heading and body font to Plus Jakarta Sans in Theme settings > Typography (headings bold).
