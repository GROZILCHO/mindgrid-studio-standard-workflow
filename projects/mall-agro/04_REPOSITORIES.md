# Repository Registry - Mall Agro Redesign

## Repositories

| Repository | Role | URL | Branch Information | Source-Of-Truth Responsibility |
| --- | --- | --- | --- | --- |
| `mall-agro-redesign` | Application repository | `https://github.com/GROZILCHO/mall-agro-redesign.git` | Main branch implied by source report context; HEAD reported as `ac4c20f docs: add grain processing public copy map` | Application source, assets, routes, builds, validation, detailed project docs, Git history, releases. |
| `mindgrid-studio-standard-workflow` | Central workflow / PMO repository | `https://github.com/GROZILCHO/mindgrid-studio-standard-workflow.git` | `main` | Workflow rules, templates, governance, PMO package, cross-project operating model. |

## Important Application Documentation Paths

- `AGENTS.md`
- `docs/PROJECT_RULES.md`
- `docs/BRAND_POSITIONING.md`
- `docs/SITE_STRUCTURE.md`
- `docs/CONTENT_MODEL.md`
- `docs/DEPLOYMENT_GUIDE.md`
- `docs/SEO_PLAN.md`
- `docs/CURRENT_STATUS.md`
- `docs/PROJECT_HANDOFF.md`
- `docs/NEXT_ACTIONS.md`
- `docs/DECISIONS_LOG.md`
- `docs/ISSUES_LOG.md`
- `docs/HOMEPAGE_*`
- `docs/HOMEPAGE_VISUAL_HIERARCHY_EVIDENCE_STRATEGY.md`
- `docs/editorial/EDITORIAL_PLAYBOOK.md`
- `docs/editorial/AGRICULTURE_CATEGORY_GOLDEN_MASTER_v2.0.md`
- `docs/editorial/AGRICULTURE_PUBLIC_PAGE_COPY_MAP_v1.1.md`
- `docs/editorial/GRAIN_PROCESSING_CATEGORY_GOLDEN_MASTER_v1.0.md`
- `docs/editorial/GRAIN_PROCESSING_PUBLIC_PAGE_COPY_MAP_v1.0.md`
- `src/lib/content/categoryPages.js`
- `src/lib/content/categories.js`
- `src/lib/routes/siteRoutes.js`
- `src/lib/routes/routePairs.js`
- `src/lib/routes/languageUrls.js`
- `src/app/products/components/CategoryLandingPage.js`

## Repository Rules

- The application repository is authoritative for implementation.
- This PMO package must not copy application code.
- This PMO package must not copy full editorial docs, terminal logs, route inventories, or Git history.
- Local Windows paths may be useful in a live session, but they are not durable project requirements and are not recorded here.
- Do not store secrets, credentials, tokens, private access data, or deployment credentials.

