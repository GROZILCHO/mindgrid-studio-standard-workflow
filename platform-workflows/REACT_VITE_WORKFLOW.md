# React/Vite Workflow

Status: Draft

## 1. Purpose

This workflow defines how React/Vite websites should be handled inside the MindGrid Studio Standard Workflow.

React/Vite projects are strongly suited for file-based development, GitHub-based memory, Codex implementation, controlled builds, prerender/static output, and static deployment. The repository can store nearly the full implementation truth, which makes the platform a good fit for company websites, product websites, SEO-oriented landing systems, and industrial/corporate sites.

This workflow is based on practical lessons from the Mall Electro project, especially route discipline, prerender/static output, SEO config, sitemap generation, PageHero and image governance, optimized image derivatives, build/typecheck validation, `.htaccess` deployment behavior, performance sprint work, and narrow Codex task scoping.

## 2. Core Principle

React/Vite projects should be treated as structured, file-controlled products.

The repository should contain:

- Source code.
- Route definitions.
- Components.
- SEO config.
- Static assets.
- Optimized assets.
- Deployment rules.
- Documentation.
- QA checklists.
- Current status and handoff files.

GitHub can store nearly the full project truth, unlike WordPress where database, media library, page builder layouts, and plugin settings also matter. If a project decision affects implementation, routing, SEO, assets, deployment, or QA, it should be reflected in repository files.

## 3. What GitHub Should Store

GitHub should store the file-based project system:

- Application source code: React/Vite entry points, app shell, routing, and runtime logic.
- Page components: route-level screens and page-specific content structure.
- Layout components: shared page frames, shells, navigation areas, and footer structure.
- Shared UI components: reusable buttons, cards, CTAs, sections, forms, and content blocks.
- Route definitions: app routes, redirects where file-based, and route maps in docs.
- SEO configuration: central route metadata such as titles, descriptions, canonical paths, Open Graph images, robots directives, and schema references.
- Sitemap/robots generation scripts: repeatable generation logic for public canonical routes.
- Image source assets when appropriate: original or generated source images if useful and size-appropriate.
- Optimized images when required by deployment: AVIF/WebP/JPEG derivatives used at runtime.
- `.htaccess` or equivalent deployment config: Apache rewrite, cache, compression, MIME, and SPA/static behavior where needed.
- Build scripts: Vite build, prerender, sitemap, image processing, and deployment helper scripts.
- TypeScript config: project compile rules and path behavior.
- Project documentation: operating docs and implementation constraints.
- Content model: page content structure and reusable content decisions.
- Design system notes: layout, typography, color, spacing, and component rules.
- QA checklists: repeatable validation before deployment.
- Deployment guide: build, package, upload, verification, and rollback notes.
- Current status, issues, decisions, and handoff files: durable project memory.

Codex can work very effectively on React/Vite projects because the source of truth is file-based, reviewable, and testable through commands.

## 4. Recommended React/Vite Project Repository Structure

Use a structure that separates source, routes, SEO, assets, scripts, styles, docs, and build output:

```txt
project-name/
├─ README.md
├─ AGENTS.md
├─ package.json
├─ index.html
├─ src or root source files
├─ components/
│  ├─ layout/
│  ├─ shared/
│  ├─ ui/
│  └─ feature-specific/
├─ pages/
│  ├─ services/
│  ├─ solutions/
│  ├─ industries/
│  └─ legal/
├─ seo/
│  └─ seoConfig.ts
├─ scripts/
│  ├─ prerender.mjs
│  └─ other build scripts
├─ assets/
│  ├─ images/
│  ├─ optimized/
│  ├─ icons/
│  ├─ patterns/
│  └─ .htaccess
├─ styles/
├─ docs/
│  ├─ PROJECT_BRIEF.md
│  ├─ PROJECT_RULES.md
│  ├─ SITE_STRUCTURE.md
│  ├─ CONTENT_MODEL.md
│  ├─ DESIGN_SYSTEM.md
│  ├─ SEO_PLAN.md
│  ├─ IMAGE_ASSET_REGISTER.md
│  ├─ QA_CHECKLIST.md
│  ├─ CURRENT_STATUS.md
│  ├─ NEXT_ACTIONS.md
│  ├─ ISSUES_LOG.md
│  ├─ DECISIONS_LOG.md
│  ├─ PROJECT_HANDOFF.md
│  └─ DEPLOYMENT_GUIDE.md
└─ dist/
```

