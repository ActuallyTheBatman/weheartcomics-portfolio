# Architecture Diagram

```mermaid
flowchart TB
  user["Collectors / Readers"] --> edge["WeHeartComics Web App<br/>Next.js + React"]
  interviewer["Hiring Manager / Public Viewer"] --> portfolio["Public Portfolio Repo<br/>Case Study + Architecture"]

  edge --> pages["Product Surfaces<br/>Character Guides<br/>Key Issues<br/>Search<br/>Vault<br/>Wantlists<br/>Appraisal"]
  edge --> api["Next.js API Routes<br/>Search<br/>Catalog Context<br/>User Workflows<br/>Admin Tools"]

  api --> auth["Clerk<br/>Authentication"]
  api --> billing["Stripe<br/>Subscriptions"]
  api --> appdb["PostgreSQL<br/>Users, Vaults, Settings,<br/>Alerts, Appraisal Data"]
  api --> catalog["Turso / libSQL<br/>Key Issues, Characters,<br/>Series, Publishers"]
  api --> blob["Vercel Blob<br/>Cover Assets"]

  scripts["Operational Scripts<br/>Imports<br/>Migrations<br/>Cover Caching<br/>Audits<br/>Smoke Checks"] --> appdb
  scripts --> catalog
  scripts --> blob

  admin["Admin Workflows<br/>Catalog Repair<br/>Canonical Characters<br/>Cover Management"] --> api

  edge --> seo["SEO Layer<br/>Canonical URLs<br/>301 Redirects<br/>Sitemap<br/>Structured Data<br/>Noindex Rules"]
  seo --> google["Google Search<br/>Crawl + Indexing"]

  ai["AI-Assisted Workflow<br/>Planning<br/>Coding<br/>Debugging<br/>Data Cleanup<br/>SEO Review<br/>QA"] --> edge
  ai --> scripts
  ai --> portfolio
```

## What This Shows

WeHeartComics is structured as a production web application, not a static demo.

The main app runs on Next.js and connects to authentication, billing, app data, catalog data, and asset storage. Operational scripts and admin workflows support the messy parts of comic data maintenance: imports, cover caching, canonical character cleanup, audits, and smoke tests.

The SEO layer is intentional. Character guide pages are treated as canonical collector resources, while thin or duplicate routes are redirected or excluded from the sitemap.

AI tools supported the build across planning, engineering, debugging, content modeling, data cleanup, SEO, and QA.
