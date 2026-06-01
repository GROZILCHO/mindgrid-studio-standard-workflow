# MindGrid Project Intake Core

Status: Source Pack

## Purpose

Use this source pack to start a MindGrid Studio web project with enough structure for safe planning and implementation. The intake system identifies the project type, selects a starter kit, establishes minimum documentation, and prepares the first controlled Codex audit.

Do not start with code. Start with repository setup, project context, rules, site structure, and a clear next action.

## Roles

| Role | Responsibility |
| --- | --- |
| Rosen / MindGrid Studio | Project owner, operator, business context provider, QA reviewer, and final decision-maker. |
| Project Intake Assistant | Runs the initial interview, classifies the project, recommends the starter kit, identifies missing inputs, and prepares the first operational plan. |
| Project-specific PM Assistant | Coordinates the project after intake: documentation, Codex prompts, QA interpretation, tracking updates, and handoff control. |
| Codex | Inspects and edits repository files through narrow tasks with allowed files, forbidden files, validation, and reporting requirements. |
| GitHub | Source of truth and durable project memory for docs, implementation files, decisions, and handoff context. |
| Notion | Optional operations layer for task visibility, owners, deadlines, priorities, status, and milestones. |

## Minimum Documents Before Implementation

Create or adapt these files before implementation begins:

- `AGENTS.md`
- `docs/PROJECT_BRIEF.md`
- `docs/PROJECT_RULES.md`
- `docs/SITE_STRUCTURE.md`
- `docs/CURRENT_STATUS.md`
- `docs/NEXT_ACTIONS.md`

Add these as the project develops:

- `docs/CONTENT_MODEL.md`
- `docs/DESIGN_SYSTEM.md`
- `docs/SEO_PLAN.md`
- `docs/IMAGE_ASSET_REGISTER.md`
- `docs/ISSUES_LOG.md`
- `docs/DECISIONS_LOG.md`
- `docs/PROJECT_HANDOFF.md`
- `docs/DEPLOYMENT_GUIDE.md`
- `docs/QA_CHECKLIST.md`

## Operating Rules

- GitHub stores implementation truth. Chat memory and Notion do not replace repository docs.
- Notion may mirror high-level tasks, but detailed implementation rules belong in GitHub.
- Do not invent routes, claims, colors, file structures, access, or platform constraints.
- Use an audit-first workflow: inspect repository state before requesting implementation.
- Codex tasks must be narrow, scoped, validated, and reported.
- Update tracking docs only when explicitly requested or when project state genuinely changes.
- When chat context becomes long, update `CURRENT_STATUS.md`, `NEXT_ACTIONS.md`, `ISSUES_LOG.md` if needed, and `PROJECT_HANDOFF.md`.

## Stop Conditions

Stop and ask for clarification when:

- Project owner, goal, audience, or project type is unclear.
- Repository or local folder is missing.
- Working tree is dirty unexpectedly.
- Starter kit is not selected.
- Minimum planning docs are missing.
- Route/page structure is not approved.
- Codex would need to modify forbidden files.
- Required credentials, access, staging, or backup context is missing.
- A broad implementation task is requested before an audit.
- A first browser-visible baseline cannot be verified where required.

