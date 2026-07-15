# Project Handoff - Mall Agro Redesign

## Business Context

Mall Agro Redesign is a modern B2B equipment catalog and inquiry gateway for agriculture, grain processing/handling, and food industry equipment.

The site should support qualified project and equipment inquiries from agricultural businesses, grain processors/handlers, food industry operators, procurement teams, operations managers, and technical buyers.

## Project Philosophy

- Mall Agro is not being rebuilt as WooCommerce, ecommerce, marketplace, stock portal, or instant quotation system.
- Content should support qualified equipment/project inquiries, not product browsing.
- Old WooCommerce content may be used as source material only; its taxonomy must not become the new information architecture.
- Avoid unsupported claims about official representation, exclusivity, manufacturer partnerships, market leadership, certifications, stock, guaranteed delivery, turnkey/EPC responsibility, exact models/capacities, or instant quotes.

## Accepted Category Model

Approved top-level categories:

- Agriculture
- Grain Processing / Grain Handling
- Food Industry Equipment

Agriculture is accepted as `Agriculture Category Benchmark v1` at commit `80c3e30`.

Category workflow:

1. Golden Master
2. Public Page Copy Map
3. Codex implementation
4. UX refinement

## Localization Model

- `mallagro.com`: English.
- `mallagro.ro`: Romanian.
- Domain-based localization is approved.
- `/ro` route-prefix model is not approved.
- Language switcher must only link approved equivalents; no guessed fallback.

Important contradiction handling:

- Language/domain architecture is approved by DEC-010.
- Hosting and concrete deployment implementation remain unconfirmed.
- Stale deployment documentation must not override DEC-010.

## Current Phase

- Confirmed committed baseline: Agriculture benchmark accepted; homepage v2/refined messaging/visual placeholder system complete; Grain Processing editorial docs committed.
- Active local work from source report: Grain Processing public page copy map implementation is in progress and uncommitted.

## Current Uncommitted Grain Processing State

Last known application repository status from the source report:

```txt
 M src/app/products/components/CategoryLandingPage.js
 M src/lib/content/categoryPages.js
?? grain-processing-local-diff.txt
```

Observed uncommitted work:

- `categoryPages.js` maps Grain Processing public copy into runtime content.
- `CategoryLandingPage.js` adjusts benchmark-style operating context grid behavior and hides public operating-context index labels for agriculture-style layouts.
- `grain-processing-local-diff.txt` is an untracked local diff artifact.

## Immediate Continuity Instructions

- Do not start Food Industry, homepage, product import, SEO runtime, or Romanian runtime work until the dirty Grain Processing state is resolved.
- Treat README boilerplate and stale docs in the application repository as lower priority than accepted decisions and current source evidence.
- Use application repository docs and diffs for implementation evidence.
- Use this PMO package only for compact continuity.

## Do-Not-Touch Guardrails

Do not casually change:

- `src/app/products/components/CategoryLandingPage.js` without shared-route QA.
- Agriculture benchmark content/UX unless a regression is reproduced.
- `src/lib/content/categories.js` IDs, routes, slugs, icons, display order.
- `src/lib/routes/**` route-pair behavior without localization approval.
- `src/app/layout.js` language behavior without deployment/localization architecture approval.
- `public/**` visual assets without an asset task.
- Tailwind tokens/global CSS without a design-system task.
- SEO/runtime/canonical/hreflang/sitemap/robots without a dedicated SEO task.
- Romanian routes/content unless localization scope is explicit.
- Product migration or old WooCommerce taxonomy import.

## Exact Next Safe Task

Run a QA-only pre-commit review of the current uncommitted Grain Processing implementation.