Clarifications:

- `dist/` is build output and usually should not be committed unless the project intentionally stores deploy artifacts.
- Deployment ZIP files should not be committed.
- Generated optimized assets may be committed if the deployment strategy requires them.
- If output artifacts are intentionally stored, the reason must be documented in PROJECT_RULES.md or DEPLOYMENT_GUIDE.md.

## 5. Project Phases For React/Vite

### 1. Project Setup

Purpose: create the repository, copy starter documentation, install or verify the stack, and define operating rules.

Key questions:

- Is this a new site or redesign?
- What deployment target will be used?
- What validation commands exist?
- Which files may Codex edit?

Expected outputs:

- README.md
- AGENTS.md
- PROJECT_RULES.md
- CURRENT_STATUS.md
- DEPLOYMENT_GUIDE.md

Complete when: the repository and baseline docs exist, commands are known, and implementation can begin through scoped tasks.

### 2. Project Intake

Purpose: capture business context, audience, goals, constraints, and launch requirements.

Key questions:

- What is the site for?
- Who is the audience?
- What pages are required?
- What is out of scope?

Expected outputs:

- PROJECT_BRIEF.md
- PROJECT_RULES.md
- CURRENT_STATUS.md

Complete when: the brief and rules are clear enough to prevent Codex from inventing direction.

### 3. Site Architecture

Purpose: define route structure, navigation, page hierarchy, and user journeys.

Key questions:

- What routes are approved?
- What page clusters exist?
- Are redirects needed?
- What should be in the sitemap?

Expected outputs:

- SITE_STRUCTURE.md
- SEO_PLAN.md
- DECISIONS_LOG.md where route decisions are made

Complete when: routes, page purposes, navigation, redirects, and public/canonical status are documented.

### 4. Content Model

Purpose: define content per page, reusable sections, metadata needs, and localization requirements.

Key questions:

- What content belongs on each route?
- What claims are approved?
- Which content should be reusable?
- What language rules apply?

Expected outputs:

- CONTENT_MODEL.md
- SEO_PLAN.md
- PROJECT_RULES.md

Complete when: page content structure and copy boundaries are documented.

### 5. Design System

Purpose: define visual rules, component style, layout behavior, responsive behavior, and design tokens.

Key questions:

- What colors, typography, and spacing are approved?
- What layout patterns should repeat?
- What should not drift between page clusters?

Expected outputs:

- DESIGN_SYSTEM.md
- PROJECT_RULES.md
- DECISIONS_LOG.md where design decisions are made

Complete when: Codex can implement UI without inventing a new visual system.

### 6. Route And SEO Planning

Purpose: connect route structure with SEO metadata, sitemap behavior, robots behavior, canonicals, and Open Graph assets.

Key questions:

- Does every public route have metadata?
- Does every route have a canonical?
- What should be excluded from indexing?
- What image should each route use for sharing?

Expected outputs:

- SITE_STRUCTURE.md
- SEO_PLAN.md
- seoConfig or equivalent central SEO map

Complete when: routes and metadata are aligned and ready for implementation.

### 7. Visual Asset Planning

Purpose: define image requirements before implementation.

Key questions:

- What hero, section, CTA, card, OG, and gallery images are required?
- What source and optimized versions exist?
- What filenames and alt text are approved?

Expected outputs:

- IMAGE_ASSET_REGISTER.md
- DESIGN_SYSTEM.md
- SEO_PLAN.md

Complete when: asset requirements are documented and runtime images are not chosen ad hoc.

### 8. Component Architecture

Purpose: define reusable component patterns before building many pages.

Key questions:

- What layout components are needed?
- What shared CTA/card/page section components exist?
- What page clusters can share templates?

