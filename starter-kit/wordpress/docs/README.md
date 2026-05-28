# WordPress Project Docs

Status: Draft

## Purpose

This docs folder stores the durable project memory for a WordPress project. It should record both file-based implementation context and the WordPress state that GitHub cannot fully see.

## What These Docs Should Contain

- Project brief: business context, audience, goals, and constraints.
- Site structure: pages, menus, routes, redirects, and content hierarchy.
- Content model: page sections, post types, fields, language rules, and admin content ownership.
- Design system: visual direction, global styles, builder rules, and reusable layout patterns.
- Plugin register: installed plugins, purpose, criticality, license, and export status.
- Theme/builder strategy: custom theme, child theme, block theme, Elementor, Gutenberg, or hybrid approach.
- Backup/staging status: backup owner, backup date, staging URL/status, and rollback notes.
- Deployment guide: migration, theme/plugin updates, cache, permalink, and post-deploy checks.
- Current status: active phase, validation, git status, issues, and next task.
- Issues: bugs, blockers, risks, missing access, production observations, and unresolved questions.
- Decisions: real strategic, technical, content, SEO, design, plugin, or workflow decisions.
- Handoff: context for switching chats, agents, or phases.

## WordPress State Not Fully Visible In GitHub

Record or reference:

- Admin settings.
- Plugin settings.
- Page builder exports.
- Database/media backup status.

## Usage Rule

Before Codex implementation, confirm whether the task is file-based or depends on WordPress admin/database state.

