# QA Checklist

Status: Draft

## Purpose

Defines WordPress project-specific QA checks before deployment, migration, and post-launch validation.

## Usage Notes

- Record blockers in ISSUES_LOG.md.
- Do not declare launch readiness if backup, route, SEO, form, plugin, or deployment checks are missing.

## QA Scope

- Project type: [TBD]
- Pages/routes in scope: [TBD]
- Devices/breakpoints in scope: [TBD]
- Browsers if relevant: [TBD]
- QA owner: [Owner]
- QA status: Draft

## Route / Navigation QA

- [ ] Planned pages exist.
- [ ] Menus work.
- [ ] Footer links work.
- [ ] CTA links work.
- [ ] 404 works.
- [ ] Redirects work if configured.
- [ ] Permalinks work.

## Content QA

- [ ] No placeholder text.
- [ ] No unsupported claims.
- [ ] No mixed-language UI labels.
- [ ] CTA language consistent.
- [ ] Important page copy reviewed.
- [ ] Contact/legal information correct.

## Visual QA

- [ ] Design system consistency.
- [ ] Responsive layout.
- [ ] Mobile navigation.
- [ ] Hero sections.
- [ ] Cards/buttons/forms.
- [ ] Elementor/Gutenberg layouts.
- [ ] Image crops.

## SEO QA

- [ ] SEO plugin output checked.
- [ ] Titles/descriptions.
- [ ] Canonicals.
- [ ] Robots/noindex.
- [ ] Sitemap.
- [ ] OG images.
- [ ] Schema if used.
- [ ] Internal links.

## Performance QA

- [ ] Cache checked.
- [ ] Image weight reviewed.
- [ ] Lighthouse/PageSpeed checked.
- [ ] Console errors checked.
- [ ] Plugin performance risk reviewed.

## WordPress QA

- [ ] Admin login.
- [ ] Plugin conflicts.
- [ ] Forms submit.
- [ ] Media library.
- [ ] Menus.
- [ ] Widgets if used.
- [ ] Elementor/Gutenberg layout rendering.
- [ ] Cache cleared.
- [ ] Permalinks flushed.
- [ ] WooCommerce flow if relevant.
- [ ] Backup/restore readiness.
- [ ] Staging-to-production validation.

## Deployment QA

- [ ] Backup confirmed.
- [ ] Files uploaded to correct location.
- [ ] Database/media migration checked if relevant.
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

