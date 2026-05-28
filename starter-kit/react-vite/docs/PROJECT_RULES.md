# Project Rules

Status: Draft

## Purpose

Defines the rules Codex, ChatGPT, and human operators must follow during `[Project Name]`.

## Usage Notes

- Codex must stop if a task conflicts with these rules.
- Update when route, SEO, design, asset, validation, or deployment rules change.

## Operating Rules

- GitHub is source of truth.
- Notion is operations layer.
- Codex must follow AGENTS.md.
- Rosen / MindGrid Studio makes final decisions.
- Do not rely only on chat memory.

## File / Scope Rules

- Always check `git status --short` before work.
- Work only in allowed files.
- Stop if forbidden files need changes.
- Do not modify unrelated files.
- Do not create new folders unless explicitly requested.
- Do not commit deployment ZIPs or temporary files.

## Content Rules

- Do not invent claims, metrics, certifications, awards, or partnerships.
- Keep language consistent.
- Avoid placeholder text in release candidates.
- UI labels must match project language unless approved.

## Design Rules

- Follow approved design system.
- Do not invent colors, typography, spacing, or layout patterns.
- Reuse approved components.
- Avoid one-off layout drift.

## Route / SEO Rules

- Do not invent routes.
- Maintain approved route map.
- Do not change SEO config unless requested.
- Keep sitemap/canonical alignment.
- Avoid accidental noindex.
- Do not leave old routes in sitemap unless approved.

## Image / Asset Rules

- Use IMAGE_ASSET_REGISTER.md when images are involved.
- Do not change image paths unless requested.
- Do not use external fallback images without approval.
- Optimized derivatives must exist where required.
- Runtime image paths must match actual files.

## React/Vite Validation Rules

- Run typecheck/build when relevant.
- Common commands: `npx.cmd tsc --noEmit`, `npm.cmd run build`.
- Prerender route count must be checked if prerender is used.
- Hydration and console errors must be treated as blockers.

## Deployment Artifact Rules

- Do not commit deployment ZIP files.
- `dist/` is usually not committed unless the project explicitly stores deploy artifacts.
- Deployment package should be built from `dist/` contents, not nested `dist/`.
- Include `.htaccess` only when required and approved.

## Stop Conditions

- Dirty worktree outside expected scope.
- Route/SEO/design drift appears.
- Forbidden file needs edit.
- Validation fails.
- Build/prerender output is unclear.
- Deployment target is unclear.

