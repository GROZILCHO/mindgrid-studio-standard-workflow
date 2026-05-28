# Codex Task Template

## Purpose

Reusable prompt structure for assigning narrow implementation, documentation, audit, or cleanup tasks to Codex.

Status: Draft

## Context

Describe the project, repository, branch, relevant docs, current workflow phase, and any prior decisions Codex must respect.

## Goal

State the exact outcome expected from this task.

## Current State

Summarize what already exists, what is incomplete, and what should be preserved.

## Allowed Files

List the exact files or folders Codex may modify.

## Forbidden Files

List files, folders, systems, or content areas Codex must not modify.

## Requirements

- Requirement 1 placeholder.
- Requirement 2 placeholder.
- Requirement 3 placeholder.

## Tracking Docs Update

- Should `CURRENT_STATUS.md` be updated? yes/no
- Should `NEXT_ACTIONS.md` be updated? yes/no
- Should `ISSUES_LOG.md` be updated? yes/no
- Should `DECISIONS_LOG.md` be updated? yes/no
- Should `PROJECT_HANDOFF.md` be updated? yes/no

If yes, specify the exact tracking file updates expected.

## Validation

List the commands, checks, previews, or manual review steps Codex should run. If no build is required, say so explicitly.

## Output Required

Codex must report:

- Files changed.
- Summary of work completed.
- Validation performed.
- Risks or assumptions.
- `git status --short`.

## Stop Conditions

Codex should stop and report instead of continuing when:

- Required context is missing and cannot be inferred safely.
- The task requires files outside the allowed scope.
- The requested change conflicts with `AGENTS.md` or project rules.
- Validation fails for reasons unrelated to the requested change.
- A destructive operation would be required.

