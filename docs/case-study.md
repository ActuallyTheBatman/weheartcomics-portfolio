# WeHeartComics Case Study

## Problem

Comic collectors often need to answer questions that are simple to ask but hard to research:

- What is the real first appearance of this character?
- Which issues actually matter?
- Is a book important for readers, collectors, or market speculation?
- Where should a beginner start reading?
- Are there variants, facsimiles, reprints, or confusing editions?

Most answers are scattered across marketplaces, wikis, forums, YouTube videos, and auction listings. The result is a high-friction research process, especially for newer collectors.

## Goal

Build a collector-focused web app that combines structured comic data, guide-style content, search, and market context into one approachable product.

The product needed to feel useful for beginners without becoming too shallow for serious collectors.

## Product Strategy

The core product direction became:

- Character-first research pages
- Key issue and first appearance discovery
- Beginner-friendly reading paths
- Collector notes and market context
- Search and browsing surfaces that point users toward stronger guide pages

The site is not meant to index every possible generated page immediately. The strategy is to build a smaller number of useful canonical pages first, then expand quality coverage over time.

## Key Features

### Character Guides

Each character guide is designed to answer:

- Who is this character?
- What is their first appearance?
- Which key issues matter?
- Where should a beginner start?
- What should collectors know?

### Key Issue Pages

Issue pages focus on the collector event that makes a book matter: first appearance, origin, death, return, costume change, major storyline, or market-sensitive event.

### Search

Search is designed around collector intent rather than generic catalog lookup. It helps users jump into characters, issues, and guides.

### Collector Workflows

The app includes workflows for vault tracking, wantlists, appraisal views, alerts, and market-aware collecting.

## SEO Rebuild

One major improvement was consolidating programmatic character subpages into canonical character guide pages.

Old pattern:

- `/character/[slug]`
- `/character/[slug]/first-appearance`
- `/character/[slug]/key-issues`

New pattern:

- `/character/[slug]`
- `/character/[slug]#first-appearance`
- `/character/[slug]#key-issues`

Deprecated subpages now redirect to the canonical page. The sitemap focuses on stronger character pages and excludes thin generated subroutes.

This reduces crawl waste and helps the site look more like a useful collector guide than a large batch of template pages.

## AI Leverage

AI tools helped me operate like a much larger team:

- Engineering copilot for Next.js, React, Prisma, scripts, and route work
- Product partner for feature prioritization and UX decisions
- Data assistant for normalization and quality checks
- SEO reviewer for crawl strategy, canonical tags, and sitemap decisions
- QA assistant for smoke checks, build checks, and browser-flow verification

I still made the product and technical decisions, but AI helped accelerate the work and reduce iteration time.

## Results

The result is a production web app with:

- A live collector-facing product
- Searchable comic intelligence
- Character and key issue guide architecture
- Admin and data tooling
- Deployment on Vercel
- A clearer SEO foundation for future growth

## Lessons Learned

- Programmatic pages need quality thresholds before they belong in a sitemap.
- Collector intent is more valuable than raw catalog volume.
- AI is most useful when used as a collaborator across product, engineering, QA, and content strategy.
- The strongest traffic strategy is fewer, better pages before scaling coverage.
