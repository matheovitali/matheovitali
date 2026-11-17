# CBienLà — Real estate web and mobile platform

[Back to profile](../README.md) · [Product website](https://cbienla.fr)

**Team project · Full-stack product engineering · Source code private**

## Context

CBienLà is a real-estate platform developed with a team of five. The product brings together web and mobile experiences with shared backend services, integrations and tools for managing business workflows.

My involvement has included full-stack engineering and automation across the product. This is **team work, not a claim of sole ownership**.

## Technology

| Layer | Technologies |
| --- | --- |
| Web | Nuxt 4, Vue 3, TypeScript |
| Mobile | Flutter, Dart |
| Backend | Firebase Cloud Functions, Node.js / TypeScript |
| Data & authentication | Firebase and Cloud Firestore |
| Delivery | GitHub Actions and automated checks |
| Integrations | External real-estate feeds and third-party services |

## Engineering areas

**Multi-client consistency.** Web and Flutter clients connect to shared data and business operations. Changes need consistent behavior across platforms and clear boundaries between the interface, backend and data rules.

**Data ingestion.** Integrations import and normalize external property-related information. This work entails validating incoming data, managing incomplete fields and handling differences between source formats.

**Business workflows.** The platform supports operational features such as lead-management and administrative flows, requiring authorization checks and predictable state updates.

**Delivery and maintenance.** Engineering includes CI/CD, debugging, validation and incremental changes in an active multi-contributor repository.

## Simplified system view

This is a **portfolio-level illustration**, not an exact diagram of internal infrastructure or security controls.

```mermaid
flowchart LR
  Web[Nuxt / Vue web client] --> Services[Firebase-backed services]
  Mobile[Flutter mobile client] --> Services
  Services --> Store[(Cloud Firestore)]
  Feed[External property feeds] --> Import[Import and normalization workflows]
  Import --> Store
```

### Explore the live product

These links lead to **real public pages** of the product rather than mockups or screenshots. They illustrate the current user-facing experience; they do **not** establish which individual teammate implemented each feature.

| Public page | What to look for |
| --- | --- |
| [Homepage and property search](https://cbienla.fr/) | Search entry point, listings and property discovery |
| [Browse properties by region](https://cbienla.fr/immobilier) | Hierarchical regional discovery and navigation |
| [Professional directory](https://cbienla.fr/professionals) | Search and category filters for real-estate professionals |
| [About the platform](https://cbienla.fr/qui-sommes-nous) | Public product and team context |

### Screenshots and supporting media

**No screenshots are included yet.** The product website contains third-party listings, photos, personal profile information and brand assets, which must not automatically be republished in a developer portfolio. Any future media must be authorized by the relevant rights holders, based on real app screens, and checked for personal or sensitive content.

A suitable approved set would show (1) the homepage search UI, (2) a regional-discovery page and (3) the directory filters **with visible personal information and copyrighted listing images excluded or appropriately cleared**.

**Private work:** source history, back-office flows and integration code are intentionally not published here.

## What this case study demonstrates

- Working with an interconnected **web + mobile + serverless** codebase
- Practical experience with TypeScript, Vue/Nuxt, Flutter and Firebase
- Navigating complex product workflows and external data integrations
- Collaborating within a small product team, including testing and delivery

## Scope and verification

The [product website](https://cbienla.fr) is a public entry point. **The private source code, client information, internal architecture specifics and operational credentials are intentionally not included.** This document is a high-level technical overview, not an independent security audit or a claim of publicly verified performance.

Additional sanitized screenshots or architecture diagrams may be added after review of ownership and confidentiality constraints.
