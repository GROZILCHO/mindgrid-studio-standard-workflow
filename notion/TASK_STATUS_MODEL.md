# Task Status Model

Status: Draft

## Purpose

This document defines a practical task status model for MindGrid Studio OS / Notion project tracking.

GitHub remains the implementation source of truth; Notion tracks operational task state, ownership, deadlines, priorities and review status.

## 1. Recommended Statuses

| Status | Meaning | Use when |
| --- | --- | --- |
| Not Started | Task is planned but no work has begun | Task is defined but inactive |
| In Progress | Work is actively being done | Codex/ChatGPT/Rosen is working |
| Review | Work is done but needs human/QA review | Codex returned result, awaiting approval |
| Blocked | Work cannot continue | Missing access, decision, file, backup or context |
| Done | Work is completed and accepted | Validated, committed/pushed if relevant |
| Canceled | Task is no longer needed | Scope changed or task was replaced |

## 2. Optional Statuses

Optional statuses:

- Backlog.
- Waiting for Client.
- Waiting for Access.
- Waiting for Content.
- Waiting for Assets.
- Needs Fix.
- Ready for Deploy.
- Deployed.

Optional statuses should be used only if they help, not if they create clutter.

## 3. Status Transition Rules

Common transitions:

- Not Started -> In Progress
- In Progress -> Review
- Review -> Done
- Review -> Needs Fix / In Progress
- In Progress -> Blocked
- Blocked -> In Progress
- Any active status -> Canceled when scope changes

## 4. Status Rules For Codex Tasks

- Codex task starts as In Progress.
- After Codex report, task usually moves to Review.
- If validation passes and Rosen accepts it, task moves to Done.
- If Codex finds a blocker, task moves to Blocked.
- If Codex makes changes outside allowed scope, task should not be marked Done until reviewed.
- If git status is not clean after expected commit, task should remain Review or Needs Fix.

## 5. Status Rules For Planning Tasks

- Intake/strategy tasks can be Done when the required documents exist.
- If business decisions are missing, task is Blocked.
- If documents are draft but usable, task may move to Review.
- If documents are approved for implementation, task is Done.

## 6. Status Rules For Deployment Tasks

- Pre-deploy task is Done only if required checks pass.
- Deployment task is Done only after production smoke test.
- Post-launch task is Done only after Search Console/sitemap/analytics/cookie/performance checks are handled or intentionally deferred.

## 7. Priority Model

| Priority | Meaning |
| --- | --- |
| Critical | Blocks launch, production, data integrity or core functionality |
| High | Important for project delivery or quality |
| Medium | Needed but not blocking immediate progress |
| Low | Polish, documentation or future improvement |

## 8. Stop Conditions

Do not mark a task Done if:

- Validation failed.
- Owner has not approved.
- Major issue remains unresolved.
- Production was not checked after deploy.
- Files were changed outside scope.
- Current Git state is unclear.
- Missing access/credentials block verification.
