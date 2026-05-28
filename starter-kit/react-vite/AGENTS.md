# React/Vite Project AGENTS

Status: Draft

## Purpose

This file defines Codex rules for React/Vite projects.

## Operating Rules

Codex must:

- Inspect AGENTS.md and docs before changes.
- Not invent routes.
- Not invent design tokens.
- Not alter SEO unless requested.
- Not alter image paths unless requested.
- Not mix performance, design, content, and SEO changes unless explicitly allowed.
- Run validation commands when relevant.
- Report build/typecheck results.
- Never commit deployment ZIPs.
- Stop if hydration, route, SEO, or deployment risks are found.

## Typical Validation Commands

```cmd
npx.cmd tsc --noEmit
npm.cmd run build
```

Exact commands may differ by project. Use the project README.md, package.json scripts, and DEPLOYMENT_GUIDE.md when available.

## Required Context Files

Inspect these files when relevant:

- docs/PROJECT_BRIEF.md
- docs/PROJECT_RULES.md
- docs/SITE_STRUCTURE.md
- docs/DESIGN_SYSTEM.md
- docs/SEO_PLAN.md
- docs/IMAGE_ASSET_REGISTER.md
- docs/CURRENT_STATUS.md
- docs/ISSUES_LOG.md
- docs/DEPLOYMENT_GUIDE.md

## Stop Conditions

Stop and report if:

- Route structure is unclear.
- SEO map conflicts with routes.
- Hydration risk is found.
- Build/typecheck fails.
- Forbidden files need changes.
- Deployment target is unclear.