Expected outputs:

- Component plan in docs or implementation notes
- DESIGN_SYSTEM.md updates where needed
- DECISIONS_LOG.md for major architecture decisions

Complete when: the implementation can reuse components without one-off page drift.

### 9. Implementation With Codex

Purpose: execute controlled file-based tasks through narrow prompts.

Key questions:

- What exact change is required?
- Which files are allowed?
- Which files are forbidden?
- What validation proves completion?

Expected outputs:

- Implemented files
- Validation output
- CURRENT_STATUS.md or tracking docs when project state changes

Complete when: the task is implemented, validated, and reported with git status.

### 10. Build / Prerender / Static Output

Purpose: verify the site can build and generate expected static output.

Key questions:

- Does TypeScript pass?
- Does Vite build pass?
- Does prerender generate every expected route?
- Are sitemap, robots, 404, assets, and deployment files present?

Expected outputs:

- Build output
- Prerender audit
- Sitemap/robots output
- QA or deployment notes

Complete when: build and static output match the approved route and deployment plan.

### 11. QA

Purpose: validate routes, links, metadata, images, visuals, language, performance, and console behavior.

Key questions:

- Do all routes open directly and through navigation?
- Are metadata and sitemap correct?
- Are images present and optimized?
- Are there hydration or console errors?

Expected outputs:

- QA_CHECKLIST.md
- ISSUES_LOG.md
- CURRENT_STATUS.md

Complete when: blockers are resolved or explicitly accepted.

### 12. Deployment

Purpose: deploy a known build from a clean state to the hosting environment.

Key questions:

- Is git clean before packaging?
- Is the build validated?
- Is the deployment package correctly structured?
- Is `.htaccess` or equivalent config included?

Expected outputs:

- DEPLOYMENT_GUIDE.md
- Deployment package if intentionally created outside Git
- Post-deployment smoke test notes

Complete when: production is updated, verified, and documented.

### 13. Post-launch

Purpose: verify production behavior and define follow-up work.

Key questions:

- Are sitemap, robots, redirects, forms, tracking, and performance working?
- Are there production-only issues?
- What should be improved next?

Expected outputs:

- CURRENT_STATUS.md
- NEXT_ACTIONS.md
- ISSUES_LOG.md

Complete when: production checks are done and follow-up work is recorded.

### 14. Retrospective

Purpose: capture reusable lessons after launch or a major phase.

Key questions:

- What worked?
- What failed?
- What should change in workflow, templates, prompts, or QA?

Expected outputs:

- PROJECT_RETROSPECTIVE.md
- DECISIONS_LOG.md where workflow decisions are made

Complete when: lessons are documented and reusable improvements are identified.

## 6. React/Vite Intake Questions

Use these questions during intake:

- Is this a new site or redesign?
- Static site or app-like behavior?
- Expected page count?
- Required language structure?
- SEO-critical pages?
- Need prerender/static HTML?
- Need sitemap generation?
- Need robots.txt?
- Need canonical URLs?
- Need Open Graph images?
- Need schema/structured data?
- Hosting environment?
- Deployment method?
- Asset volume?
- Image-heavy site?
- Form handling needed?
- Analytics/tracking needed?
- Cookie consent needed?
- Expected launch deadline?
- Need WordPress/CMS integration or pure static?
- Need future multilingual expansion?

Missing answers that affect implementation should be recorded in ISSUES_LOG.md or NEXT_ACTIONS.md.

## 7. Route Architecture

Routes must be planned before implementation.

Rules:

- Do not invent routes during implementation.
- Maintain a route map in SITE_STRUCTURE.md.
- Every route should have a purpose, SEO intent, and page component.
- Redirects should be documented.
- Old routes should be mapped before deployment.
- 404 behavior should be intentional.
- Sitemap should include only public canonical routes.
- Unprefixed or legacy routes should not appear in the sitemap unless approved.

Route audit expectations:

