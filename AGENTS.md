# Agents

## Purpose

Defines the basic operating rules for people and AI agents using the MindGrid Studio Standard Workflow.

Status: Draft

## Roles

- Rosen / MindGrid Studio: project owner and operator.
- ChatGPT Lead Assistant: strategist, planner, QA guide, and Codex prompt author.
- Codex: implementation developer working through repository files.

## Basic Operating Rules

- Inspect project docs before implementation.
- Do not invent routes, colors, claims, or file structures.
- Use narrow tasks with clear acceptance criteria.
- Always report files changed, validation, risks, and git status.
- Always update CURRENT_STATUS.md in real projects when asked.

## Tracking Document Rules

Codex must not update all tracking files automatically on every small task.

Codex should update tracking docs only when:

- The task explicitly requests it.
- The task changes project state.
- A new issue or risk is found.
- A decision is made.
- A handoff is requested.

## Tracking Document Responsibilities

- CURRENT_STATUS.md: update after significant implementation, QA, deployment, or planning tasks. It should show current phase, completed work, active issues, next task, git status, last validation, and do not touch notes.
- NEXT_ACTIONS.md: update when there are concrete next steps. List next tasks in priority order with owner, status, priority, and dependency if known.
- ISSUES_LOG.md: update when bugs, blockers, risks, or unresolved questions are found. Include description, severity, affected area, status, owner, and proposed next action.
- DECISIONS_LOG.md: update only when a real strategic, architectural, technical, or content decision is made. Do not use it as a daily changelog.
- PROJECT_HANDOFF.md: update only when requested, at the end of a major phase, before switching chats or agents, or before pausing a project. It should summarize context for a new ChatGPT/Codex session.

## Placeholder Sections

- Agent handoff rules
- Review escalation rules
- Project-specific constraints
- Validation standards
- Reporting format

