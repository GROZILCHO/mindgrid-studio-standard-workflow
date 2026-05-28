# Codex Audit Template

Status: Draft

## 1. Purpose

This template is used for audit-only Codex tasks.

Audit tasks should inspect, verify, compare, and report. They must not modify files unless a later implementation task explicitly allows changes.

Use cases:

- Route audits.
- SEO audits.
- Image asset audits.
- Visual consistency audits.
- Performance audits.
- Build/deployment audits.
- WordPress readiness audits.
- Repository structure audits.
- Tracking document audits.
- Broken link/internal link audits.
- Pre-launch checks.

## 2. Core Rule

Audit tasks are read-only by default.

Codex must not:

- Edit files.
- Rename files.
- Move files.
- Delete files.
- Create files.
- Stage files.
- Commit files.
- Push changes.
- Run destructive commands.

This changes only if the task explicitly changes from audit to implementation and the user approves it.

## 3. Standard Audit Task Structure

Use this structure for audit tasks:

- Context.
- Audit Goal.
- Current State.
- Files / Folders to Inspect.
- Files / Folders Not to Touch.
- Audit Questions.
- Validation Commands.
- Output Required.
- Stop Conditions.

## 4. Mandatory First Step

Every audit task should begin with:

```cmd
git status --short
```

Rules:

- If working tree is clean, continue.
- If working tree is dirty but the audit explicitly allows dirty state, continue and report the dirty files.
- If working tree is dirty unexpectedly, stop and report before inspecting further.
- Never modify a dirty worktree during audit.

## 5. Context Files To Inspect

Common project context files to inspect when relevant:

- AGENTS.md
- README.md
- docs/PROJECT_BRIEF.md
- docs/PROJECT_RULES.md
- docs/SITE_STRUCTURE.md
- docs/CONTENT_MODEL.md
- docs/DESIGN_SYSTEM.md
- docs/SEO_PLAN.md
- docs/IMAGE_ASSET_REGISTER.md
- docs/QA_CHECKLIST.md
- docs/CURRENT_STATUS.md
- docs/NEXT_ACTIONS.md
- docs/ISSUES_LOG.md
- docs/DECISIONS_LOG.md
- docs/DEPLOYMENT_GUIDE.md
- docs/PROJECT_HANDOFF.md

Codex should inspect only files relevant to the audit. Do not read unrelated files just to expand scope.

## 6. Audit Types

### Route Audit

Checks:

- Route exists.
- Page component exists.
- Internal links resolve.
- Sitemap includes public route.
- Canonical matches route.
- No old route leakage.

### SEO Audit

Checks:

- Title.
- Description.
- Canonical.
- Robots directives.
- Sitemap.
- `ogImage`.
- Schema if used.
- Noindex mistakes.
- Duplicate metadata.

### Image Asset Audit

Checks:

- Source file exists.
- Optimized derivatives exist where required.
- Folder/naming rules are followed.
- Alt text exists where relevant.
- Repeated images are intentional.
- Runtime paths match actual files.

### Visual Consistency Audit

Checks:

- Design system consistency.
- Repeated layouts/images.
- Language labels.
- CTA consistency.
- Responsive risks.
- Visual drift.

### Performance Audit

Checks:

- Bundle size.
- Build warnings.
- Hydration risks.
- Compression.
- Image weight.
- Lighthouse findings if report is provided.
- Console errors if browser data is provided.

### Deployment Audit

Checks:

- Build output.
- `dist` structure.
- `.htaccess`.
- Sitemap.
- Robots.
- Asset folders.
- Direct route refresh.
- Deployment package correctness.

### WordPress Audit

Checks:

- What is tracked in GitHub.
- What lives in DB/admin.
- Backup/staging status.
- Plugin/theme risks.
- Elementor/ACF/export status.
- Production safety.

## 7. Output Report Format

Use this report format:

1. Executive summary.
2. Audit scope.
3. Files/folders inspected.
4. Findings table.
5. Passed checks.
6. Issues found.
7. Risks / assumptions.
8. Recommended next actions.
9. Implementation task recommendation, if needed.
10. `git status --short`.

Findings table:

| Area | Check | Result | Evidence | Priority | Recommended action |
| --- | --- | --- | --- | --- | --- |
| Placeholder | Placeholder | Pass/Fail/Unverified | Placeholder | Info | Placeholder |

## 8. Priority Model

- Critical: blocks launch or breaks core functionality.
- High: should be fixed before release.
- Medium: should be fixed soon but does not block all progress.
- Low: polish, documentation, or future improvement.
- Info: useful observation, not an issue.

## 9. Evidence Rules

Codex should provide evidence from:

- File paths.
- Line references where practical.
- Command output.
- Build output.
- File existence checks.
- Sitemap/HTML inspection.
- Repository structure.

Codex should not make unsupported claims.

If something cannot be verified from files or command output, state that it is unverified.

## 10. Stop Conditions

Stop and report if:

- Working tree is dirty unexpectedly.
- Required files are missing.
- Repository is not initialized.
- Command cannot run.
- Audit requires credentials not available.
- Audit requires browser-only verification unavailable to Codex.
- Audit requires WordPress admin/database access not available.
- Task asks for file changes but is labelled audit-only.
- Inspection reveals risk of data loss.
- Instructions conflict.

## 11. Tracking Docs

Audit tasks may recommend tracking document updates but should not update them unless explicitly requested.

Use this rule:

- CURRENT_STATUS.md: recommend update if audit changes project state.
- NEXT_ACTIONS.md: recommend update if audit produces concrete follow-up tasks.
- ISSUES_LOG.md: recommend update if bugs, blockers, or risks are found.
- DECISIONS_LOG.md: recommend update only if the audit forces a real decision.
- PROJECT_HANDOFF.md: recommend update only if switching agents/chats or ending a phase.

## 12. Example Audit Prompt Skeleton

```md
# TASK — [Project] [Audit Name]

## Goal

Audit [area] without modifying files.

## Mandatory first step

Run:

git status --short

If dirty unexpectedly, stop and report.

## Audit scope

Inspect:

- ...

Do not modify:

- ...

## Audit questions

1. ...
2. ...
3. ...

## Validation commands

Run:

- ...

## Output required

1. Executive summary
2. Files/folders inspected
3. Findings table
4. Issues found
5. Recommended next actions
6. git status --short
```

## 13. Final Operating Principle

Audit first. Change later.
Do not repair during inspection.
Do not hide uncertainty.
Do not turn an audit into implementation without approval.

