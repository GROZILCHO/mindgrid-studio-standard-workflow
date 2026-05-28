# Pre-Codex Checklist

Status: Draft

## Purpose

This checklist prevents uncontrolled Codex work by ensuring the task has enough context, allowed scope, validation rules, and stop conditions before implementation begins.

## 1. Repository State

- [ ] Correct repository is open.
- [ ] Correct branch is active.
- [ ] git status is clean, unless task explicitly allows dirty worktree.
- [ ] Remote origin is configured.
- [ ] Latest changes are pulled or branch state is understood.
- [ ] No accidental files exist, such as deployment ZIPs, pasted text files, or temporary files.

## 2. Context Files To Inspect

- [ ] AGENTS.md
- [ ] README.md
- [ ] docs/PROJECT_BRIEF.md
- [ ] docs/PROJECT_RULES.md
- [ ] docs/CURRENT_STATUS.md
- [ ] docs/NEXT_ACTIONS.md
- [ ] docs/ISSUES_LOG.md
- [ ] docs/DECISIONS_LOG.md
- [ ] docs/SITE_STRUCTURE.md, when routes/pages are involved.
- [ ] docs/DESIGN_SYSTEM.md, when UI is involved.
- [ ] docs/SEO_PLAN.md, when SEO is involved.
- [ ] docs/IMAGE_ASSET_REGISTER.md, when images are involved.
- [ ] docs/DEPLOYMENT_GUIDE.md, when deployment is involved.

## 3. Task Definition

- [ ] Context is clear.
- [ ] Goal is specific.
- [ ] Current state is described.
- [ ] Allowed files are listed.
- [ ] Forbidden files are listed.
- [ ] Requirements are concrete.
- [ ] Tracking Docs Update rules are set.
- [ ] Validation commands are defined.
- [ ] Output report format is defined.
- [ ] Stop conditions are defined.

## 4. Scope Control

- [ ] Codex must not modify files outside allowed scope.
- [ ] Codex must stop if forbidden files need changes.
- [ ] Codex must not invent routes.
- [ ] Codex must not invent colors.
- [ ] Codex must not invent unsupported claims.
- [ ] Codex must not create new file structures unless explicitly requested.
- [ ] Codex must not commit deployment ZIPs or temporary files.
- [ ] Codex must not mix unrelated fixes into one task.

## 5. Validation Planning

- [ ] Required validation commands are known.
- [ ] For React/Vite: typecheck/build/prerender expectations are defined if relevant.
- [ ] For WordPress: backup/staging/rollback expectations are defined if relevant.
- [ ] Manual QA expectations are listed if needed.
- [ ] Browser checks are listed if needed.
- [ ] Deployment checks are listed if needed.

## 6. Tracking Document Update Decision

| Tracking Document | Update? | Rule |
| --- | --- | --- |
| CURRENT_STATUS.md | yes/no | Update after significant implementation, QA, deployment or planning tasks. |
| NEXT_ACTIONS.md | yes/no | Update when there are concrete next steps. |
| ISSUES_LOG.md | yes/no / only if issues found | Update when bugs, blockers, risks or unresolved questions are found. |
| DECISIONS_LOG.md | yes/no / only if decision made | Update only when a real decision is made. |
| PROJECT_HANDOFF.md | yes/no | Update when switching chats/agents, pausing, or ending a phase. |

## 7. Stop Conditions

Stop before assigning the task to Codex if any of these apply:

- [ ] Dirty worktree outside expected scope.
- [ ] Missing required context files.
- [ ] Unclear goal.
- [ ] Unclear allowed files.
- [ ] Unclear forbidden files.
- [ ] Validation cannot be run.
- [ ] Task requires credentials not available to Codex.
- [ ] Task requires WordPress DB/admin context not available.
- [ ] Task requires modifying production without backup.
- [ ] Task could affect SEO/routes/design without explicit approval.

## 8. Codex Task Readiness Decision

- [ ] Ready for Codex: yes/no.
- [ ] If no, list what must be clarified first.

