# Architecture Summary

Visual diagram: [architecture-diagram.md](architecture-diagram.md)

## Frontend

WeHeartComics uses Next.js with the App Router and React for the main web experience.

Primary surfaces include:

- Homepage
- Character guides
- Key issue pages
- First appearance and collector education pages
- Search
- Vault and wantlist flows
- Appraisal tools
- Admin tooling

## Data Layer

The app uses two data stores:

- PostgreSQL for app data such as users, vaults, settings, alerts, and product workflows.
- Turso/libSQL for catalog-style key issue data and character/issue relationships.

Prisma is used for database access, with a separate Prisma schema for Turso.

## Assets

Cover assets are cached and served through Vercel Blob and app routes. The system includes scripts and admin tools for cover repair, migration, and auditing.

## Search And Catalog Work

Search combines structured issue data, character mappings, publisher data, and normalized slugs. Import and repair scripts help manage inconsistent comic catalog data.

## SEO Architecture

The SEO strategy prioritizes canonical guide pages:

- Strong character pages use `/character/[slug]`.
- Deprecated character intent subpages redirect to anchors.
- Sitemap excludes thin generated character subroutes.
- Thin or incomplete pages can be excluded or marked noindex.
- Landing pages connect users and crawlers to the strongest guides.

## Deployment

The app is deployed on Vercel and uses production environment variables for database, authentication, payment, and asset services.

## Operational Tooling

The project includes scripts and admin routes for:

- Data import
- Cover caching
- Catalog audits
- Key issue expansion
- First appearance checks
- Smoke tests
- Admin search and repair workflows
