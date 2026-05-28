# Agents

## Purpose

Defines the basic operating rules for people and AI agents using the MindGrid Studio Standard Workflow.

Status: Draft

## Roles

- Rosen / MindGrid Studio: project owner and operator.
- ChatGPT Lead Assistant: strategist, planner, QA guide, and Codex prompt author.
- Codex: implementation developer working through repository files.

## Docs-First Behavior

Before implementation or documentation changes, Codex should inspect the relevant project docs and understand the current state. If the task affects a real project, docs are treated as the source of operating context.

## Mandatory Files To Inspect Before Implementation

For real projects, inspect these files when present:

- `README.md`
- `AGENTS.md`
- `docs/PROJECT_BRIEF.md`
- `docs/PROJECT_RULES.md`
- `docs/CURRENT_STATUS.md`
- `docs/NEXT_ACTIONS.md`
- `docs/ISSUES_LOG.md`
- `docs/DECISIONS_LOG.md`

For this master workflow repository, inspect the relevant workflow, template, prompt, or checklist file before editing it.

## Narrow Task Discipline

- Work on the smallest useful task that satisfies the request.
- Keep edits inside the files allowed by the task.
- Avoid unrelated refactors, rewrites, or structure changes.
- Stop and report if the requested change conflicts with existing project rules.

## Forbidden Behavior

Codex must not invent:

- Routes or page structures.
- Colors, typography, or visual systems.
- Marketing claims, guarantees, prices, or business facts.
- File structures, frameworks, or dependencies outside the task scope.

## Reporting Requirements

Every Codex result should report:

- Files changed.
- Validation performed.
- Risks or assumptions.
- `git status --short`.

## Tracking Docs Update Rules

Codex must not update all tracking files automatically on every small task.

Codex should update tracking docs only when:

- The task explicitly requests it.
- The task changes project state.
- A new issue or risk is found.
- A real decision is made.
- A handoff is requested.

## Tracking Document Responsibilities

- `CURRENT_STATUS.md`: update after significant implementation, QA, deployment, or planning tasks. It should show current phase, current state, completed work, active issues, next task, git status, last validation, do not touch notes, and handoff notes.
- `NEXT_ACTIONS.md`: update when there are concrete next steps. List tasks in priority order with owner, status, priority, dependency, and suggested next prompt or task.
- `ISSUES_LOG.md`: update when bugs, blockers, risks, or unresolved questions are found. Include ID, severity, affected area, description, status, owner, proposed action, and resolution notes.
- `DECISIONS_LOG.md`: update only when a real strategic, architectural, technical, or content decision is made. Do not use it as a daily changelog.
- `PROJECT_HANDOFF.md`: update only when requested, at the end of a major phase, before switching chats or agents, or before pausing a project. It should summarize context for a new ChatGPT/Codex session.

## Placeholder Sections

- Agent handoff examples
- Review escalation rules
- Project-specific reporting formats

