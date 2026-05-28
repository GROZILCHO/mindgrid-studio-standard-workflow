# Mall Electro Performance Sprint Example

Status: Draft

## Purpose

This is an example/reference performance sprint summary based on Mall Electro as a React/Vite case study. It shows how performance work can be planned, scoped, validated, and converted into reusable workflow lessons.

This document is not a universal performance recipe. Future projects should adapt the checks to their platform, hosting, route count, asset volume, and deployment method.

## Initial Symptoms / Observations

- The project needed a dedicated performance pass after feature and content work.
- The main JavaScript bundle required review because route-level behavior affected initial load.
- Prerendered output required hydration checks.
- Image format and optimized derivative handling affected runtime performance and deployment QA.
- Deployment server behavior for `.htaccess`, AVIF/WebP MIME types, Brotli/Gzip, sitemap, robots, and direct route refresh needed verification.
- Lighthouse results needed to be gathered in a clean browser context to avoid extension noise.

## Scope

| Area | Included | Notes |
|---|---|---|
| JavaScript bundle | Yes | Review route-level imports and splitting opportunities. |
| Hydration | Yes | Confirm prerendered HTML and client rendering stay consistent. |
| Images | Yes | Check optimized derivatives, AVIF/WebP paths, and runtime usage. |
| Fonts | Yes | Review font loading strategy and render behavior. |
| Server config | Yes | Check `.htaccess`, compression, MIME types, and direct route refresh. |
| SEO files | Yes | Confirm sitemap and robots survive deployment packaging. |
| Visual redesign | No | Visual changes should stay separate from performance tasks unless required. |

## Actions Taken

- Reviewed route-level bundle behavior and identified where eager imports could increase initial JavaScript.
- Used route-level code splitting as a performance direction where appropriate.
- Checked hydration behavior and treated `hydrateRoot` versus `createRoot` as a React/Vite prerender decision.
- Reviewed font loading to reduce avoidable render delay.
- Checked image optimization workflow and runtime paths for AVIF/WebP derivatives.
- Verified deployment expectations for `.htaccess`, direct route refresh, compression behavior, and asset folders.
- Treated console errors as follow-up issues rather than ignoring them after deploy.

## Validation Performed

| Validation | Result Format | Notes |
|---|---|---|
| Typecheck/build | Pass/fail command output | Required before performance conclusions are trusted. |
| Prerender output | Route count and generated files | Confirms expected static output exists. |
| Runtime route checks | Manual browser checks | Direct refresh is important for static hosting. |
| Asset checks | File existence and browser loading | AVIF/WebP must resolve with correct MIME behavior. |
| Lighthouse/PageSpeed | Clean browser report | Extension-polluted Lighthouse runs are not reliable. |
| Console checks | Browser console review | Hydration errors are blockers. |

## Remaining Risks

- Browser-only checks can miss hosting-specific behavior if run only locally.
- Lighthouse values should be treated as context, not a single absolute truth.
- Compression and MIME behavior depend on hosting configuration.
- Image quality/performance tradeoffs may need Rosen / MindGrid Studio approval.
- Performance fixes can create route, SEO, or visual regressions if tasks are too broad.

## Lessons Learned

- Run audits before implementation so issues are visible before files change.
- Keep performance tasks narrow: bundle, hydration, images, fonts, deployment config, and console errors should not all become one uncontrolled task.
- Validate prerendered React/Vite sites with hydration behavior in mind.
- Avoid shipping all page code on the homepage when route-level splitting is available.
- Do not trust Lighthouse reports from a browser with extensions or unstable state.
- Confirm optimized image derivatives exist before replacing runtime paths.
- Confirm `.htaccess`, sitemap, robots, and asset folders are included in deployment output.

## Follow-up Actions

| Priority | Action | Owner / Actor | Status | Notes |
|---|---|---|---|---|
| High | Record performance checks in QA_CHECKLIST.md. | ChatGPT Lead Assistant / Codex | Done | Helps future projects repeat the sprint. |
| High | Add deployment-specific static hosting checks. | Codex | Done | Covers `.htaccess`, direct refresh, sitemap, robots, and compression. |
| Medium | Keep console error review as a post-deploy task. | Rosen / MindGrid Studio | Planned | Should be tracked in NEXT_ACTIONS.md or ISSUES_LOG.md if issues appear. |
| Medium | Separate image optimization from SEO `ogImage` updates. | ChatGPT Lead Assistant / Codex | Done | Reduces accidental SEO drift. |
