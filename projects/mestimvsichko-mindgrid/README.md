# Mestimvsichko MindGrid PMO v2 Project Instance

This folder is the concrete PMO v2 project instance for the Mestimvsichko.bg + MindGrid Request System project.

It is based on the reusable PMO v2 template in `templates/project-pmo-v2/`, but it is populated with known project-specific context, decisions, workstreams, and next actions.

## What This Instance Is

- Project memory for PM / PM Assistant work.
- Handoff package for future ChatGPT or Codex sessions.
- Control documentation for client demo, plugin direction, translation planning, and commercial preparation.
- A documentation-only project instance.

## What This Instance Is Not

- It is not application code.
- It is not the WordPress plugin repository.
- It is not a place for credentials, secrets, tokens, API keys, passwords, WordPress admin access, or private client access data.
- It is not final commercial pricing.

## Recommended Read Order

1. `00_PM_SYSTEM_PROMPT.md`
2. `01_PROJECT_HANDOFF.md`
3. `02_PROJECT_STATUS.md`
4. `03_WORKSTREAMS.md`
5. `09_NEXT_ACTIONS.md`
6. `10_DECISIONS_LOG.md`

## How A New PM Should Start

1. Read the files in the recommended order.
2. Treat the current demo as stable until PM approves changes.
3. Separate client demo, plugin implementation, WordPress site work, translation work, and commercial preparation.
4. Convert needed work into narrow Codex/QA/content/commercial tasks.
5. Update this folder only when project state changes.

## Relation To The Standard Template

- Source template: `templates/project-pmo-v2/`
- This instance: `projects/mestimvsichko-mindgrid/`
- The template remains reusable and generic.
- This folder contains concrete project facts and decisions.

## Must Not Change Without PM Approval

- The staging demo page `/podrobna-zayavka/`.
- The live/production website.
- Plugin release, merge, or tag state.
- Payment/calendar/Google Maps/AI scope.
- Final commercial package prices.
- Translation implementation strategy.
- Any client-facing promise.
