# Platform Notes

Status: Source Pack

## Purpose

Use these startup notes to identify platform risks before implementation. Confirm the actual project state rather than assuming a platform behaves like another one.

## Platform Summary

| Platform | What GitHub Can Control | What May Live Outside GitHub | Key Startup Warning |
| --- | --- | --- | --- |
| React/Vite | Source code, routes, components, SEO config, scripts, static assets, optimized assets, deployment config, docs. | Hosting settings, credentials, analytics dashboards, external services. | Define routes, SEO behavior, build/prerender expectations, and deployment target before implementation. |
| Next.js | Source code, routes, components, config, docs, many deployment rules. | Hosting platform settings, environment variables, external services, runtime data sources. | Adapt React documentation structure, but confirm Next.js routing, rendering mode, data fetching, image handling, and deployment model. |
| WordPress | Theme, child theme, custom plugins, MU-plugins, file-based CSS/JS, ACF JSON, exports, docs. | Database, media library, admin settings, menus, users, builder layouts, plugin state, form submissions. | Do not treat WordPress as only files. Confirm backup, staging, access, exports, and rollback. |
| WooCommerce | Versioned theme/plugin code and docs. | Products, orders, customers, payments, database state, plugin settings, media. | Treat data integrity as critical. Confirm backups, staging, migration scope, and production risk before changes. |
| Static Website | HTML/CSS/JS, assets, docs, deployment config. | Hosting configuration, DNS, external forms, analytics. | Confirm route refresh behavior, asset paths, sitemap, robots, SSL, caching, and deployment root. |
| Redesign Project | Versioned implementation files and docs. | Legacy CMS state, current hosting, redirects, analytics history, content ownership. | Audit the existing site first. Map old URLs, redirects, content, SEO, assets, and deployment risks. |

## React/Vite Startup Checks

- Confirm static, SPA, prerendered, or mixed behavior.
- Define approved routes before implementation.
- Confirm SEO config, sitemap, robots, canonicals, and OG image handling.
- Confirm typecheck/build commands and expected output.
- Check hydration when prerendered HTML is used.
- Confirm image derivative paths and AVIF/WebP MIME behavior.
- Confirm `.htaccess` or equivalent hosting config where relevant.

## Next.js Startup Checks

- Confirm App Router or Pages Router.
- Confirm static generation, server rendering, incremental regeneration, or client rendering.
- Confirm hosting target and environment variable handling.
- Confirm image optimization and external image rules.
- Confirm API routes, middleware, and dynamic routes.
- Adapt docs and validation commands to the project. Do not assume Vite commands apply.

## WordPress And WooCommerce Startup Checks

- Confirm admin, hosting, file, database, and staging access.
- Confirm full files, database, and media backup strategy.
- Confirm theme, builder, plugin, SEO, forms, cache, multilingual, and analytics setup.
- Export Elementor, ACF, forms, or settings where applicable.
- For WooCommerce, identify product, order, customer, payment, and migration risks.
- Do not perform risky production changes without backup and rollback context.

## SEO And Localization Warnings

- Do not invent routes or slugs.
- Define public, private, draft, and noindex rules.
- Map redirects for redesigns.
- Keep language, canonicals, metadata, UI labels, and alt text consistent.
- Confirm sitemap and robots behavior before launch.
- Do not use unsupported claims.

## Stop Before Implementation When

- Platform or rendering model is unclear.
- Existing project files have not been audited.
- Repository or working tree state is unclear.
- Deployment target is unknown.
- WordPress/WooCommerce backup or staging is missing for risky work.
- Legacy URLs or SEO migration needs are unknown for a redesign.
- Required access, credentials, or ownership is missing.
- Local preview or the first browser-visible baseline cannot be verified.