| Check | Expectation |
| --- | --- |
| App route exists | The route is registered in the app/router. |
| Page component exists | The route resolves to an intentional page component. |
| Internal links resolve | Navigation and inline links do not point to missing pages. |
| Canonical matches route | Metadata canonical path matches the approved route. |
| Sitemap includes route if public | Public canonical routes appear in sitemap.xml. |
| Noindex if needed | Private, temporary, duplicate, or utility routes are excluded or marked appropriately. |

## 8. SEO And Metadata Workflow

React/Vite sites need explicit SEO planning because metadata is often file-controlled.

Use a central `seoConfig` or equivalent SEO map for:

- Title.
- Description.
- Canonical path.
- `ogImage`.
- Robots directives.
- Schema when needed.
- Sitemap generation.
- robots.txt generation.
- Route-level metadata checks.
- Open Graph image mapping.
- Language and canonical consistency.

SEO changes should be scoped and validated separately from visual or layout changes when possible. This reduces the risk of accidental route, metadata, or sitemap drift.

## 9. Component Architecture

Component categories:

- Layout components.
- PageHero / hero systems.
- Shared CTA components.
- Cards.
- Service/solution/industry page layouts.
- Legal/simple page layouts.
- Form components.
- Navigation/footer components.

Rules:

- Reuse existing components.
- Do not invent new style systems.
- Do not create one-off components unless justified.
- Keep page content separated from layout behavior where possible.
- Preserve design system tokens.
- Avoid layout drift across page clusters.

Component changes should be made with awareness of every page cluster that uses the component.

## 10. Visual Asset Workflow For React/Vite

Images must be planned as a system, not added ad hoc.

Rules:

- Use IMAGE_ASSET_REGISTER.md.
- Define semantic folders.
- Avoid repeated generic images.
- Separate source image, optimized image, and runtime usage.
- Define filenames in English.
- Localize alt text.
- Generate AVIF/WebP derivatives where required.
- Verify optimized derivatives exist before runtime replacement.
- Verify MIME types in hosting.
- Avoid external fallback images unless approved.
- Update `ogImage` separately after runtime hero images are stable.

Asset statuses:

| Status | Meaning |
| --- | --- |
| planned | Asset need is known, but source is not ready. |
| generated | Asset exists but is not yet approved. |
| approved-for-optimization | Asset can be processed into runtime derivatives. |
| optimized | Runtime derivatives exist. |
| implemented | Asset is used in code and validated. |
| rejected | Asset should not be used. |
| needs-replacement | Temporary asset is in use or planned for replacement. |

## 11. Build And Prerender Workflow

Expected build validation commands commonly include:

```cmd
npx.cmd tsc --noEmit
npm.cmd run build
```

Build should confirm:

- Vite client build passes.
- SSR/prerender build passes if used.
- Expected route count generated.
- sitemap.xml generated.
- robots.txt generated.
- 404 route generated.
- No unexpected old routes.
- Static assets copied correctly.
- `.htaccess` or deployment config copied correctly if used.

If prerender is used, hydration must be checked carefully. Client render must match prerendered HTML. Hydration errors are deployment blockers.

## 12. Performance Workflow

Practical performance lessons:

- Route-level code splitting should be considered when App imports all pages.
- Hydration should use `hydrateRoot` for prerendered HTML.
- Avoid shipping all page code on the homepage.
- Avoid unnecessary runtime preloads.
- Use responsive image formats.
- Use AVIF/WebP where supported.
- Verify compression headers.
- Use Brotli/Gzip where possible.
- Avoid committing deployment ZIP files.
- Run Lighthouse in a clean/incognito browser.
- Extension-polluted Lighthouse reports are not reliable.
- Track FCP, LCP, TBT, CLS, Speed Index, and transfer size.

Common targets:

- No console errors.
- LCP below 2.5-3.5s depending on project complexity and hosting.
- CLS close to 0.
- No broken images.
- No hydration errors.
- No major render-blocking resources unless justified.

Performance work should be measured before and after changes. Do not mix large visual refactors with performance audits unless explicitly scoped.

## 13. Deployment Workflow

Before deployment:

