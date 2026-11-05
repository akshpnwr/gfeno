# Amrit Herbals – Shopify theme

Shopify store for Amrit Herbals: household cleaning products (handwash, dishwash, floor cleaner, refills) made with natural ingredients. Market: India, mostly mobile shoppers.

Theme: **Dawn** (Shopify free theme, Online Store 2.0). Pages are designed in claude.ai using the Amrit Herbals design system, then built here as Liquid.

## Repo map

| Path | What |
| --- | --- |
| `layout/ sections/ snippets/ blocks/ templates/ config/ locales/ assets/` | Dawn theme files (pulled with Shopify CLI) |
| `assets/amrit-tokens.css` | Design tokens as CSS variables, all prefixed `--ah-`. Generated from `design-system/tokens.json`. |
| `assets/amrit-components.css` | Shared component styles, classes prefixed `ah-`. |
| `design-system/` | Copy of the design system: `README.md` (brand book, read it), `tokens.json`, `components/<Name>/README.md` + `preview.html` (reference HTML). Not uploaded to Shopify. |
| `design-handoff/<page>/` | Approved page designs to build: exported HTML, desktop/mobile screenshots, `spec.md`. Not uploaded to Shopify. |

Before building anything visual, read `design-system/README.md` and the relevant `design-system/components/*/README.md`.

## Commands

```bash
shopify theme dev --store gfeno.myshopify.com     # local preview with hot reload
shopify theme pull --store gfeno.myshopify.com    # pull latest from the store (overwrites local files: commit first)
shopify theme push --unpublished                    # push as a new unpublished theme for review
shopify theme check                                 # lint Liquid
```

Never run `shopify theme push --live` or publish a theme unless explicitly asked.

## Rules for working on this theme

### Do not edit Dawn core files

- Build custom work as **new files**: `sections/ah-<name>.liquid`, `snippets/ah-<name>.liquid`, `assets/ah-<name>.js`.
- Only touch Dawn files where unavoidable (e.g. loading CSS in `layout/theme.liquid`). Mark every such change:
  `{%- comment -%} AMRIT: <reason> {%- endcomment -%}`
- This keeps future Dawn updates mergeable.

### Never delete existing code

- Never delete lines, including comments, from existing files. Comment out or add alongside instead, and say what was changed.
- Refer to code by exact region (file + surrounding code), not by line numbers.

### Styling

- Use the design tokens only: `var(--ah-brand)`, `var(--ah-space-4)`, `var(--ah-radius-md)`, etc. No raw hex values, no new colours, no new fonts.
- Token names in `design-system/` are unprefixed (`brand`, `space-4`); in the theme they are `--ah-brand`, `--ah-space-4`.
- Type styles are shorthand variables: `font: var(--ah-text-heading-1); letter-spacing: var(--ah-tracking-heading-1);`. Spacing steps are 2, 3, 4, 6, 8, 12 (8–48px); use `calc()` only for larger multiples (64px, 96px).
- Reuse classes from `assets/amrit-components.css` (`ah-btn`, `ah-heading`, `ah-tag`, ...). New component CSS goes in that file or in a section's `{% stylesheet %}` tag, prefixed `ah-`.
- Breakpoint: 750px (matches Dawn). Mobile first.
- Font: Plus Jakarta Sans only, loaded once in `layout/theme.liquid`. Also set Dawn's heading and body fonts to Plus Jakarta Sans in Theme settings > Typography.
- Never use cream backgrounds, forest green, copper/brown accents or serif fonts (keeps us distinct from a look-alike competitor).
- Contrast: `--ah-accent`, `--ah-offer`, `--ah-leaf-tint` take `--ah-ink` text only. Sale prices use `--ah-offer-strong`.

### Sections

- Every section has a full `{% schema %}`: merchant-editable settings for all copy, images, links and toggles; blocks for repeatable items (reviews, tags, cards); `presets` so it can be added in the theme editor.
- Wrap section markup in a root element with class `ah-root` plus the section class.
- Section `{% stylesheet %}` CSS loads before `assets/amrit-components.css`, so a section rule that overrides a component class needs an extra class in the selector (`.ah-hero .ah-hero__heading`, not `.ah-hero__heading`).
- Colour scheme settings: add `ah-scheme color-{{ section.settings.color_scheme }}`; the background follows the scheme, text stays `--ah-ink`. Schemes 1–4 only; scheme 5 (brand background, white text) is not supported by `ah-` sections.
- No hard-coded copy in markup; all text comes from settings or locale strings.
- Images: `image_url` with `widths` + `image_tag` (responsive `srcset`), `loading: 'lazy'` below the fold, always an alt text setting.
- JS: none unless needed. If needed, vanilla JS (custom element, like Dawn), in `assets/ah-<name>.js`, loaded with `defer`. No jQuery, no frameworks.
- Accessibility: semantic HTML, visible focus states, `aria-label` on icon-only controls and star ratings.

### Copy

- Plain, upbeat, specific. Product titles lead with the hero ingredient: "Neem & Tulsi Handwash, 250 ml".
- Only provable claims ("made with natural ingredients"). No "chemical-free" / "100% natural" unless confirmed.
- Sentence case. No emoji.

### config/settings_data.json

- Holds the store's live theme-editor settings and is overwritten by `theme pull`. Do not hand-edit it unless asked; colour schemes and typography are set in the theme editor (mapping in `design-system/README.md` > Shopify mapping).

## Building a page from a handoff

1. Read `design-handoff/<page>/spec.md`, the screenshots and the exported HTML.
2. List the sections needed; reuse existing `ah-` sections before creating new ones.
3. Build each section as `sections/ah-<name>.liquid` with schema, then add it to the right template (`templates/*.json`).
4. Check with `shopify theme dev` at 375px and 1280px, and run `shopify theme check`.
5. Report anything in the design that could not be built as designed, instead of silently changing it.

## Source of truth

- Design decisions are made in claude.ai (Amrit herbals project, design system artifact). If a change is made here during build (spacing, colour, new component), list it in the summary so it can be copied back to the design system.

## Owner preferences

- Give only what is asked; no extras unless requested. Direct, no flattery, no emojis. Say when guessing.
- Owner's general stack (for any non-Shopify tooling): React + TypeScript, Tailwind + shadcn/ui, React Hook Form + Zod, TanStack Query, Zustand, Node/Express + TypeScript, MongoDB + Mongoose.
