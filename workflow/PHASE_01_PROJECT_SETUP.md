# Phase 01: Project Setup

Status: Draft

## Purpose

Prepare the project repository, local workspace, starter documentation, operating roles, and initial tracking docs before project intake or implementation begins.

## When To Use This Phase

Use this phase at the start of every new MindGrid Studio project, before strategy, design, content, or code work.

## Main Questions

- Does the project repository exist?
- Is the local project folder ready?
- Which starter kit should be copied?
- Is GitHub remote origin configured?
- Will Notion be used for operational tracking?
- Are AGENTS.md and docs/ present?
- Is the initial Git state clean?

## Required Inputs

- Project name.
- Project owner.
- Expected project type.
- Repository location or creation plan.
- Starter-kit choice: general, React/Vite, WordPress, or other.
- Access requirements.

## Expected Outputs

- Project repository created or identified.
- Local folder prepared.
- Starter-kit docs copied.
- AGENTS.md present.
- docs/ folder present.
- Remote origin configured where applicable.
- Initial CURRENT_STATUS.md created.
- Initial NEXT_ACTIONS.md created.
- Notion project entry created if used.

## Recommended Steps

1. Confirm project owner and project name.
2. Create or identify GitHub repository.
3. Prepare local project folder.
4. Select starter kit.
5. Copy starter documentation.
6. Confirm AGENTS.md and docs/ exist.
7. Configure remote origin.
8. Run `git status --short`.
9. Create initial CURRENT_STATUS.md and NEXT_ACTIONS.md entries.
10. Create Notion project entry if relevant.

## Codex / Agent Involvement

- ChatGPT Lead Assistant should guide setup and confirm required docs.
- Codex may inspect files and create documentation only when explicitly scoped.
- Rosen / MindGrid Studio confirms project ownership and final setup decisions.

## Tracking Docs Update Rules

- Update CURRENT_STATUS.md after setup is complete.
- Update NEXT_ACTIONS.md with the first intake task.
- Update ISSUES_LOG.md if repo, access, or folder setup is blocked.
- Update DECISIONS_LOG.md only if a real repository/starter-kit decision is made.
- Update PROJECT_HANDOFF.md only if pausing or switching sessions.

## Completion Criteria

- Repository/folder exists.
- Starter docs exist.
- AGENTS.md exists.
- Git state is understood.
- First intake task is clear.

## Stop Conditions

- No clear project owner.
- No repository or working folder.
- Missing access credentials.
- Starter-kit choice is unclear.
- Git repository cannot be initialized or located.
- Remote origin is unclear when required.

## Handoff Notes

New sessions should inspect README.md, AGENTS.md, docs/CURRENT_STATUS.md, docs/NEXT_ACTIONS.md, and docs/PROJECT_BRIEF.md if already started.

