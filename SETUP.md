# Setup (one time)

1. Pull Dawn from your store into an empty folder and start git:

   ```bash
   shopify theme pull --store gfeno.myshopify.com
   git init && git add -A && git commit -m "Dawn baseline"
   ```

2. Copy everything from this kit into the theme root (same level as `layout/`): `CLAUDE.md`, `.shopifyignore`, `design-system/`, `design-handoff/`, `assets/amrit-tokens.css`, `assets/amrit-components.css`.

3. Load the font and CSS in `layout/theme.liquid`, inside `<head>`, after Dawn's `base.css` line (`{{ 'base.css' | asset_url | stylesheet_tag }}`). Do not remove anything:

   ```liquid
   {%- comment -%} AMRIT: brand font and design tokens {%- endcomment -%}
   <link rel="preconnect" href="https://fonts.googleapis.com">
   <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
   <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
   {{ 'amrit-tokens.css' | asset_url | stylesheet_tag }}
   {{ 'amrit-components.css' | asset_url | stylesheet_tag }}
   ```

   Or ask Claude Code to do this step; `CLAUDE.md` tells it how.

4. In the theme editor: set colour schemes and typography as described in `design-system/README.md` > Shopify mapping. Upload the logo under Theme settings > Logo (placeholder is in `design-system/assets/logos/`).

5. Commit: `git add -A && git commit -m "Add Amrit Herbals design kit"`.

## Keeping the kit in sync

When the design system changes in claude.ai, replace `design-system/` and regenerate the two CSS files (ask in the Amrit herbals project for an updated kit).
