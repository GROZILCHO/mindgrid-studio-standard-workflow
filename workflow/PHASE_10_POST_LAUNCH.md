# Phase 10: QA And Deployment

Status: Draft

## Purpose

Validate the project before launch, prepare deployment safely, release to production, and run production smoke tests.

## When To Use This Phase

Use this phase after implementation is complete enough for release candidate review and before any production launch.

## Main Questions

- Has pre-build QA been completed?
- Do React/Vite typecheck, build, prerender, sitemap, and robots outputs pass if relevant?
- Do WordPress staging, backup, and rollback requirements exist and pass if relevant?
- Have visual, content, SEO, performance, accessibility, and deployment checks been completed?
- Is the deployment package or migration method correct?
- Has production smoke testing been planned?

## Required Inputs

- QA_CHECKLIST.md.
- DEPLOYMENT_GUIDE.md.
- PRE_BUILD_CHECKLIST.md.
- PRE_DEPLOY_CHECKLIST.md.
- SEO_LAUNCH_CHECKLIST.md.
- VISUAL_QA_CHECKLIST.md.
- CURRENT_STATUS.md.
- ISSUES_LOG.md.

## Expected Outputs

- QA findings.
- Build/typecheck/prerender results where relevant.
- WordPress backup/staging confirmation where relevant.
- Pre-deploy readiness decision.
- Deployment package or migration plan.
- Production smoke test results.
- CURRENT_STATUS.md and ISSUES_LOG.md updated as needed.

## Recommended Steps

1. Run pre-build checklist.
2. Run platform-specific validation.
3. Review route, link, content, visual, SEO, image, and performance QA.
4. Resolve or log blockers.
5. Confirm deployment target and rollback path.
6. Prepare deployment package or migration procedure.
7. Deploy only after approval.
8. Run production smoke test.
9. Record post-deploy results and next actions.

## Codex / Agent Involvement

- QA / Release Specialist may prepare QA findings and readiness decisions.
- Codex may run builds, audits, file checks, and docs updates within scope.
- ChatGPT Lead Assistant coordinates interpretation and next tasks.
- Rosen / MindGrid Studio approves release and deployment decisions.

## Tracking Docs Update Rules

- Update CURRENT_STATUS.md after QA and deployment milestones.
- Update NEXT_ACTIONS.md with unresolved launch or post-launch tasks.
- Update ISSUES_LOG.md for blockers, production problems, or unresolved risks.
- Update DECISIONS_LOG.md only for real deployment, rollback, SEO, or release decisions.
- Update PROJECT_HANDOFF.md if pausing after deployment or switching sessions.

## Completion Criteria

- Required QA checks pass or non-blockers are accepted.
- Build/typecheck pass where relevant.
- Backup/staging requirements are met for WordPress where relevant.
- Deployment is approved.
- Production smoke test is complete.
- Post-launch tasks are documented.

## Stop Conditions

- Build or typecheck fails.
- Major route, SEO, image, visual, or performance issue remains.
- WordPress backup is missing for risky work.
- Deployment target is unclear.
- Rollback path is unclear.
- Project owner has not approved release.
- Production smoke test fails.

## Handoff Notes

New sessions should inspect QA_CHECKLIST.md, DEPLOYMENT_GUIDE.md, CURRENT_STATUS.md, ISSUES_LOG.md, NEXT_ACTIONS.md, and the relevant platform workflow.
