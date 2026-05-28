# Project Rules

Status: Draft

## Purpose

This document defines the rules Codex, ChatGPT, and human operators must follow during the project.

## Usage Notes

- Treat this file as the project-specific rule layer.
- Update when scope, platform, content, design, SEO, validation, or deployment rules change.
- Codex tasks should respect these rules and stop if a request conflicts with them.

## 1. Operating Rules

- GitHub is source of truth.
- Notion is operations layer.
- Codex must follow AGENTS.md.
- ChatGPT Lead Assistant prepares scoped tasks.
- Rosen / MindGrid Studio makes final decisions.
- Do not rely only on chat memory.
- Update tracking docs when required.

## 2. File And Scope Rules

- Always check `git status --short` before work.
- Work only in allowed files.
- Stop if forbidden files need changes.
- Do not modify unrelated files.
- Do not mix unrelated tasks.
- Do not commit deployment ZIPs or temporary files.
- Do not create new folders unless explicitly requested.

## 3. Content Rules

- Do not invent claims.
- Do not add unsupported numbers or guarantees.
- Do not invent certifications, awards, or partnerships.
- Keep language consistent.
- Avoid placeholder text in release candidates.
- Technical terms may stay in English when appropriate.
- All visible UI labels must match the project language unless intentionally approved.

## 4. Design Rules

- Follow approved design system.
- Do not invent colors.
- Do not invent typography.
- Do not invent spacing/layout patterns.
- Reuse approved components.
- Avoid one-off visual drift.
- Mobile behavior must be considered.

## 5. Route And SEO Rules

- Do not invent routes.
- Maintain approved route map.
- Keep sitemap/canonical alignment.
- Do not change SEO metadata unless requested.
- Avoid accidental noindex.
- Redirects must be documented.
- Open Graph images must resolve.

## 6. Image/Asset Rules

- Use IMAGE_ASSET_REGISTER.md when images are involved.
- Do not use external fallback images without approval.
- Use semantic filenames.
- Use localized alt text.
- Avoid repeated generic images unless intentional.
- Optimized derivatives must exist where required.
- Do not move assets without mapping.

## 7. Validation Rules

- Define validation per task.
- React/Vite tasks may require typecheck/build.
- WordPress tasks may require backup/staging/manual QA.
- Browser-only checks must be marked as browser-only.
- Do not claim production readiness without required checks.

## 8. Stop Conditions

Stop and report if:

- Dirty worktree outside expected scope.
- Unclear goal.
- Missing required context.
- Forbidden file needs edit.
- Validation fails.
- Production risk appears.
- SEO/route/design drift appears.
- Credentials/access missing.
- Backup missing for risky WordPress work.

