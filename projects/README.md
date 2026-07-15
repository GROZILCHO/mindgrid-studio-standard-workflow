# PMO Project Instances

Status: Draft

## Purpose

This folder stores compact operational PMO project instances for active, maintained, or strategically important MindGrid Studio projects.

## Folder Roles

| Folder | Role |
| --- | --- |
| `templates/` | Reusable blank structures and generic templates. |
| `starter-kit/` | Reusable project-start documentation packs copied or adapted into project repositories. |
| `projects/` | Operational PMO project instances with compact continuity, status, decisions, workstreams, repository links, and next actions. |
| `examples/` | Reusable case studies, sanitized lessons, retrospectives, and reference examples. |
| `platform-workflows/` | Platform-specific operating guidance for React/Vite, WordPress, and related project types. |
| External application repositories | Implementation source of truth for application code, assets, technical docs, branches, builds, and releases. |

## Operating Rules

- `projects/` must not become a mirror of every application repository.
- `projects/` stores compact operational continuity and links.
- `projects/` must not duplicate application source code, full terminal logs, full route inventories, or complete project documentation sets.
- `examples/` stores reusable lessons and sanitized reference material.
- External application repositories remain authoritative for implementation.
- Do not store secrets, credentials, tokens, private access data, or durable local-machine requirements.

## Project Index

| Project | Status | Project Repository | PMO Instance | Case Study / Example | Current Phase |
| --- | --- | --- | --- | --- | --- |
| Mestimvsichko MindGrid | Active client-demo / requirements validation | `GROZILCHO/mindgrid-request-system` | `projects/mestimvsichko-mindgrid/` | Not applicable | Client demo / requirements validation |
| Mall Agro Redesign | Active implementation QA needed; Grain Processing work uncommitted in application repository | `GROZILCHO/mall-agro-redesign` | `projects/mall-agro/` | No example package in this task | Grain Processing pre-commit QA |
| Mall Electro | Release-ready in main; production deployment not confirmed here | `GROZILCHO/mall-electro` | `projects/mall-electro/` | `examples/mall-electro/` | Post-localization release readiness |

## PMO v2 Baseline

Use `templates/project-pmo-v2/` as the structural baseline for complex project instances. Create only the files that are operationally useful for the project.
