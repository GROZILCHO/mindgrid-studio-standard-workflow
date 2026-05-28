# Deployment Guide

Status: Draft

## Purpose

Defines the React/Vite deployment method, required checks, rollback plan, and post-deploy validation for `[Project Name]`.

## Usage Notes

- Complete before production deployment.
- Do not store passwords directly.
- Record risky assumptions in ISSUES_LOG.md.

## Deployment Overview

| Field | Value |
| --- | --- |
| Project | [Project Name] |
| Platform | React/Vite |
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
- DNS if relevant: [TBD]
- Analytics/Search Console if relevant: [TBD]

Do not store passwords directly. Note where credentials are managed.

## React/Vite Deployment Notes

- Build command: [TBD]
- Output folder: [dist / TBD]
- Deployment ZIP rules: create from output folder contents, not nested folder.
- Do not upload nested `dist/` folder.
- `.htaccess` required if Apache: [TBD]
- Asset folders: [TBD]
- Optimized images: [TBD]
- Sitemap/robots: [TBD]
- Direct route refresh: [TBD]
- AVIF/WebP MIME check: [TBD]
- Compression check: [TBD]
- Cache behavior check: [TBD]

## Pre-deploy Checklist

- [ ] Git clean.
- [ ] Latest pushed.
- [ ] Typecheck passed.
- [ ] Build passed.
- [ ] Prerender output checked if used.
- [ ] Sitemap/robots checked.
- [ ] Images and optimized derivatives checked.
- [ ] Owner approval confirmed.

## Deployment Steps

1. [TBD]
2. [TBD]
3. [TBD]
4. [TBD]

## Rollback Plan

- Restore previous files: [TBD]
- Revert Git commit: [TBD]
- Restore previous ZIP/package: [TBD]
- Clear cache: [TBD]
- Notify stakeholders: [TBD]

## Post-deploy Validation

- [ ] Homepage.
- [ ] Key pages.
- [ ] Direct refresh.
- [ ] Nav.
- [ ] Forms.
- [ ] Images.
- [ ] AVIF/WebP MIME.
- [ ] Compression.
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

