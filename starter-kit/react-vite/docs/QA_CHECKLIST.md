# QA Checklist

Status: Draft

## Purpose

Defines React/Vite project-specific QA checks before build, deployment, and post-launch validation.

## Usage Notes

- Record blockers in ISSUES_LOG.md.
- Do not declare launch readiness if build, route, SEO, image, or deployment checks are missing.

## QA Scope

- Project type: [TBD]
- Pages/routes in scope: [TBD]
- Devices/breakpoints in scope: [TBD]
- Browsers if relevant: [TBD]
- QA owner: [Owner]
- QA status: Draft

## Route / Navigation QA

- [ ] All planned routes exist.
- [ ] Direct route refresh works.
- [ ] Nav links work.
- [ ] Footer links work.
- [ ] CTA links work.
- [ ] 404 works.
- [ ] Redirects work if configured.

## Content QA

- [ ] No placeholder text.
- [ ] No unsupported claims.
- [ ] No mixed-language UI labels.
- [ ] CTA language consistent.
- [ ] Important page copy reviewed.

## Visual QA

- [ ] Design system consistency.
- [ ] Responsive layout.
- [ ] Mobile navigation.
- [ ] Hero sections.
- [ ] Cards/buttons/forms.
- [ ] Image crops.
- [ ] Repeated image review.

## SEO QA

- [ ] Titles.
- [ ] Descriptions.
- [ ] Canonicals.
- [ ] Robots.
- [ ] Sitemap.
- [ ] OG images.
- [ ] Schema if used.
- [ ] No accidental noindex.
- [ ] Internal links.

## React/Vite QA

- [ ] Typecheck passes.
- [ ] Build passes.
- [ ] Prerender route count matches expected routes, if used.
- [ ] sitemap.xml generated.
- [ ] robots.txt generated.
- [ ] No hydration errors.
- [ ] No critical console errors.
- [ ] Optimized image paths resolve.
- [ ] Direct route refresh works on deployment target.
- [ ] Compression/MIME checks pass if deployed on Apache/static hosting.

## Performance QA

- [ ] Build output reviewed.
- [ ] Bundle size reviewed if relevant.
- [ ] Image weight reviewed.
- [ ] Lighthouse/PageSpeed checked.
- [ ] Cache behavior checked if relevant.

## Deployment QA

- [ ] Deployment package correct.
- [ ] Files uploaded to correct location.
- [ ] SSL works.
- [ ] Sitemap/robots live.
- [ ] Analytics/cookie consent checked.
- [ ] Production smoke test complete.

## Issue Log

| Issue | Severity | Area | Status | Owner | Next Action |
| --- | --- | --- | --- | --- | --- |
| [TBD] | Low/Medium/High/Critical | [TBD] | Open | [Owner] | [TBD] |

## QA Decision

- Ready for deployment: yes/no
- Blockers: [TBD]
- Non-blocking issues: [TBD]
- Next QA action: [TBD]

