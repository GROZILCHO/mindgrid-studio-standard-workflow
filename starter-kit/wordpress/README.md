# WordPress Project Starter Kit

Status: Draft

## Purpose

This starter kit is used for WordPress, WooCommerce, Elementor, Gutenberg, custom theme, or child theme projects.

## When To Use

Use this starter for:

- WordPress websites.
- WordPress redesigns.
- WooCommerce projects.
- Elementor-based sites.
- Custom theme/child theme projects.
- Plugin/snippet controlled WordPress work.

## WordPress-specific Warning

GitHub can store code and documentation, but it does not fully store database content, media library, page builder layouts, plugin settings, menus, users, forms, or WooCommerce orders/products by default.

WordPress projects need backup, export, staging, and manual QA strategy in addition to GitHub documentation.

## What Must Be Handled Separately

- Database backup.
- Media backup.
- Elementor exports.
- ACF exports.
- Forms exports.
- Plugin settings.
- SEO plugin settings.
- Redirects.
- Staging environment.
- Rollback plan.

## First Project Sequence

1. Confirm access.
2. Confirm backup strategy.
3. Confirm staging.
4. Fill PROJECT_BRIEF.md.
5. Fill PROJECT_RULES.md.
6. Define SITE_STRUCTURE.md.
7. Decide theme/builder strategy.
8. Define plugin register.
9. Assign Codex only to file-based tasks with clear scope.
10. QA on staging before production.

## Reference

See `platform-workflows/WORDPRESS_WORKFLOW.md`.

