# Post-Deploy Checklist

Status: Draft

## Purpose

This checklist is used immediately after production deployment to verify the live site.

## 1. Live Route Smoke Test

- [ ] Homepage opens.
- [ ] Main service/product/category pages open.
- [ ] About/contact pages open.
- [ ] Legal pages open if present.
- [ ] Direct route refresh works.
- [ ] 404 behavior works.
- [ ] Old redirects work if configured.

## 2. Asset And Server Checks

- [ ] CSS loads.
- [ ] JS loads.
- [ ] Images load.
- [ ] AVIF/WebP assets load if used.
- [ ] Fonts load or fallback correctly.
- [ ] Sitemap loads.
- [ ] Robots.txt loads.
- [ ] `.htaccess` behavior works if Apache.
- [ ] Compression works where applicable.
- [ ] Static caching is acceptable.
- [ ] HTML no-cache behavior is acceptable.

## 3. Browser Console Checks

- [ ] No critical console errors.
- [ ] No hydration errors.
- [ ] No missing asset 404s.
- [ ] No mixed-content warnings.
- [ ] No major preload warnings.
- [ ] No blocked critical resources.

## 4. UX Smoke Test

- [ ] Desktop navigation works.
- [ ] Mobile navigation works.
- [ ] CTA links work.
- [ ] Contact forms work.
- [ ] Phone/email links work.
- [ ] Scroll behavior works.
- [ ] Key pages are readable on mobile.

## 5. SEO Live Checks

- [ ] Canonical is correct.
- [ ] Title and meta description are present.
- [ ] Open Graph tags are present.
- [ ] Sitemap URLs are correct.
- [ ] Robots directives are correct.
- [ ] No unintended noindex on public pages.
- [ ] Search Console submission is planned.

## 6. WordPress-specific Checks

- [ ] Admin login works.
- [ ] Permalinks work.
- [ ] Cache cleared.
- [ ] Forms submit.
- [ ] Plugin conflicts not visible.
- [ ] Media library assets appear.
- [ ] Elementor/Gutenberg layouts render correctly if used.
- [ ] WooCommerce flows checked if relevant.

## 7. Stop Conditions

Escalate immediately if:

- [ ] Homepage is broken.
- [ ] CSS/JS fails.
- [ ] Main navigation fails.
- [ ] Contact form fails.
- [ ] Public pages are noindexed accidentally.
- [ ] Mixed-content or SSL issue appears.
- [ ] Severe performance regression appears.
- [ ] WordPress admin is inaccessible after deploy.

