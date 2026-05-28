# Notion Task Mapping

Status: Draft

## Purpose

This document defines how work from GitHub, Codex, and ChatGPT should be represented as tasks in Notion.

GitHub stores project documentation, implementation files, decisions, and durable context. Notion stores operational task visibility: task name, status, priority, owner, dates, project relation, and progress notes.

Codex reports should be summarized into Notion when tasks are completed. Notion should not be used as the only place where technical implementation rules live.

## 1. When To Create A Notion Task

Create a Notion task when:

- A project phase begins.
- An implementation task is assigned.
- An audit task is assigned.
- A QA task is assigned.
- A deployment task is assigned.
- A post-launch task is assigned.
- An issue requires follow-up.
- A decision requires operational follow-through.
- Client/operator review is needed.

Tiny edits do not always need separate Notion tasks unless they are part of a tracked sprint.

## 2. Recommended Task Naming Format

Use task names that preserve project and sequence:

- `[Project Name] 01. Project Intake and Brief`
- `[Project Name] 02. Site Structure and Route Planning`
- `[Project Name] 03. Design System Setup`
- `[Project Name] 04. Content Model Development`
- `[Project Name] 05. Visual Asset Planning`
- `[Project Name] 06. Implementation Sprint 1`
- `[Project Name] 07. QA and Deployment`
- `[Project Name] 08. Post-launch SEO Setup`

Numbering helps preserve sequence across project phases, Notion views, and handoffs.

## 3. Task Fields

Recommended Notion fields:

| Field | Purpose | Example |
| --- | --- | --- |
| Name | Task title | `[Project] 03. Design System Setup` |
| Task Status | Current state | Not started / In Progress / Review / Done / Blocked |
| Priority | Importance | Low / Medium / High / Critical |
| Type | Work category | Strategy / Content / Design / Development / QA / Deployment / SEO / Ops |
| Project | Related project | Mall Electro / Future Client Site |
| Assigned To | Responsible person | Rosen / Codex / ChatGPT Lead / External |
| Start Date | Planned start | YYYY-MM-DD |
| Due Date | Planned completion | YYYY-MM-DD |
| Notes | Operational summary | Short human-readable task context |
| GitHub Reference | Optional repo/commit/PR/file link | repo URL or commit hash |
| Source Document | Related doc | CURRENT_STATUS.md / NEXT_ACTIONS.md / ISSUES_LOG.md |

If a Notion database has different field names, adapt the mapping without changing the workflow logic.

## 4. Mapping From GitHub Docs To Notion

| GitHub document | Notion use |
| --- | --- |
| CURRENT_STATUS.md | Current project status summary |
| NEXT_ACTIONS.md | Source for upcoming tasks |
| ISSUES_LOG.md | Source for bug/risk/blocker tasks |
| DECISIONS_LOG.md | Source for follow-up tasks when decisions require action |
| PROJECT_HANDOFF.md | Used when pausing or restarting a project |
| QA_CHECKLIST.md | Source for QA task groups |
| DEPLOYMENT_GUIDE.md | Source for deployment tasks |

## 5. Mapping From Codex Report To Notion

Codex reports should be summarized into Notion with:

- Files changed.
- Task result.
- Validation result.
- Risks/assumptions.
- Next recommended action.
- Commit hash if available.
- Whether task is Done, Review, Blocked, or Needs Follow-up.

Do not paste huge Codex reports into Notion if a concise operational summary and GitHub reference are enough.

## 6. Task Granularity Rules

- Use broader tasks for strategy and planning phases.
- Use specific tasks for implementation and QA.
- Do not create one Notion task for every tiny line edit.
- Create separate tasks for different responsibility zones:
  - Content.
  - Visual assets.
  - Implementation.
  - SEO.
  - Performance.
  - Deployment.
  - Post-launch.
- If a task produces follow-up work, add it to NEXT_ACTIONS.md first or create Notion tasks directly if operationally needed.

## 7. Completion Rule

A task can be marked Done only when:

- Requested work is complete.
- Validation is complete or intentionally not required.
- Risks are documented.
- Git status is clean where relevant.
- Changes are committed/pushed where relevant.
- NEXT_ACTIONS.md or ISSUES_LOG.md is updated if needed.

## 8. Stop Conditions

Stop Notion task sync if:

- Project relation is unclear.
- Owner is unclear.
- Task status model is unclear.
- Task duplicates an existing task.
- Codex report is incomplete.
- Work is not actually done.
- Issue requires decision before task creation.

