# Change: Refactor Astro static mirror for hiso33.casino

## Why
The current app mirrors a Framer-exported site but includes bloated assets and legacy scaffolding. We need a cleaner, maintainable static mirror of https://www.hiso33.casino/ that preserves layout, SEO metadata, and tracking while reducing unnecessary code and assets.

## What Changes
- Keep Astro static output and the Framer mirror approach already in the repo.
- Refresh the mirrored snapshot and asset list from https://www.hiso33.casino/.
- Prune unused/duplicate assets and remove unused styling or tooling (e.g., Tailwind if not required).
- Preserve all SEO metadata and tracking snippets from the live site.
- Document the mirror workflow so future updates are repeatable.

## Impact
- Affected specs: marketing-site
- Affected code: mirror script, Astro pages/components, styles, and public assets.
