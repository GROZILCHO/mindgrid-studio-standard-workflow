# Project Rules

Status: Draft

## Purpose

Defines the rules Codex, ChatGPT, and human operators must follow during `[Project Name]`.

## Usage Notes

- Codex must stop if a task conflicts with these rules.
- Update when access, backup, staging, platform, content, design, SEO, validation, or deployment rules change.

## Operating Rules

- GitHub is source of truth for code/docs.
- WordPress admin/database state must be verified separately.
- Notion is operations layer.
- Codex must follow AGENTS.md.
- Rosen / MindGrid Studio makes final decisions.

## File / Scope Rules

- Always check `git status --short` before file work.
- Work only in allowed files.
- Stop if forbidden files need changes.
- Do not modify unrelated files.
- Do not create theme/plugin files unless explicitly requested.
- File-based Codex tasks must include allowed files and rollback notes.

## Content Rules

- Do not invent claims, metrics, certifications, awards, or partnerships.
- Keep language consistent.
- Avoid placeholder text in release candidates.
- WordPress admin content should match documented page intent.

## Design Rules

- Follow approved design system.
- Do not invent colors, typography, spacing, or layout patterns.
- Avoid mixing multiple visual systems.
- Elementor/Gutenberg/global theme styles must be documented when used.

## Route / SEO Rules

- Do not invent pages/slugs/routes.
- Maintain approved site structure.
- Do not change SEO plugin settings unless requested.
- Keep sitemap/canonical alignment.
- Avoid accidental noindex.
- Document redirects.

## Image / Asset Rules

- Use IMAGE_ASSET_REGISTER.md when images are involved.
- Do not upload duplicate generic media unless intentional.
- Use semantic filenames where possible.
- Use localized alt text in WordPress media.
- Do not rely on external fallback images without approval.

## WordPress Validation Rules

- Confirm admin access when admin state is involved.
- Confirm staging/backup before risky work.
- Confirm plugin/theme behavior manually when needed.
- Browser-only checks must be marked as browser-only.
- Do not claim production readiness without required checks.

## Backup / Staging Rules

- Do not treat WordPress as only files.
- Do not assume database/admin state is visible in GitHub.
- Do not update plugins blindly.
- Do not change WooCommerce-related files/settings without explicit scope.
- Do not modify production-sensitive files without backup/staging context.
- Do not invent plugin settings.
- Do not assume Elementor layouts unless exported.

## Stop Conditions

- Dirty worktree outside expected scope.
- Backup missing for risky work.
- Staging unavailable for risky work.
- Required access missing.
- Forbidden file needs edit.
- Database/admin state is required but unavailable.
- WooCommerce risk appears.
- Validation fails.

