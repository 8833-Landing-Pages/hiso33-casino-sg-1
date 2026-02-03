## ADDED Requirements
### Requirement: Static Astro Mirror
The system SHALL provide a static Astro site that mirrors the live https://www.hiso33.casino/ layout and content.

#### Scenario: Static build
- **WHEN** the project is built for production
- **THEN** the output SHALL be a fully static site without runtime data dependencies

### Requirement: Framer Snapshot Embedding
The system SHALL render the Framer-exported markup and styles as a static snapshot.

#### Scenario: Snapshot render
- **WHEN** the home page loads
- **THEN** the Framer snapshot content and styles SHALL render as authored

### Requirement: Local Asset Mirror
The system SHALL store mirrored assets locally under `public/assets/external` and serve them from that path.

#### Scenario: Asset load
- **WHEN** the page loads in the browser
- **THEN** image and media requests SHALL be served from local `public/assets/external` paths

### Requirement: SEO and Tracking Preservation
The system SHALL preserve SEO metadata and tracking snippets from the live site.

#### Scenario: Metadata present
- **WHEN** the HTML head is rendered
- **THEN** the SEO metadata and tracking tags SHALL be present and match the live site
