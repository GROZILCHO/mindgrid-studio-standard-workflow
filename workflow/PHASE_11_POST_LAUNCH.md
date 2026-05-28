# Phase 11: Post-launch

Status: Draft

## Purpose

Verify production behavior after launch, complete search/tracking setup, monitor technical quality, and record follow-up work.

## When To Use This Phase

Use this phase immediately after deployment and during the first post-launch review period.

## Main Questions

- Is Google Search Console configured?
- Has the sitemap been submitted?
- Are Analytics / Tag Manager and cookie consent working?
- Do forms submit correctly?
- Are 404s and redirects behaving correctly?
- Are console, Lighthouse/PageSpeed, and Core Web Vitals acceptable?
- What follow-up tasks or issues exist?

## Required Inputs

- DEPLOYMENT_GUIDE.md.
- POST_DEPLOY_CHECKLIST.md.
- SEO_LAUNCH_CHECKLIST.md.
- CURRENT_STATUS.md.
- ISSUES_LOG.md.
- NEXT_ACTIONS.md.

## Expected Outputs

- Search Console setup or plan.
- Sitemap submission status.
- Analytics/cookie consent status.
- Form test results.
- 404/redirect checks.
- Lighthouse/PageSpeed notes.
- NEXT_ACTIONS.md updated.
- ISSUES_LOG.md updated if needed.

## Recommended Steps

1. Run live route smoke test.
2. Submit sitemap or confirm submission plan.
3. Verify Analytics / Tag Manager.
4. Verify cookie consent.
5. Test forms and key CTAs.
6. Check 404 and redirects.
7. Check browser console.
8. Run Lighthouse/PageSpeed where relevant.
9. Record Core Web Vitals monitoring plan.
10. Update tracking docs.

## Codex / Agent Involvement

- QA / Release Specialist may review post-launch checks.
- SEO/AEO Specialist may guide Search Console and indexing checks.
- Codex may run file-based audits or update docs only when scoped.

## Tracking Docs Update Rules

- Update CURRENT_STATUS.md after post-launch checks.
- Update NEXT_ACTIONS.md with concrete follow-up tasks.
- Update ISSUES_LOG.md for production issues.
- Update DECISIONS_LOG.md only if a real post-launch decision is made.
- Update PROJECT_HANDOFF.md if pausing after launch.

## Completion Criteria

- Live site smoke tests are complete.
- Search/tracking plan is documented.
- Production issues are logged.
- Follow-up tasks are clear.

## Stop Conditions

- Homepage or key pages are broken.
- Forms fail.
- Public pages are accidentally noindexed.
- Sitemap/robots are broken.
- Severe performance regression appears.
- Analytics/cookie consent requirement is unresolved.

## Handoff Notes

New sessions should inspect CURRENT_STATUS.md, NEXT_ACTIONS.md, ISSUES_LOG.md, SEO_PLAN.md, and DEPLOYMENT_GUIDE.md.

