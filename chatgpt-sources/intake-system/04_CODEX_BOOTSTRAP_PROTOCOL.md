# Codex Bootstrap Protocol

Status: Source Pack

## Purpose

Use this compact protocol to prepare the first Codex interaction for a project. Start with a read-only audit. Request implementation only after repository state, context files, and scope are understood.

## Mandatory First Step

Every Codex task should begin with:

```cmd
git status --short
```

Continue only when the worktree state matches the task instructions. Stop and report unexpected modified or untracked files.

## Required Task Inputs

- Repository name.
- Local folder.
- Branch.
- Task type: audit-only or implementation.
- Context files to inspect.
- Allowed files.
- Forbidden files.
- Requirements.
- Tracking docs update decision.
- Validation commands.
- Output report format.
- Stop conditions.

## Context Files To Inspect When Relevant

- `AGENTS.md`
- `README.md`
- `docs/PROJECT_BRIEF.md`
- `docs/PROJECT_RULES.md`
- `docs/SITE_STRUCTURE.md`
- `docs/CURRENT_STATUS.md`
- `docs/NEXT_ACTIONS.md`
- `docs/ISSUES_LOG.md`
- `docs/DECISIONS_LOG.md`
- `docs/DESIGN_SYSTEM.md` for UI work
- `docs/SEO_PLAN.md` for SEO work
- `docs/IMAGE_ASSET_REGISTER.md` for asset work
- `docs/DEPLOYMENT_GUIDE.md` for deployment work

## Audit-Only Versus Implementation

| Task Type | Allowed Behavior |
| --- | --- |
| Audit-only | Inspect, compare, run read-only validation, and report. Do not edit, create, rename, move, stage, commit, or push files. |
| Implementation | Modify only explicitly allowed files, run validation, report changed files and risks, and stop if scope expands. |

## Reusable Codex Prompt Skeleton

```md
# TASK - [Project] [Task Name]

Repository: [repo]
Local folder: [path]
Branch: [branch]

## Context
[Relevant project state and docs.]

## Goal
[One narrow outcome.]

## Mandatory First Step
Run:
git status --short

If dirty unexpectedly, stop and report.

## Current State
[Known state.]

## Allowed Files
- [...]

## Forbidden Files
- [...]

## Requirements
- [...]

## Tracking Docs Update
- CURRENT_STATUS.md: yes/no
- NEXT_ACTIONS.md: yes/no
- ISSUES_LOG.md: yes/no / only if issues found
- DECISIONS_LOG.md: yes/no / only if decision made
- PROJECT_HANDOFF.md: yes/no

## Validation
Run:
- [...]

## Output Required
1. Files inspected or changed
2. Validation results
3. Risks or assumptions
4. git status --short

## Stop Conditions
- Dirty worktree outside expected scope
- Missing context
- Need to edit forbidden files
- Validation failure
- Data-loss, route, SEO, design, or deployment risk
```

## Bootstrap Sequence

1. Audit repository structure and Git state.
2. Confirm docs and do-not-touch areas.
3. Identify missing context or risks.
4. Update planning docs if needed through a separate scoped task.
5. Prepare the first narrow implementation task.
6. Validate the first browser-visible baseline.

