# Project Dashboard Structure

Status: Draft

## Purpose

This document defines the recommended Notion dashboard structure for managing MindGrid Studio projects. The dashboard should show high-level project state, not replace GitHub docs.

## 1. Dashboard Purpose

The dashboard should help Rosen see:

- Active projects.
- Current phase.
- Next actions.
- Blocked tasks.
- Pending reviews.
- Launch readiness.
- Post-launch tasks.
- Project owner/responsible people.

## 2. Recommended Databases

### Projects

Fields:

- Project Name.
- Client / Brand.
- Project Type.
- Status.
- Priority.
- Start Date.
- Target Launch Date.
- GitHub Repo.
- Website URL.
- Current Phase.
- Owner.
- Notes.

### Tasks

Fields:

- Task Name.
- Project.
- Task Status.
- Priority.
- Type.
- Assigned To.
- Start Date.
- Due Date.
- GitHub Reference.
- Source Document.
- Notes.

### Issues / Risks

Fields:

- Issue Name.
- Project.
- Severity.
- Status.
- Affected Area.
- Owner.
- Proposed Action.
- Resolution Notes.
- Related GitHub Document.

### Decisions

Fields:

- Decision Title.
- Project.
- Decision Date.
- Area.
- Impact.
- Related Files.
- Notes.

### Assets / Content Optional

Fields:

- Asset / Content Item.
- Project.
- Type.
- Status.
- Owner.
- Source.
- Usage.
- Notes.

## 3. Recommended Dashboard Views

- Active Projects.
- Tasks by Project.
- Tasks by Status.
- Blocked Tasks.
- Due This Week.
- Ready for Review.
- Launch Readiness.
- Post-launch Follow-up.
- High/Critical Issues.
- Decisions Log.

## 4. Project Phase Display

Recommended project phases:

- Intake.
- Strategy.
- Architecture.
- Content.
- Design System.
- Assets.
- Implementation.
- QA.
- Deployment.
- Post-launch.
- Retrospective.

## 5. How GitHub And Notion Should Connect

- Notion task should link to GitHub repo or relevant file/commit when useful.
- GitHub docs remain the detailed technical source.
- Notion tracks operational state and responsibility.
- CURRENT_STATUS.md should match the high-level Notion project status.
- NEXT_ACTIONS.md should inform upcoming Notion tasks.
- ISSUES_LOG.md should inform issues/risk database.
- DECISIONS_LOG.md should inform decisions database if used.

## 6. Minimal Dashboard For Small Projects

For small projects, use only:

- Projects.
- Tasks.
- Issues/Risks.

Do not overbuild Notion if the project is short and simple.

## 7. Stop Conditions

Do not rely on the dashboard alone if:

- GitHub docs are outdated.
- Implementation status is unclear.
- Task owner is unclear.
- Launch readiness is not validated.
- Issues are not documented.
- There is no link between project task and repository state.

