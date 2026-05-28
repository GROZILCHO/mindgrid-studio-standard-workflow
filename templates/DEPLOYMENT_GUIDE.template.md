# Deployment Guide

Status: Draft

## Purpose

This document defines the deployment method, required checks, rollback plan, and post-deploy validation for a specific project.

## Usage Notes

- Complete before production deployment.
- Do not store passwords directly in this file.
- Use this with PRE_DEPLOY_CHECKLIST.md and POST_DEPLOY_CHECKLIST.md.
- Record risky deployment assumptions in ISSUES_LOG.md.

## 1. Deployment Overview

| Field | Value |
| --- | --- |
| Project | |
| Platform | |
| Hosting | |
| Production URL | |
| Staging URL | |
| Deployment Method | |
| Responsible Person | |
| Launch Window | |

## 2. Access And Credentials

- Hosting/cPanel:
- FTP/SFTP:
- GitHub:
- WordPress admin if relevant:
- DNS if relevant:
- Analytics/Search Console if relevant:

Do not store passwords directly. Note where credentials are managed.

## 3. React/Vite Deployment Notes

- Build command:
- Output folder:
- Deployment ZIP rules:
- `.htaccess` rules if Apache:
- Asset folders:
- Optimized images:
- Sitemap/robots:
- Direct route refresh:
- Compression/MIME checks:

## 4. WordPress Deployment Notes

- Backup:
- Staging:
- Theme/plugin upload:
- Database migration:
- Media migration:
- Elementor/ACF/form exports:
- Permalinks flush:
- Cache clear:
- Plugin version notes:
- WooCommerce risk if relevant:

## 5. Pre-deploy Checklist

- [ ] Git clean.
- [ ] Latest pushed.
- [ ] Build passed.
- [ ] QA passed.
- [ ] Sitemap/robots checked.
- [ ] Backup confirmed.
- [ ] Owner approval confirmed.

## 6. Deployment Steps

1. Placeholder deployment step.
2. Placeholder deployment step.
3. Placeholder deployment step.
4. Placeholder deployment step.

## 7. Rollback Plan

- Restore files:
- Restore database:
- Revert Git commit:
- Restore previous ZIP:
- Disable problematic plugin:
- Clear cache:
- Notify stakeholders:

## 8. Post-deploy Validation

- [ ] Homepage.
- [ ] Key pages.
- [ ] Direct refresh.
- [ ] Nav.
- [ ] Forms.
- [ ] Images.
- [ ] Sitemap.
- [ ] Robots.
- [ ] Console.
- [ ] Lighthouse/PageSpeed.
- [ ] Search Console.
- [ ] Analytics/cookie consent if relevant.

## 9. Deployment Report

| Check | Result | Notes |
| --- | --- | --- |
| Placeholder | Pass/Fail/Not checked | Placeholder |

