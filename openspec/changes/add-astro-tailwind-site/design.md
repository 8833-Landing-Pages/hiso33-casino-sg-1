## Context
Astro static site that mirrors a Framer-exported marketing page from https://www.hiso33.casino/. The current repo already uses a Framer snapshot + local asset mirror, but needs cleanup and refreshed assets.

## Goals / Non-Goals
- Goals: visual parity with the reference site, refreshed snapshot + assets, SEO and tracking parity, and a clean static build.
- Non-Goals: dynamic data sources, CMS integration, localization, or runtime personalization.

## Decisions
- Decision: Keep Astro static output and file-based routing.
- Decision: Keep Framer snapshot HTML split into `FramerMain`/`FramerScripts` and mirror its CSS into `src/styles/framer.css`.
- Decision: Store mirrored third-party assets locally in `public/assets/external` and rewrite snapshot URLs to local paths.
- Decision: Keep fonts loaded externally (as provided by the Framer export) to avoid unnecessary local font bloat.
- Decision: Scope work to the main landing page plus the existing redirect page.

## Risks / Trade-offs
- Asset volume can still be large; pruning must avoid breaking the snapshot.
- Mirroring Framer output trades flexibility for parity and speed.

## Migration Plan
- Refresh snapshot, CSS, and asset list from the live site.
- Rebuild local assets and update snapshot URLs to match.

## Open Questions
- None.