- Clean git status.
- Successful typecheck.
- Successful build.
- Route/prerender audit.
- Image asset audit.
- Sitemap/robots audit.
- `.htaccess` audit if Apache.
- No accidental ZIP artifacts in Git.

Deployment package:

- Create ZIP from `dist/` contents.
- Upload contents directly to document root.
- Do not upload nested `dist/` directory.
- Do not upload nested ZIP folder.
- Confirm `.htaccess` is included.
- Confirm `assets/`, `images/`, `optimized/`, `bg/`, sitemap, and robots are present where applicable.

After deployment:

- Open key routes.
- Direct refresh key routes.
- Check console errors.
- Check images.
- Check AVIF MIME.
- Check compression.
- Check sitemap.xml.
- Check robots.txt.
- Run Lighthouse.
- Test mobile navigation.
- Test forms if present.

## 14. Codex Role In React/Vite Projects

Codex can do well:

- Inspect repository files.
- Update components.
- Update pages.
- Update SEO config.
- Create route audits.
- Implement controlled image replacements.
- Generate build reports.
- Update docs.
- Prepare deployment checklists.
- Perform narrow refactors.

Codex constraints:

- Must follow AGENTS.md.
- Must inspect docs first.
- Must work only within allowed files.
- Must stop on dirty worktree unless the task allows it.
- Must report validation results.
- Must not make broad unrelated changes.
- Must not invent routes, claims, styles, or folders.
- Must not commit generated ZIPs or accidental files.

Every task should define allowed files, forbidden files, requirements, validation, output required, and stop conditions.

## 15. React/Vite QA Gates

QA gates:

- Route QA.
- Internal link QA.
- Navigation QA.
- Mobile menu QA.
- SEO metadata QA.
- Sitemap/robots QA.
- Image path QA.
- Optimized derivative QA.
- Visual consistency QA.
- Language consistency QA.
- Build/typecheck QA.
- Performance QA.
- Deployment QA.
- Console error QA.

React hydration errors are deployment blockers. Console errors after deployment should be investigated before launch approval.

## 16. Common Failure Patterns

| Failure Pattern | Prevention |
| --- | --- |
| Importing all pages eagerly and creating a large initial bundle | Consider route-level splitting and measure bundle output. |
| Using `createRoot` instead of `hydrateRoot` on prerendered HTML | Match the React entry strategy to prerendered output. |
| Broken optimized image paths | Verify generated derivative paths before replacing runtime images. |
| AVIF served with wrong MIME type | Confirm hosting MIME config and `.htaccess` behavior. |
| Deployment ZIP uploaded with wrong folder nesting | ZIP the contents of `dist/`, not the parent folder. |
| Stale production bundle after local build | Confirm deployment package timestamp and clear cache. |
| Repeated generic images across pages | Use IMAGE_ASSET_REGISTER.md and page-specific asset planning. |
| English UI labels in a localized site | Run language consistency QA. |
| Unsupported claims in CTA copy | Check PROJECT_BRIEF.md, CONTENT_MODEL.md, and approved copy. |
| Accidental untracked files like deployment ZIPs or pasted text artifacts | Check `git status --short` before and after tasks. |
| Git commands run from the wrong directory | Confirm working directory before git operations. |
| Line-ending warnings mistaken for fatal errors | Treat LF/CRLF warnings as warnings unless content changes are unexpected. |
| Console errors ignored after deployment | Make console error QA part of post-deploy checks. |

## 17. Stop Conditions

Codex or the project operator should stop and report if:

- Working tree is dirty unexpectedly.
- Route structure is unclear.
- SEO map conflicts with routes.
- Build fails.
- Typecheck fails.
- Prerender output is missing routes.
- Forbidden files need editing.
- Image derivatives are missing.
- Deployment target is unclear.
- Performance regression appears.
- Hydration or console errors appear.
- Accidental files are found.

## 18. Operating Principle

Plan the structure before coding.
Keep the repository as the source of truth.
Use Codex for narrow controlled implementation.
Validate every build.
Deploy only from a known clean state.
Do not trust memory, browser cache, or assumptions.

