# Deployment Guide

Status: Draft

## Purpose

Defines the deployment method, required checks, rollback plan, and post-deploy validation for `[Project Name]`.

## Usage Notes

- Complete before production deployment.
- Do not store passwords directly.
- Record risky assumptions in ISSUES_LOG.md.

## Deployment Overview

| Field | Value |
| --- | --- |
| Project | [Project Name] |
| Platform | [React/Vite / WordPress / WooCommerce / Static / Other] |
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
- WordPress admin if relevant: [TBD]
- DNS if relevant: [TBD]
- Analytics/Search Console if relevant: [TBD]

Do not store passwords directly. Note where credentials are managed.

## React/Vite Deployment Notes

- Build command: [TBD]
- Output folder: [TBD]
- Deployment ZIP rules: [TBD]
- `.htaccess` rules if Apache: [TBD]
- Asset folders: [TBD]
- Optimized images: [TBD]
- Sitemap/robots: [TBD]
- Direct route refresh: [TBD]
- Compression/MIME checks: [TBD]

## WordPress Deployment Notes

- Backup: [TBD]
- Staging: [TBD]
- Theme/plugin upload: [TBD]
- Database migration: [TBD]
- Media migration: [TBD]
- Elementor/ACF/form exports: [TBD]
- Permalinks flush: [TBD]
- Cache clear: [TBD]
- Plugin version notes: [TBD]
- WooCommerce risk if relevant: [TBD]

## Pre-deploy Checklist

- [ ] Git clean.
- [ ] Latest pushed.
- [ ] Build passed.
- [ ] QA passed.
- [ ] Sitemap/robots checked.
- [ ] Backup confirmed.
- [ ] Owner approval confirmed.

## Deployment Steps

1. [TBD]
2. [TBD]
3. [TBD]
4. [TBD]

## Rollback Plan

- Restore files: [TBD]
- Restore database: [TBD]
- Revert Git commit: [TBD]
- Restore previous ZIP: [TBD]
- Disable problematic plugin: [TBD]
- Clear cache: [TBD]
- Notify stakeholders: [TBD]

## Post-deploy Validation

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

## Deployment Report

| Check | Result | Notes |
| --- | --- | --- |
| [TBD] | Pass/Fail/Not checked | [TBD] |

