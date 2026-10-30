# <Page name> – build spec

Copy this folder to `design-handoff/<page>/` (e.g. `design-handoff/home/`) and fill it in.

## Files in this folder

- `design.html` – exported HTML of the approved design
- `desktop.png` – full-page screenshot at 1280px
- `mobile.png` – full-page screenshot at 375px

## Template

- Shopify template: `templates/<index|product|collection|page.about|cart>.json`

## Sections (top to bottom)

| # | Section file | Existing or new | Settings | Blocks |
| --- | --- | --- | --- | --- |
| 1 | `sections/ah-hero.liquid` | new | heading, text, image, button label + link | – |
| 2 | `sections/ah-image-with-text.liquid` | new | eyebrow, heading, text, image, image on right, 2 buttons | tag (text) |
| 3 | Dawn `featured-collection` | existing (restyle only) | collection | – |

## Data sources

- Which collection, products, metafields or apps feed each section (e.g. reviews from Judge.me).

## Notes

- Interactions (sliders, drawers), states (empty, sold out), anything not obvious from the screenshots.
- Anything that is sample copy and must come from settings.
