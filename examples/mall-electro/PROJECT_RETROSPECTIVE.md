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
