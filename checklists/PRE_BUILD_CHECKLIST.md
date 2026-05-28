# Pre-Build Checklist

Status: Draft

## Purpose

This checklist is used before running a production build or major validation step.

## 1. Repository State

- [ ] Correct repository is open.
- [ ] Correct branch is active.
- [ ] `git status --short` has been checked.
- [ ] Dirty worktree is expected and understood, or worktree is clean.
- [ ] No accidental files are present.
- [ ] No deployment ZIP files are staged.
- [ ] No pasted terminal artifacts are present.
- [ ] Remote origin is configured.
- [ ] Latest branch state is understood.

## 2. Context And Documentation

- [ ] AGENTS.md has been reviewed.
- [ ] CURRENT_STATUS.md is up to date or intentionally unchanged.
- [ ] ISSUES_LOG.md has no unresolved blocking issues.
- [ ] NEXT_ACTIONS.md matches the current task direction.
- [ ] DECISIONS_LOG.md contains relevant recent decisions.
- [ ] Project-specific docs are available for the task.

## 3. Scope Check

- [ ] Changed files match the task scope.
- [ ] No forbidden files were modified.
- [ ] No unrelated fixes were mixed into the task.
- [ ] No routes were changed unless explicitly requested.
- [ ] No SEO metadata was changed unless explicitly requested.
- [ ] No image paths were changed unless explicitly requested.
- [ ] No layout/design system drift was introduced.

## 4. React/Vite Build Readiness

- [ ] TypeScript changes are expected.
- [ ] Route changes are intentional and documented.
- [ ] Sitemap route expectations are clear.
- [ ] Static asset expectations are clear.
- [ ] Image optimized derivatives exist where required.
- [ ] `.htaccess` or deployment config changes are intentional.
- [ ] Hydration/prerender risks are considered.

## 5. WordPress Build/Readiness Equivalent

- [ ] Staging target is clear.
- [ ] Backup status is known.
- [ ] Theme/plugin files are scoped.
- [ ] Database-affecting changes are identified.
- [ ] Elementor/ACF/export needs are known.
- [ ] Rollback plan is understood.

## 6. Stop Conditions

Stop if:

- [ ] Working tree contains unexpected changes.
- [ ] Required context files are missing.
- [ ] Build command is unclear.
- [ ] Validation cannot be run.
- [ ] A forbidden file was modified.
- [ ] The task scope changed without approval.
- [ ] There are unresolved blocking issues.

