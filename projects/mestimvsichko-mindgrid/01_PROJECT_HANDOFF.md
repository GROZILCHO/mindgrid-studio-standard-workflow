# Project Handoff — Mestimvsichko.bg + MindGrid Request System

## Project Identity

- Project name: Mestimvsichko.bg + MindGrid Request System
- Internal type: client website + custom smart request plugin
- Short description: Bulgarian WordPress site with custom MindGrid request flow for detailed moving/service inquiries, indicative estimate preview, human review, and future commercial expansion.

## Project Lead

- Lead: Росен Станев
- PM / PMO owner: Росен Станев / PM Assistant
- Technical execution: Codex, under PM-approved tasks
- Commercial owner: Росен Станев

## Client

- Client name: Никола
- Client reference: "Колеца"
- Client status: positive initial reaction to current demo
- Approval status: encouraging validation, not final approval

## Current Phase

- Phase: client demo / requirements validation
- Current demo status: GO for client discussion
- Production/live status: HOLD
- Stable demo page: `https://staging.mestimvsichko.bg/podrobna-zayavka/`

## Current Repositories

- Control / PM repository: `GROZILCHO/mindgrid-studio-standard-workflow`
- Implementation repository: `GROZILCHO/mindgrid-request-system`
- Implementation repo local path: `C:\Users\A.Atanasov\Desktop\MindGrid Studio\mindgrid-request-system`

## Current Plugin Context

- Plugin slug: `mindgrid-request-system`
- Shortcode: `[mindgrid_request_flow]`
- CPT: `mgrs_request`
- Admin menu: `MindGrid Requests`
- Current stable RC: `v0.6.0-rc.1`
- Known implementation branch: `develop`

## Completed Plugin Milestones

- `v0.1.0`: plugin skeleton, CPT, admin menu, status registry, admin columns.
- `v0.2.0`: request entity/admin detail foundation, meta registry, computed MRS request number, contact fields, internal notes, created source, list filter.
- `v0.3.0`: frontend shortcode prototype, five-step PHP-rendered flow, vanilla JS navigation/review screen.
- `v0.4.0`: real submission engine through `admin-post.php`, nonce, honeypot, validation, `mgrs_request` creation, success screen.
- `v0.5.0-rc.1`: Bulgarian Mestimvsichko UX draft and client-specific demo field set.
- `v0.6.0-rc.1`: demo estimate preview, live estimate panel, server-side recalculation, estimate saved in summary only.

## Client Feedback

- Demo looks good.
- Demo looks easy.
- Demo looks suitable.
- Some details must be adapted to the real process.
- Client asked/was curious whether there is a calendar at the end.
- Overall reaction was encouraging.

This is commercial/product validation, not final approval.

## Current PM Decisions

- Current client demo remains stable.
- `/podrobna-zayavka/` must not change before client meeting unless PM approves.
- Smart Request Flow is not a Fantastic Services clone.
- Fantastic Services is only an expectation signal.
- Product logic: detailed request -> indicative price -> human review -> confirmation -> optional payment.
- No live payment without separate scope.
- No real calendar/booking engine without separate scope.
- No Google Maps production integration without separate scope.
- No full WordPress site GitHub migration at this stage.
- Use this control repository for PM context.

## Handoff Notes For New PM

- Read `00_PM_SYSTEM_PROMPT.md` first.
- Treat the current demo as stable.
- Do not request plugin changes unless there is a PM-approved task.
- Keep commercial preparation separate from previous website balance discussions.
- Clarify calendar/payment/pricing expectations in the next client conversation.
