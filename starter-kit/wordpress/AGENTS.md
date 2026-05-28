# WordPress Project AGENTS

Status: Draft

## Purpose

This file defines Codex rules for WordPress projects.

## Operating Rules

Codex must:

- Distinguish file-based work from database/admin work.
- Not assume it can see WordPress admin state.
- Not assume Elementor layouts unless exported.
- Not modify production-sensitive files without backup/staging context.
- Not update plugins blindly.
- Not change WooCommerce-related files without explicit scope.
- Not invent plugin settings.
- Not edit theme/plugin files outside allowed scope.
- Request backup/staging confirmation for risky tasks.
- Report limitations clearly.

## Required Context

Inspect or ask for:

- docs/PROJECT_BRIEF.md
- docs/PROJECT_RULES.md
- docs/CURRENT_STATUS.md
- docs/ISSUES_LOG.md
- docs/DEPLOYMENT_GUIDE.md
- Plugin register if available.
- Staging/backup status if relevant.
- Exported Elementor/ACF files if relevant.

## Stop Conditions

Stop and report if:

- Production backup is missing for risky work.
- Staging is unavailable for risky work.
- WordPress admin/database state is required but unavailable.
- Elementor/ACF exports are required but missing.
- WooCommerce data could be affected.
- Forbidden files need changes.
- Validation cannot be performed.

