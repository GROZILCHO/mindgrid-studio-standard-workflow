# QA Checklist

Status: Draft

## Purpose

This document defines project-specific QA checks before build, deployment, and post-launch validation.

## Usage Notes

- Use this with PRE_BUILD_CHECKLIST.md, PRE_DEPLOY_CHECKLIST.md, POST_DEPLOY_CHECKLIST.md, SEO_LAUNCH_CHECKLIST.md, and VISUAL_QA_CHECKLIST.md when available.
- Record blockers in ISSUES_LOG.md.
- Do not declare launch readiness if required checks are missing.

## 1. QA Scope

- Project type:
- Pages/routes in scope:
- Devices/breakpoints in scope:
- Browsers if relevant:
- QA owner:
- QA status:

## 2. Route And Navigation QA

- [ ] All planned routes exist.
- [ ] Direct route refresh works where applicable.
- [ ] Nav links work.
- [ ] Footer links work.
- [ ] CTA links work.
- [ ] 404 works.
- [ ] Redirects work if configured.

## 3. Content QA

- [ ] No placeholder text.
- [ ] No unsupported claims.
- [ ] No mixed-language UI labels.
- [ ] CTA language consistent.
- [ ] Headings meaningful.
- [ ] Legal/contact information correct.
- [ ] Important page copy reviewed.

## 4. Visual QA

- [ ] Design system consistency.
- [ ] Responsive layout.
- [ ] Mobile navigation.
- [ ] Hero sections.
- [ ] Cards.
- [ ] Buttons.
- [ ] Forms.
- [ ] Image crops.
- [ ] Repeated image review.

## 5. SEO QA

- [ ] Titles.
- [ ] Descriptions.
- [ ] Canonicals.
- [ ] Robots.
- [ ] Sitemap.
- [ ] OG images.
- [ ] Schema if used.
- [ ] No accidental noindex.
- [ ] Internal links.

## 6. Performance QA

- [ ] Build output reviewed.
- [ ] Bundle size reviewed if relevant.
- [ ] Image weight reviewed.
- [ ] Compression checked.
- [ ] Lighthouse/PageSpeed checked.
- [ ] Console errors checked.
- [ ] Hydration errors checked for React/Vite.
- [ ] Cache checked if relevant.

## 7. WordPress QA

- [ ] Admin login.
- [ ] Plugin conflicts.
- [ ] Forms.
- [ ] Media library.
- [ ] Elementor/Gutenberg layout.
- [ ] Cache.
- [ ] Permalinks.
- [ ] WooCommerce flow if relevant.
- [ ] Backup/restore readiness.

## 8. Deployment QA

- [ ] Deployment package correct.
- [ ] Files uploaded to correct location.
- [ ] SSL works.
- [ ] Sitemap/robots live.
- [ ] Analytics/cookie consent checked.
- [ ] Production smoke test complete.

## 9. Issue Log

| Issue | Severity | Area | Status | Owner | Next Action |
| --- | --- | --- | --- | --- | --- |
| Placeholder | Low/Medium/High/Critical | Placeholder | Open | Placeholder | Placeholder |

## 10. QA Decision

- Ready for deployment: yes/no
- Blockers:
- Non-blocking issues:
- Next QA action:

