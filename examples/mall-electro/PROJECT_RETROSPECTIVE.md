# Mall Electro Project Retrospective Example

Status: Draft

## Purpose

This is an example/reference retrospective based on Mall Electro as a practical case study for MindGrid Studio Standard Workflow. It shows how a completed or mature project can produce reusable process lessons without making future projects dependent on Mall Electro.

## Project Summary

| Field | Example Notes |
|---|---|
| Project | Mall Electro |
| Project Type | React/Vite website project |
| Primary Learning Value | Workflow control, image governance, performance QA, deployment QA, and AI-assisted implementation discipline |
| Main Actors | Rosen / MindGrid Studio, ChatGPT Lead Assistant, Codex |
| Source of Truth | GitHub |
| Operations Layer | Notion where useful |
| Final Status | Reference case study for future workflow development |

## What Went Well

- GitHub became the durable project memory for docs, implementation files, decisions, and handoff context.
- AGENTS.md helped define how Codex should behave inside the repository.
- Narrow Codex tasks reduced accidental drift across routes, SEO, visuals, and content.
- Read-only audits helped identify issues before implementation tasks began.
- Tracking docs such as CURRENT_STATUS.md, NEXT_ACTIONS.md, ISSUES_LOG.md, DECISIONS_LOG.md, and PROJECT_HANDOFF.md improved continuity.
- The project exposed reusable patterns for React/Vite static deployment, prerender checks, `.htaccess`, sitemap, robots, AVIF/WebP, and console QA.

## What Caused Friction

- Long chat context became unreliable as the project grew.
- Visual asset generation created folder, naming, and role ambiguity.
- Runtime PageHero images, optimized derivatives, and SEO `ogImage` updates needed separate task boundaries.
- Repeated visual motifs across pages created a later cleanup task.
- Mixed-language UI labels required QA attention.
- Performance work required a dedicated sprint rather than being treated as a small polish task.
- Deployment checks needed to account for hosting behavior, direct route refresh, compression, and MIME types.

## Decisions That Became Standards

| Decision | Why It Worked | Should Become Standard? | Notes |
|---|---|---|---|
| Start with structure before code. | Prevented routes, content, and design from drifting during implementation. | Yes | PROJECT_BRIEF.md, PROJECT_RULES.md, and SITE_STRUCTURE.md should exist before implementation. |
| Use GitHub as project memory. | Allowed ChatGPT Lead Assistant and Codex to resume from files instead of chat memory. | Yes | Notion remains operational, not the implementation source of truth. |
| Keep Codex tasks narrow. | Reduced unintended changes and made validation easier. | Yes | Allowed files, forbidden files, validation, and output requirements should be explicit. |
| Separate audit and implementation. | Made risks visible before changes were made. | Yes | Useful for route, SEO, asset, performance, and deployment work. |
| Plan visual assets before implementation. | Reduced image repetition and broken-path risk. | Yes | IMAGE_ASSET_REGISTER.md should be used early. |
| Run post-deploy checks. | Caught issues that local validation cannot prove. | Yes | DEPLOYMENT_GUIDE.md and QA_CHECKLIST.md should include live checks. |

## Issues To Prevent Next Time

| Issue | Root Cause | Prevention Rule | Related Workflow File |
|---|---|---|---|
| Route or SEO drift | Implementation before route/SEO structure is stable | Complete SITE_STRUCTURE.md and SEO_PLAN.md before route tasks | SITE_STRUCTURE.md, SEO_PLAN.md |
| Image folder ambiguity | Assets generated before governance was clear | Define image roles, folders, filenames, and statuses first | IMAGE_ASSET_REGISTER.md |
| Repeated generic visuals | Images were placed before a full visual usage audit | Add visual repetition review before release | VISUAL_QA_CHECKLIST.md |
| Mixed-language labels | UI label QA happened late | Add language consistency to content and visual QA | CONTENT_MODEL.md, QA_CHECKLIST.md |
| Performance surprises | Performance sprint started after many implementation decisions | Plan performance QA earlier for React/Vite projects | REACT_VITE_WORKFLOW.md |
| Chat context overload | Too much project memory lived in conversation | Use CURRENT_STATUS.md and PROJECT_HANDOFF.md before context breaks | CURRENT_STATUS.md, PROJECT_HANDOFF.md |

## Multilingual Localization Phase Retrospective

### Validated Project Result

Mall Electro completed 24 mapped BG/EN/RO public page groups on a dedicated localization branch before merging the validated result into `main`. The final static output contained 76 prerendered route files and 75 sitemap URLs: 27 BG, 24 EN, and 24 RO. Approved mapped pages used reciprocal BG/EN/RO hreflang and self-referencing canonicals. BG-only legal pages remained without fabricated EN/RO alternatives.

This result is project evidence, not a universal route-count target. Future projects should define and validate their own explicit locale route registry and expected output counts.

### Batch-Based Localization

Page-by-page translation created excessive cycles of translation, reporting, external review, verification, and context recovery. The Romanian phase became more efficient when work was grouped into structurally related batches:

1. Repository and localization inventory.
2. Shared and overview content.
3. Service and solution detail content.
4. Industry detail content.
5. Controlled runtime preview.
6. Language switcher activation.
7. Editorial QA and public SEO activation.

