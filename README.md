# WeHeartComics

WeHeartComics is a comic collector intelligence platform I built to help readers and collectors research key issues, first appearances, character guides, market context, and beginner-friendly reading paths.

Live site: https://weheartcomics.app

## What It Does

- Helps collectors research comic key issues and first appearances.
- Builds canonical character guides with first appearance, key issue, reading, and collector context.
- Supports search across characters, issues, publishers, and collector-relevant metadata.
- Provides market-aware collector workflows such as vault tracking, wantlists, alerts, and appraisal tools.
- Turns raw comic catalog data into practical guides for new and experienced collectors.

## Why I Built It

Comic collecting is full of fragmented information: first appearance debates, variant confusion, inconsistent catalog data, shifting market attention, and beginner-unfriendly terminology.

WeHeartComics is designed to make that research easier by combining structured issue data, collector education, market context, and readable guide pages in one place.

## My Role

I designed, built, and shipped the product end to end:

- Product strategy and information architecture
- Full-stack Next.js implementation
- Database modeling and data pipelines
- Comic data normalization and import tooling
- Search, character pages, issue pages, and landing pages
- SEO architecture and sitemap strategy
- Admin tooling, audits, scripts, and QA workflows
- AI-assisted development, debugging, content modeling, and product iteration

## Tech Stack

- Next.js App Router
- React
- TypeScript
- Prisma
- PostgreSQL for user/product data
- Turso/libSQL for catalog-style key issue data
- Vercel deployment
- Vercel Blob for cover assets
- Clerk authentication
- Stripe billing
- AI-assisted engineering and content workflows

## AI-Assisted Development

I used AI tools as a product and engineering multiplier, not just as autocomplete.

AI helped with:

- Planning feature architecture
- Generating and refactoring code
- Debugging production issues
- Writing import, migration, and audit scripts
- Reviewing mobile UX and page layouts
- Creating SEO strategy for canonical character pages
- Turning rough collector data into structured guide content
- Building smoke tests and verification workflows

See [AI workflow](docs/ai-workflow.md) for more detail.

## Selected Product Work

- Consolidated thin programmatic character SEO pages into stronger canonical guides.
- Built key issue and first appearance research flows.
- Created character search and character guide pages.
- Added collector education pages for key issues, reading orders, and collecting basics.
- Built admin tools for catalog repair, canonical character mapping, and cover management.
- Added user workflows for vaults, wantlists, scan tools, and appraisal views.

## Case Study

Read the full product case study: [docs/case-study.md](docs/case-study.md)

## Architecture

Read the technical architecture summary: [docs/architecture.md](docs/architecture.md)

## Note About Source Code

The production repository contains private configuration, integration details, and operational scripts. This public portfolio repo is a sanitized project summary intended for interviews and technical review. Source code samples can be provided selectively on request.
