# Deployment Guide

Status: Draft

## Purpose

Defines the WordPress deployment method, required backups, staging requirements, rollback plan, and post-deploy validation for `[Project Name]`.

## Usage Notes

- Complete before production deployment or migration.
- Do not store passwords directly.
- Record risky assumptions in ISSUES_LOG.md.
- Do not deploy risky WordPress changes without backup/staging context.

## Deployment Overview

| Field | Value |
| --- | --- |
| Project | [Project Name] |
| Platform | WordPress |
| Hosting | [TBD] |
| Production URL | [URL] |
| Staging URL | [URL] |
| Deployment Method | [TBD] |
| Responsible Person | [Owner] |
| Launch Window | [TBD] |

## Access / Credentials Notes

- Hosting/cPanel: [TBD]
- FTP/SFTP: [TBD]
- GitHub: [TBD]
- WordPress admin: [TBD]
- Database/phpMyAdmin: [TBD]
- DNS if relevant: [TBD]
- Analytics/Search Console if relevant: [TBD]

Do not store passwords directly. Note where credentials are managed.

## WordPress Deployment Notes

- Full files backup: [TBD]
- Full database backup: [TBD]
- Media backup: [TBD]
- Theme/plugin upload: [TBD]
- Database migration: [TBD]
- Media migration: [TBD]
- Elementor export/import if relevant: [TBD]
- ACF export/import if relevant: [TBD]
- Forms export/import if relevant: [TBD]
- Permalinks flush: [TBD]
- Cache clear: [TBD]
- Plugin version notes: [TBD]
- WooCommerce order/customer/product risk: [TBD]
- Admin login check: [TBD]
- Form submission test: [TBD]
- SEO plugin output check: [TBD]

## Backup Requirements

- [ ] Full files backup exists.
- [ ] Full database backup exists.
- [ ] Media backup exists.
- [ ] Backup location is known.
- [ ] Restore path is understood.

## Staging Requirements

- [ ] Staging environment exists or is explicitly not needed.
- [ ] Staging was tested if needed.
- [ ] Staging-to-production method is understood.
- [ ] Production-only risks are documented.

## Pre-deploy Checklist

- [ ] Git clean where file changes are involved.
- [ ] Latest changes pushed where relevant.
- [ ] Backup confirmed.
- [ ] Staging approved if used.
- [ ] Theme/plugin changes ready.
- [ ] Database/media migration plan clear.
- [ ] SEO plugin output checked.
- [ ] Owner approval confirmed.

## Deployment Steps

1. [TBD]
2. [TBD]
3. [TBD]
4. [TBD]

## Rollback Plan

- Restore files: [TBD]
- Restore database: [TBD]
- Restore media: [TBD]
- Revert Git commit: [TBD]
- Disable problematic plugin: [TBD]
- Restore previous theme/plugin files: [TBD]
- Clear cache: [TBD]
- Notify stakeholders: [TBD]

## Post-deploy Validation

- [ ] Homepage.
- [ ] Key pages.
- [ ] Menus.
- [ ] Forms.
- [ ] Images/media.
- [ ] Permalinks.
- [ ] Admin login.
- [ ] Cache cleared.
- [ ] Sitemap.
- [ ] Robots.
- [ ] SEO plugin output.
- [ ] WooCommerce flow if relevant.
- [ ] Search Console.
- [ ] Analytics/cookie consent if relevant.

## Deployment Report

| Check | Result | Notes |
| --- | --- | --- |
| [TBD] | Pass/Fail/Not checked | [TBD] |

