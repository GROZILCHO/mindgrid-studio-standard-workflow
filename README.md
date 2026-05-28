# MindGrid Studio Standard Workflow

## Purpose

This repository is the reusable workflow and starter documentation system for MindGrid Studio web projects.

Status: Draft

## What This Repository Is

MindGrid Studio Standard Workflow v1.0 is a documentation-first operating system for planning, building, validating, launching, and reviewing web projects.

It is not an application repository. It contains workflow documents, templates, prompts, checklists, starter-kit documentation, and platform notes that can be reused when creating project-specific repositories.

## When To Use It

Use this repository when starting a new MindGrid Studio web project, preparing a project handoff, writing a Codex task, auditing a project, or standardizing documentation before implementation begins.

Use the templates as starting points, then copy the relevant project docs into the real project repository.

## Operating Roles

- Rosen / MindGrid Studio: project owner and operator. Defines business goals, approves direction, and owns final project decisions.
- ChatGPT Lead Assistant: strategist, planner, QA guide, and Codex prompt author. Helps turn goals into scoped plans and implementation prompts.
- Codex: implementation developer. Works through repository files, completes narrow tasks, validates changes, and reports files changed, validation, risks, and git status.

## Variant B Model

This repository follows Variant B:

- One master workflow repository stores the reusable process, templates, prompts, and checklists.
- Starter-kit folders provide reusable documentation packs for general, React/Vite, and WordPress projects.
- Real client or product projects receive copied/adapted documentation from this repository rather than changing the master workflow for every project.

## Recommended Project Start Sequence

1. Review `workflow/MINDGRID_STUDIO_STANDARD_WORKFLOW_v1.0.md`.
2. Create project docs from `templates/PROJECT_BRIEF.template.md` and `templates/PROJECT_RULES.template.md`.
3. Choose the closest starter kit from `starter-kit/`.
4. Fill `CURRENT_STATUS.md`, `NEXT_ACTIONS.md`, and any immediate `ISSUES_LOG.md` entries in the project repository.
5. Use `prompts/CODEX_TASK_TEMPLATE.md` to create the first narrow Codex task.
6. Validate the first task and update tracking docs only when project state changes.

## Placeholder Sections

- Starter-kit copy workflow
- Project archive workflow
- Versioning policy
- Example project references

