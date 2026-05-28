# WordPress Project Docs

Status: Draft

## Purpose

This folder contains project documentation copied into a new WordPress MindGrid Studio project before implementation, configuration, migration, or deployment begins.

## Usage Notes

- Use these docs to define project scope, access, backup/staging state, site structure, SEO, content, design, assets, validation, deployment, and handoff context.
- GitHub stores code and documentation.
- WordPress database/admin state must be documented, exported, backed up, or verified separately.
- Notion may track operational tasks, but implementation truth belongs in GitHub docs and verified WordPress state.
- Implementation should not start before PROJECT_BRIEF.md, PROJECT_RULES.md, SITE_STRUCTURE.md, backup/staging status, and access context are established.

## Recommended Reading Order

1. PROJECT_BRIEF.md
2. PROJECT_RULES.md
3. CURRENT_STATUS.md
4. SITE_STRUCTURE.md
5. CONTENT_MODEL.md
6. DESIGN_SYSTEM.md
7. SEO_PLAN.md
8. IMAGE_ASSET_REGISTER.md
9. DEPLOYMENT_GUIDE.md
10. NEXT_ACTIONS.md
11. ISSUES_LOG.md
12. DECISIONS_LOG.md
13. QA_CHECKLIST.md
14. PROJECT_HANDOFF.md

## GitHub Docs And WordPress State

GitHub docs should describe the project rules and durable context. They do not automatically capture WordPress database content, media uploads, Elementor/Gutenberg layouts, plugin settings, users, menus, forms, or WooCommerce orders/products.

WordPress admin/database state should be captured through backups, exports, screenshots, staging notes, or explicit documentation when relevant.

## Relationship To Codex Tasks

Codex should work only on file-based tasks unless WordPress admin/database context is provided and the task is explicitly scoped. Tasks must define allowed files, forbidden files, backup/staging status, validation, and rollback notes.

