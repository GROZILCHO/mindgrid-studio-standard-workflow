# Pre-Deploy Checklist

Status: Draft

## Purpose

This checklist is used before uploading or releasing a site to production.

## 1. General Deployment Readiness

- [ ] Project owner approved release candidate.
- [ ] Git worktree is clean after final commit.
- [ ] Latest changes are pushed.
- [ ] Final validation passed.
- [ ] Deployment target is confirmed.
- [ ] Credentials/access are available.
- [ ] Rollback path is known.
- [ ] Launch window is acceptable.

## 2. React/Vite Static Deployment Readiness

- [ ] `npm run build` or equivalent passed.
- [ ] Typecheck passed if applicable.
- [ ] Expected route count is generated.
- [ ] `sitemap.xml` is generated.
- [ ] `robots.txt` is generated.
- [ ] `404` behavior is correct.
- [ ] `.htaccess` or equivalent deployment config is included.
- [ ] `assets/`, `images/`, `optimized/`, `icons/`, `patterns/` are included when needed.
- [ ] Deployment ZIP is created from `dist` contents.
- [ ] ZIP does not contain nested `dist/` folder.
- [ ] ZIP does not contain unrelated files.

## 3. WordPress Deployment Readiness

- [ ] Full backup exists.
- [ ] Staging was tested if needed.
- [ ] Theme/plugin changes are ready.
- [ ] Database migration plan is clear.
- [ ] Media migration plan is clear.
- [ ] Elementor/ACF/form exports exist if relevant.
- [ ] Plugin versions are documented.
- [ ] Cache/security/SEO plugins are considered.
- [ ] WooCommerce data risk is reviewed if relevant.

## 4. SEO Readiness

- [ ] Canonicals are correct.
- [ ] Sitemap contains only intended public routes/pages.
- [ ] Robots rules are intentional.
- [ ] Noindex rules are intentional.
- [ ] Redirects are defined if needed.
- [ ] Open Graph images are valid.
- [ ] Main pages have titles/descriptions.
- [ ] Schema is valid if used.

## 5. Visual/Content Readiness

- [ ] Key pages visually reviewed.
- [ ] Mobile layout reviewed.
- [ ] Navigation reviewed.
- [ ] Footer reviewed.
- [ ] Forms reviewed.
- [ ] CTA links reviewed.
- [ ] Images are not broken.
- [ ] Alt text is acceptable.
- [ ] No unsupported claims remain.
- [ ] Localized UI labels are consistent.

## 6. Stop Conditions

Stop deployment if:

- [ ] Build fails.
- [ ] Typecheck fails.
- [ ] Sitemap/robots are wrong.
- [ ] Key images are broken.
- [ ] Navigation is broken.
- [ ] Production credentials are unclear.
- [ ] Backup is missing for WordPress.
- [ ] Major console errors exist.
- [ ] Project owner has not approved release.

