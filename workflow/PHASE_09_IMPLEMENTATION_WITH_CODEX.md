# Phase 09: Implementation With Codex

Status: Draft

## Purpose

Execute approved implementation and documentation tasks through narrow, scoped Codex work that follows project docs, allowed files, validation rules, and reporting requirements.

## When To Use This Phase

Use this phase only after the required project documents are clear enough to prevent Codex from inventing routes, claims, styles, file structures, or technical decisions.

## Main Questions

- Is the task narrow enough for Codex?
- Are allowed and forbidden files listed?
- Are validation commands defined?
- Are tracking doc update rules explicit?
- Does the task follow PROJECT_BRIEF.md, PROJECT_RULES.md, SITE_STRUCTURE.md, CONTENT_MODEL.md, and DESIGN_SYSTEM.md?
- What should Codex do if scope changes?

## Required Inputs

- AGENTS.md.
- PROJECT_BRIEF.md.
- PROJECT_RULES.md.
- SITE_STRUCTURE.md when routes/pages are involved.
- CONTENT_MODEL.md when content is involved.
- DESIGN_SYSTEM.md when UI is involved.
- SEO_PLAN.md when SEO is involved.
- IMAGE_ASSET_REGISTER.md when images are involved.
- CURRENT_STATUS.md, NEXT_ACTIONS.md, ISSUES_LOG.md, and DECISIONS_LOG.md.

## Expected Outputs

- Completed scoped implementation/documentation task.
- Validation results.
- Files changed report.
- Risks and assumptions.
- Git status report.
- Tracking docs updated only when requested or justified by project state changes.

## Recommended Steps

1. Inspect required context docs.
2. Run `git status --short`.
3. Confirm allowed and forbidden files.
4. Implement only the requested change.
5. Avoid unrelated fixes.
6. Run required validation.
7. Review changed files.
8. Update tracking docs only when requested or justified.
9. Report files changed, validation, risks, assumptions, and git status.

## Codex / Agent Involvement

- Codex performs scoped file edits and validation.
- ChatGPT Lead Assistant prepares tasks and interprets reports.
- Rosen / MindGrid Studio approves decisions and reviews final results.
- Specialist agents may provide strategy, content, SEO, visual, or QA input before implementation.

## Tracking Docs Update Rules

- Do not update all tracking docs automatically.
- Update CURRENT_STATUS.md after significant implementation, QA, deployment, or planning tasks.
- Update NEXT_ACTIONS.md when concrete next steps exist.
- Update ISSUES_LOG.md when bugs, blockers, risks, or unresolved questions are found.
- Update DECISIONS_LOG.md only when a real decision is made.
- Update PROJECT_HANDOFF.md when requested, pausing, switching sessions, or ending a phase.

## Completion Criteria

- Task requirements are met.
- Only allowed files were changed.
- Validation was run or clearly marked not required.
- Risks and assumptions are reported.
- Git status is reported.

## Stop Conditions

- Working tree is dirty unexpectedly.
- Required files are missing.
- Allowed/forbidden file scope is unclear.
- Task requires modifying forbidden files.
- Validation fails.
- Possible data loss appears.
- Route, SEO, design, content, or deployment drift appears.

## Handoff Notes

New sessions should inspect AGENTS.md, CURRENT_STATUS.md, NEXT_ACTIONS.md, ISSUES_LOG.md, DECISIONS_LOG.md, and the last Codex report.
