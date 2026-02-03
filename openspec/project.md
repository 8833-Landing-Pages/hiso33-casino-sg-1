# Project Context

## Purpose
Static marketing site for Hiso33 (Singapore) that mirrors a Framer export and serves as a fast, static landing page. Includes a dedicated registration redirect page.

## Tech Stack
- Astro 4 (static output)
- TypeScript (scripts via tsx)
- Node.js (build/dev)

## Project Conventions

### Code Style
- ESM modules across the codebase.
- No explicit lint/format config in repo; follow existing file patterns.
- Astro pages live in `src/pages`, components in `src/components`, styles in `src/styles`.

### Architecture Patterns
- Static site generation (`output: "static"`, `build.format: "file"`).
- Framer-exported HTML is surfaced through `FramerMain`/`FramerScripts` components.
- Assets are mirrored into `public/assets/external` via `npm run mirror`.

### Testing Strategy
- No automated tests configured.

### Git Workflow
- Not specified in this repo.

## Domain Context
- Online casino marketing/landing site for the Singapore market.
- SEO/meta tags and tracking pixels are important to preserve.
- `register-success` page redirects users to an external registration URL.

## Important Constraints
- Must remain a fully static build (Astro static output).
- Keep Framer-derived HTML/CSS intact unless intentionally updated.
- Preserve tracking/SEO tags (e.g., Meta Pixel, canonical, robots directives).

## External Dependencies
- Meta Pixel (`connect.facebook.net`, `facebook.com/tr`)
- Framer assets referenced under `framerusercontent.com`
- Fonts preconnect to `fonts.gstatic.com`
- External registration redirect target (`hiso33play.com`)
