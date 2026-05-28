# Phase 08: Repository Setup

Status: Draft

## Purpose

Prepare the project repository for platform-specific work, copy the correct starter documentation, confirm AGENTS.md rules, and establish branch, commit, and file-scope discipline.

## When To Use This Phase

Use this phase after project strategy, structure, content, design, and asset rules are clear enough to support implementation.

## Main Questions

- Is the project repository ready for implementation?
- Which platform-specific structure is needed?
- Are React/Vite or WordPress setup notes documented?
- Are starter-kit docs copied and adapted?
- Is AGENTS.md present and project-specific?
- Is GitHub the source of truth?
- Is branch and commit discipline clear?
- Are accidental files excluded?

## Required Inputs

- PROJECT_BRIEF.md.
- PROJECT_RULES.md.
- SITE_STRUCTURE.md.
- CONTENT_MODEL.md.
- DESIGN_SYSTEM.md.
- IMAGE_ASSET_REGISTER.md where relevant.
- Platform workflow: React/Vite, WordPress, or other.

## Expected Outputs

- Project repository structure prepared.
- Starter docs copied from the selected starter kit.
- AGENTS.md present.
- Platform-specific folders or documentation identified.
- Remote origin and branch state understood.
- Initial implementation scope ready.
- CURRENT_STATUS.md and NEXT_ACTIONS.md updated.

## Recommended Steps

1. Confirm project platform and starter kit.
2. Confirm docs are copied and adapted.
3. Confirm AGENTS.md matches project needs.
4. Confirm GitHub remote and active branch.
5. Confirm no accidental files are present.
6. Define allowed project structure.
7. Record platform-specific setup notes.
8. Run `git status --short`.
9. Prepare first narrow Codex implementation task.

## Codex / Agent Involvement

- ChatGPT Lead Assistant prepares repository setup instructions.
- Codex may inspect repository structure, create documentation, or prepare scoped project files only when allowed.
- Rosen / MindGrid Studio approves platform and repository decisions.

## Tracking Docs Update Rules

- Update CURRENT_STATUS.md after repository setup is usable.
- Update NEXT_ACTIONS.md with the first implementation task.
- Update ISSUES_LOG.md for Git, access, folder, branch, or accidental-file problems.
- Update DECISIONS_LOG.md for real platform/repository structure decisions.
- Update PROJECT_HANDOFF.md if implementation will begin in a new session.

## Completion Criteria

- Repository structure is ready for scoped implementation.
- Project docs exist.
- AGENTS.md is present.
- Git state is understood.
- First Codex task can be written with allowed and forbidden files.

## Stop Conditions

- Repository is missing or not initialized.
- Git state is dirty unexpectedly.
- Platform structure is unclear.
- Required starter docs are missing.
- AGENTS.md is missing.
- Accidental files or deployment artifacts are present.

## Handoff Notes

New sessions should inspect AGENTS.md, README.md, CURRENT_STATUS.md, NEXT_ACTIONS.md, PROJECT_RULES.md, and the relevant platform workflow.
