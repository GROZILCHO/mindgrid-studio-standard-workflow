# Project Document Templates Summary

Status: Source Pack

## Purpose

Use this as a compact guide to the project documents that preserve implementation context beyond a single chat.

## Document Summary

| Document | Purpose | Minimum Content |
| --- | --- | --- |
| `AGENTS.md` | Defines how Codex and agents behave. | Docs-first rules, scope control, validation expectations, reporting, stop conditions. |
| `PROJECT_BRIEF.md` | Business source of truth. | Identity, offer, audience, goals, scope, content/assets, SEO context, constraints, approvals. |
| `PROJECT_RULES.md` | Project-specific control layer. | Git/file scope, content, design, route/SEO, image, validation, platform, and stop rules. |
| `SITE_STRUCTURE.md` | Approved architecture before route/page work. | Routes or slugs, navigation, page clusters, intent, CTAs, redirects, sitemap/noindex rules. |
| `CONTENT_MODEL.md` | Repeatable content structures. | Page types, content fields, CTA model, claim safety, localization, internal links. |
| `DESIGN_SYSTEM.md` | Prevents visual drift. | Visual direction, colors, typography, spacing, components, responsive rules, accessibility basics. |
| `SEO_PLAN.md` | Controls search visibility decisions. | Search intent, page SEO matrix, metadata, canonicals, sitemap, robots, schema, internal links, OG images. |
| `IMAGE_ASSET_REGISTER.md` | Governs visual assets. | Roles, source/optimized/runtime paths, filenames, status, alt text, optimization, visual QA. |
| `CURRENT_STATUS.md` | Current project snapshot. | Phase, state, completed work, active issues, next task, Git status, last validation, do-not-touch notes. |
| `NEXT_ACTIONS.md` | Prioritized concrete next work. | Priority, action, owner, status, dependency, suggested next prompt/task. |
| `ISSUES_LOG.md` | Captures bugs, blockers, risks, and unresolved questions. | ID, severity, area, description, status, owner, proposed action, resolution notes. |
| `DECISIONS_LOG.md` | Records real decisions, not daily activity. | Date, decision, reason, alternatives, impact, related files/tasks. |
| `PROJECT_HANDOFF.md` | Enables chat/agent continuation. | Summary, phase, completed work, issues, decisions, repo state, next task, inspect-first files, warnings. |
| `DEPLOYMENT_GUIDE.md` | Controls release and rollback. | Hosting, access notes, method, pre-deploy checks, steps, rollback, post-deploy validation. |
| `QA_CHECKLIST.md` | Defines project-specific quality gates. | Route, content, visual, SEO, performance, platform, deployment, and post-launch checks. |
| `PROJECT_RETROSPECTIVE.md` | Captures reusable lessons. | What worked, friction, standards, prevention rules, reusable assets, workflow improvements. |

## Minimum Start Set

Before implementation, create:

- `AGENTS.md`
- `PROJECT_BRIEF.md`
- `PROJECT_RULES.md`
- `SITE_STRUCTURE.md`
- `CURRENT_STATUS.md`
- `NEXT_ACTIONS.md`

Add the remaining docs as project needs become clear. Mark unknowns explicitly instead of guessing.

