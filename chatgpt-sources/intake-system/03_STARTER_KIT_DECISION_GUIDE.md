# Starter Kit Decision Guide

Status: Source Pack

## Purpose

Choose the documentation starter kit that best matches the project. Starter kits are project-start documentation bases, not full application scaffolds.

## Decision Table

| Starter Kit | Use When | Key Notes |
| --- | --- | --- |
| `starter-kit/general` | Platform is undecided, discovery is still active, or the project needs strategy-first documentation. | Start here when the technical direction is unclear. Move to a platform-specific workflow after the decision. |
| `starter-kit/react-vite` | Project is a React/Vite website, static/prerendered site, SEO-oriented company site, product site, or landing system. | GitHub can usually store nearly the full project truth. Add real app files separately. |
| `starter-kit/wordpress` | Project is WordPress, WooCommerce, Elementor, Gutenberg, custom theme, child theme, or plugin-controlled work. | GitHub stores code/docs, but database, media, admin settings, builder layouts, and plugin state require separate handling. |

## Platform Notes

### Next.js Projects

Use `starter-kit/react-vite` only as general React documentation structure guidance. Adapt project docs to Next.js routing, rendering mode, data fetching, build output, hosting, middleware, image handling, and deployment rules. Do not assume Vite commands or static output behavior apply.

### WooCommerce Redesigns

Use `starter-kit/wordpress`. Confirm backups, staging, products, orders, customers, payment behavior, plugins, theme/builder strategy, and migration risks before implementation.

### Static Sites

Use `starter-kit/react-vite` when a React/Vite static or prerendered build is planned. Use `starter-kit/general` for plain HTML/static work until the implementation model is confirmed.

### Landing Pages

Use `starter-kit/general` if platform choice is open. Use the matching platform starter if the landing page belongs to an existing React/Vite, Next.js, or WordPress project.

### Existing Projects With Files Already Present

- Inspect before copying files.
- Preserve current project structure unless a scoped task approves changes.
- Add or adapt docs without overwriting implementation files.
- Run a read-only Codex audit before requesting changes.
- Record do-not-touch areas in `PROJECT_RULES.md` and `CURRENT_STATUS.md`.

## Stop Conditions

Stop before selecting a starter kit when:

- The platform is unclear and existing files have not been inspected.
- Copying starter docs could overwrite project-specific files.
- WordPress database/admin risks are unknown.
- Next.js is being treated as identical to React/Vite.
- Existing deployment behavior is undocumented.