Recommended standard: translate by related content models, not one page per Codex task. Run one complete validation suite and produce one report per batch. Use smaller tasks only for isolated blockers or defects that carry disproportionate risk.

### Content Before Activation

The safe sequence was to create locale content while routes remained inactive, verify structural parity, complete every approved content group, then expose runtime routes under `noindex, follow`. Browser QA and language-switch parity were completed before sitemap, hreflang, and public indexing were enabled.

Recommended standard: do not combine initial translation, runtime activation, switcher exposure, and public SEO activation in one uncontrolled task. Treat content readiness, runtime preview, navigation exposure, and indexing as separate gates.

### Locale-Neutral Route And SEO Architecture

One locale-neutral route key per conceptual page allowed BG, EN, and RO paths to remain equivalent without forcing identical slugs. Locale-specific paths and SEO values remained explicit. SEO lookup had to be locale-aware rather than selecting the first metadata entry that shared a conceptual page key.

An earlier defect showed why static inspection alone is insufficient: generated HTML titles were correct, but hydration could rewrite `document.title` from a wrong-locale fallback. The fix and verification required both generated HTML inspection and hydrated runtime checks.

Recommended standard: use shared conceptual route keys, explicit localized path mappings, and locale-aware SEO registry entries. Validate the generated `<title>` and canonical output as well as runtime `document.title` after hydration.

### Content Parity And Output Guards

The content parity guard checked missing locale files, missing keys, array-length mismatches, empty strings, suspicious untranslated source text, Cyrillic or invalid Romanian diacritics, wrong-locale internal links, and missing image assets. It ran before locale activation and after editorial changes.

The generated-output guard used an explicit allowlist and checked exact route and sitemap counts, reciprocal hreflang, self-referencing canonicals, legal-page exclusions, robots directives, internal routes, anchors, assets, and SSR fallback behavior.

Recommended standard: add structural content parity before activating a locale, then validate generated output against the approved route registry. Never treat every path under a locale prefix as automatically valid.

### Controlled Noindex Preview And Switcher Parity

Romanian routes were first rendered with visible RO content while remaining absent from the sitemap and hreflang output, hidden from the public language switcher, and protected by `noindex, follow`. After route, content, browser, and structural QA, RO was added to the switcher. Editorial QA then preceded removal of noindex and activation of sitemap and hreflang.

Every switchable conceptual page had a valid BG/EN/RO target before RO became visible. Legal pages stayed BG-only because approved translations did not exist.

Recommended standard: use a controlled noindex preview when runtime review must precede public search activation. Never fabricate legal translations or redirect an unavailable legal locale to an unrelated overview page.

### Codex Budget Mode And Session Recovery

Larger guarded tasks were more efficient than repeated microtasks when they included explicit scope, allowed and forbidden files, exact output expectations, full-batch validation, and one final report. This approach is safe only when the architecture and automated guards make the batch testable.

When the final RO task was interrupted, the continuation did not reset the repository. The recovery sequence was:

1. Inspect `git status` and `git diff`.
2. Classify existing edits against the interrupted task.
3. Preserve valid partial work.
4. Continue with the original completion criteria.
5. Rerun the entire final validation suite.

Recommended standard: never run `git reset --hard`, `git restore .`, or `git clean -fd` before classifying interrupted work. Use one explicit continuation task and repeat all final gates.

### Branch, Merge, And Manual QA

The localization phase used a dedicated feature branch while `main` remained stable. Content foundation and activation stages were committed separately. The final validated branch was merged with `--no-ff`, then rebuilt and checked on `main` before push.

Automated guards did not replace manual review of browser tab titles, responsive navigation, switcher visibility, hero images, CTA wrapping, card alignment, overflow, or hydration behavior.

Recommended standard: isolate major localization work on a feature branch, validate before and after merge, inspect generated HTML, and perform hydrated browser QA at representative desktop, tablet, and mobile widths.

## Reusable Assets / Templates Created

- Codex task and audit templates.
- Project tracking document templates.
- React/Vite workflow guidance.
- WordPress workflow guidance.
- QA and deployment checklists.
- Image asset governance patterns.
- Notion operations mapping.
- Starter-kit project docs for general, React/Vite, and WordPress projects.

## Workflow Improvement Actions

| Action | Priority | Owner | Target File / Area | Status |
|---|---|---|---|---|
| Convert project lessons into the master workflow. | High | ChatGPT Lead Assistant / Codex | workflow/ | Done |
| Add React/Vite-specific deployment and performance guidance. | High | Codex | platform-workflows/REACT_VITE_WORKFLOW.md | Done |
| Add image asset governance to starter docs. | High | Codex | IMAGE_ASSET_REGISTER.md | Done |
| Add audit-only Codex template. | High | Codex | prompts/CODEX_AUDIT_TEMPLATE.md | Done |
| Keep future examples as references, not dependencies. | Medium | Rosen / MindGrid Studio | examples/ | Planned |

## Final Lessons

- Do not start with code.
- Do not rely on a single long chat.
- Do not treat generated images as implementation-ready without governance.
- Do not merge audit, design, SEO, performance, and deployment into one broad task.
- Start with structure, documents, decisions, and controlled execution.
- Keep GitHub as the project memory and use Notion for operational visibility.
