# Changelog

Status: Draft

## Purpose

This file records major MindGrid Studio Standard Workflow repository changes. It is not intended to track every small edit, typo fix, or project-specific task.

Use this changelog to understand how the reusable workflow system evolved, which major documentation systems were added, and when future workflow versions change structure, starter kits, templates, prompts, or operating rules.

## Unreleased / v1.0 Preparation

### Operating Core

- Developed root README and AGENTS operating rules.
- Developed Codex task template.
- Developed Codex audit template.
- Defined docs-first workflow behavior.
- Defined allowed/forbidden file discipline.
- Defined task reporting expectations.
- Defined tracking document update logic.
- Clarified that Codex should not update all tracking docs automatically after every small task.

### Master Workflow

- Developed `workflow/MINDGRID_STUDIO_STANDARD_WORKFLOW_v1.0.md`.
- Defined the Variant B model: master workflow repository plus reusable starter-kit folders.
- Defined roles: Rosen / MindGrid Studio, ChatGPT Lead Assistant, Codex, and optional specialist agents.
- Defined GitHub as the source of truth and shared project memory.
- Defined Notion as the operations and task tracking layer.
- Defined handoff and chat-limit protocol for long-running projects.
- Added guarded logical-batch guidance for efficient Codex execution.
- Added interrupted-session recovery rules that preserve and classify uncommitted work before continuation.

### Workflow Phases

- Developed and aligned 12 individual phase files under `workflow/`.
- Normalized phase filenames to match the 12-phase master model.
- Added Post-launch and Retrospective phases.
- Expanded each phase file with practical sections for purpose, inputs, outputs, recommended steps, agent involvement, tracking updates, completion criteria, stop conditions, and handoff notes.

### Platform Workflows

- Developed React/Vite workflow.
- Developed WordPress workflow.
- Clarified the distinction between file-based React/Vite projects and WordPress projects with database, admin, media, plugin, and page builder state.
- Added React/Vite guidance for route discipline, SEO config, prerender/static output, image optimization, performance, hydration, `.htaccess`, and deployment QA.
- Added a React/Vite multilingual phase gate covering content parity, controlled noindex preview, locale-aware routing and SEO, strict output allowlists, and generated plus hydrated-runtime validation.
- Added WordPress guidance for backups, staging, theme/builder strategy, plugin governance, database/media handling, Elementor/Gutenberg, WooCommerce risk, deployment, and rollback.

### Templates

- Developed core project templates:
  - PROJECT_BRIEF
  - PROJECT_RULES
  - SITE_STRUCTURE
  - CONTENT_MODEL
  - DESIGN_SYSTEM
- Developed launch and governance templates:
  - SEO_PLAN
  - IMAGE_ASSET_REGISTER
  - QA_CHECKLIST
  - DEPLOYMENT_GUIDE
  - PROJECT_RETROSPECTIVE
- Developed operational tracking templates:
  - CURRENT_STATUS
  - NEXT_ACTIONS
  - ISSUES_LOG
  - DECISIONS_LOG
  - PROJECT_HANDOFF

### Checklists

- Developed project start and pre-Codex checklists.
- Developed pre-build, pre-deploy, post-deploy, SEO launch, and visual QA checklists.
- Added stop conditions and validation expectations for controlled project execution.

### Specialist Prompts

- Developed prompts for:
  - ChatGPT Lead Assistant
  - Content Strategist
  - Visual Prompt Designer
  - SEO/AEO Specialist
  - QA / Release Specialist
- Defined specialist behavior, required context, deliverables, must-not-do rules, reporting expectations, and stop conditions.

### Starter Kits

- Developed general starter-kit usage docs.
- Populated general starter-kit project docs.
- Developed React/Vite starter-kit usage docs and project docs.
- Developed WordPress starter-kit usage docs and project docs.
- Clarified that starter kits are documentation/project-start bases, not full application scaffolds.

### Notion Operations

- Developed Notion task mapping.
- Developed task status model.
- Developed project dashboard structure.
- Clarified that Notion supports operational tracking for projects, tasks, owners, deadlines, statuses, issues, and retrospectives.
- Clarified that GitHub remains the implementation source of truth.

### Examples

- Developed Mall Electro example reference documents:
  - decisions log example
  - performance sprint example
  - project retrospective example
  - task summary example
- Clarified that Mall Electro is a case study reference and not a dependency for future projects.
- Captured practical lessons around GitHub memory, Codex scope control, image governance, performance sprints, deployment QA, and audit-first workflow.
- Extended the Mall Electro retrospective with the validated BG/EN/RO localization workflow, failure patterns, guards, branch strategy, and browser QA lessons.

### PMO Project Instances

- Added `projects/README.md` to clarify the roles of `projects/`, `examples/`, `templates/`, `starter-kit/`, `platform-workflows/`, and external application repositories.
- Added `projects/mall-electro/` as a compact operational PMO instance linked to the external Mall Electro application repository and the reusable Mall Electro case study.
- Added `projects/mall-agro/` as the central PMO context package for Mall Agro Redesign, linked to the external application repository without copying implementation source.

## Notes

- This changelog tracks major workflow-system milestones.
- Project-specific changelogs should live inside their own project repositories.
- Future versions should update this file when workflow structure, starter kits, templates, prompts, checklists, platform workflows, or operating rules change.
