# Project Rules

Status: Draft

## Purpose

Defines the rules Codex, ChatGPT, and human operators must follow during `[Project Name]`.

## Usage Notes

- Treat this as the project-specific rule layer.
- Update when scope, platform, content, design, SEO, validation, or deployment rules change.
- Codex must stop if a task conflicts with these rules.

## Operating Rules

- GitHub is source of truth.
- Notion is operations layer.
- Codex must follow AGENTS.md.
- ChatGPT Lead Assistant prepares scoped tasks.
- Rosen / MindGrid Studio makes final decisions.
- Do not rely only on chat memory.
- Update tracking docs when required.

## File / Scope Rules

- Always check `git status --short` before work.
- Work only in allowed files.
- Stop if forbidden files need changes.
- Do not modify unrelated files.
- Do not mix unrelated tasks.
- Do not commit deployment ZIPs or temporary files.
- Do not create folders unless explicitly requested.

## Content Rules

- Do not invent claims.
- Do not add unsupported numbers or guarantees.
- Do not invent certifications, awards, or partnerships.
- Keep language consistent.
- Avoid placeholder text in release candidates.
- Technical terms may stay in English when appropriate.
- UI labels must match project language unless approved.

## Design Rules

- Follow approved design system.
- Do not invent colors.
- Do not invent typography.
- Do not invent spacing/layout patterns.
- Reuse approved components.
- Avoid one-off visual drift.
- Consider mobile behavior.

## Route / SEO Rules

- Do not invent routes.
- Maintain approved route map.
- Keep sitemap/canonical alignment.
- Do not change SEO metadata unless requested.
- Avoid accidental noindex.
- Document redirects.
- Open Graph images must resolve.

## Image / Asset Rules

- Use IMAGE_ASSET_REGISTER.md when images are involved.
- Do not use external fallback images without approval.
- Use semantic filenames.
- Use localized alt text.
- Avoid repeated generic images unless intentional.
- Optimized derivatives must exist where required.
- Do not move assets without mapping.

## Validation Rules

- Define validation per task.
- React/Vite tasks may require typecheck/build.
- WordPress tasks may require backup/staging/manual QA.
- Mark browser-only checks as browser-only.
- Do not claim production readiness without required checks.

## Stop Conditions

- Dirty worktree outside expected scope.
- Unclear goal.
- Missing required context.
- Forbidden file needs edit.
- Validation fails.
- Production risk appears.
- SEO/route/design drift appears.
- Credentials/access missing.
- Backup missing for risky WordPress work.

