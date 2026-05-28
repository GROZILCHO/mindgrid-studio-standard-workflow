# QA Checklist

Status: Draft

## Purpose

Defines project-specific QA checks before build, deployment, and post-launch validation.

## Usage Notes

- Record blockers in ISSUES_LOG.md.
- Do not declare launch readiness if required checks are missing.
- Adapt platform-specific checks for React/Vite, WordPress, WooCommerce, static, landing, or redesign projects.

## QA Scope

- Project type: [TBD]
- Pages/routes in scope: [TBD]
- Devices/breakpoints in scope: [TBD]
- Browsers if relevant: [TBD]
- QA owner: [Owner]
- QA status: Draft

## Route / Navigation QA

- [ ] All planned routes exist.
- [ ] Direct route refresh works where applicable.
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
- [ ] Headings meaningful.
- [ ] Legal/contact information correct.
- [ ] Important page copy reviewed.

## Visual QA

- [ ] Design system consistency.
- [ ] Responsive layout.
- [ ] Mobile navigation.
- [ ] Hero sections.
- [ ] Cards.
- [ ] Buttons.
- [ ] Forms.
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

## Performance QA

- [ ] Build output reviewed.
- [ ] Bundle size reviewed if relevant.
- [ ] Image weight reviewed.
- [ ] Compression checked.
- [ ] Lighthouse/PageSpeed checked.
- [ ] Console errors checked.
- [ ] Hydration errors checked for React/Vite.
- [ ] Cache checked if relevant.

## WordPress QA

- [ ] Admin login.
- [ ] Plugin conflicts.
- [ ] Forms.
- [ ] Media library.
- [ ] Elementor/Gutenberg layout.
- [ ] Cache.
- [ ] Permalinks.
- [ ] WooCommerce flow if relevant.
- [ ] Backup/restore readiness.

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

