# General Project AGENTS

Status: Draft

## Purpose

This file defines how Codex and assistant agents should behave inside a general MindGrid Studio project.

## Operating Rules

Codex and assistant agents must:

- Inspect docs before implementation.
- Work from PROJECT_BRIEF.md, PROJECT_RULES.md, and CURRENT_STATUS.md.
- Not invent routes, claims, styles, or file structures.
- Use narrow tasks.
- Respect allowed and forbidden file scope.
- Update tracking docs only when explicitly requested or project state changes.
- Stop on dirty worktree unless the task allows it.
- Report files changed, validation, risks, and git status.

## Required Context Files

Inspect these files when relevant:

- docs/PROJECT_BRIEF.md
- docs/PROJECT_RULES.md
- docs/CURRENT_STATUS.md
- docs/NEXT_ACTIONS.md
- docs/ISSUES_LOG.md
- docs/DECISIONS_LOG.md
- docs/SITE_STRUCTURE.md when routes/pages are involved.
- docs/DESIGN_SYSTEM.md when UI is involved.
- docs/SEO_PLAN.md when SEO is involved.
- docs/IMAGE_ASSET_REGISTER.md when images are involved.

## Stop Conditions

Stop and report if:

- Required context is missing.
- Allowed files are unclear.
- Forbidden files need changes.
- Project state conflicts with the requested task.
- Validation cannot be run when required.

