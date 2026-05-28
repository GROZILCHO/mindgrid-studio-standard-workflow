# WordPress Workflow

Status: Draft

## 1. Purpose

This workflow defines how WordPress websites should be handled inside the MindGrid Studio Standard Workflow.

WordPress projects require a different operating model than React/Vite projects because not everything lives in GitHub. A WordPress site can depend on code files, database state, media uploads, plugin settings, theme settings, page builder layouts, server configuration, and admin-only content.

The goal is to make WordPress projects repeatable, recoverable, documented, and safe to operate across Rosen / MindGrid Studio, ChatGPT Lead Assistant, Codex, GitHub, and Notion.

## 2. Core Principle

GitHub is reliable for code and documentation, but WordPress also depends on database state, media files, plugin settings, theme settings, page builder layouts, and server configuration.

Therefore WordPress projects must use:

- GitHub for code and documentation.
- WordPress admin for CMS/page content.
- Staging environment for safe changes.
- Database and media backups for recoverability.
- Exports for Elementor, ACF, options, forms, SEO settings, or other plugin data where applicable.
- Notion for operational task tracking.

Do not treat a WordPress project as complete just because the repository is clean. The live site state must also be backed up, exported where possible, and manually QA-tested.

## 3. What GitHub Should Store

GitHub should store file-based project memory and implementation assets:

- Custom theme: project-specific theme files.
- Child theme: overrides and customizations for a parent theme.
- Custom plugin: project-specific behavior that should not live in theme files.
- MU-plugin: must-use functionality that should load independently of normal plugin activation.
- Theme template parts: reusable PHP, block, or template files.
- `functions.php` changes: documented, scoped theme behavior.
- Custom CSS/SCSS: project-specific styling.
- Custom JavaScript: project-specific frontend behavior.
- Block patterns if file-based: reusable block structures stored as files.
- ACF JSON files if ACF is used: field group definitions that can be versioned.
- Translation files if file-based: `.po`, `.mo`, or related language files.
- Deployment notes: hosting, environment, release, and rollback instructions.
- Project documentation: project brief, rules, site structure, content model, design system, and SEO plan.
- QA checklists: repeatable checks before deployment.
- Decisions log: real project decisions and reasons.
- Current status: active phase, validation, issues, and next task.
- Issue log: bugs, risks, blockers, unresolved questions, and production observations.
- Handoff documents: context for switching chats, agents, or project phases.

Codex can work safely on these files when the task defines allowed files, forbidden files, backup status, staging/production target, and validation method.

## 4. What GitHub Does Not Fully Control

GitHub does not reliably store these WordPress parts by default:

- WordPress database.
- Posts and pages content.
- Elementor layouts stored in the database.
- Media library uploads.
- Plugin settings.
- WordPress options.
- Menus.
- Widgets.
- Users and roles.
- WooCommerce products, orders, and customers.
- Form submissions.
- Redirects created through plugins.
- SEO plugin settings.
- Cache plugin settings.

These items require backup, export, migration, staging, and manual QA strategy. If an implementation depends on any of them, the task must document how the current state is captured and how rollback works.

## 5. Recommended WordPress Project Repository Structure

Use a practical structure that separates documentation, WordPress code, exports, and backup notes:

```txt
project-name/
├─ README.md
├─ AGENTS.md
├─ docs/
│  ├─ PROJECT_BRIEF.md
│  ├─ PROJECT_RULES.md
│  ├─ SITE_STRUCTURE.md
│  ├─ CONTENT_MODEL.md
│  ├─ DESIGN_SYSTEM.md
│  ├─ SEO_PLAN.md
│  ├─ IMAGE_ASSET_REGISTER.md
│  ├─ QA_CHECKLIST.md
│  ├─ CURRENT_STATUS.md
│  ├─ NEXT_ACTIONS.md
│  ├─ ISSUES_LOG.md
│  ├─ DECISIONS_LOG.md
│  ├─ PROJECT_HANDOFF.md
│  └─ DEPLOYMENT_GUIDE.md
├─ wordpress/
│  ├─ themes/
│  │  └─ custom-theme-or-child-theme/
│  ├─ plugins/
│  │  └─ project-custom-plugin/
│  ├─ mu-plugins/
│  └─ acf-json/
├─ exports/
│  ├─ elementor/
│  ├─ acf/
│  ├─ seo/
│  └─ forms/
└─ backups/
   └─ README.md
```

Large database and media backups should generally not be committed to GitHub unless intentionally stored through a separate backup strategy. The repository should document where those backups live, who owns them, when they were created, and how they can be restored.

## 6. Project Phases For WordPress

### Project Setup

Purpose: create the repository, copy starter documentation, and define the WordPress operating model.

Key questions:

- Is this a new WordPress project or an existing site?
- What repository structure will be used?
- What environments exist?
- What files may Codex edit?

Expected outputs:

- README.md
- AGENTS.md
- PROJECT_RULES.md
- CURRENT_STATUS.md
- DEPLOYMENT_GUIDE.md

Complete when: the repository and baseline docs exist, access requirements are known, and no risky site changes are planned without backup/staging notes.

### WordPress Intake

Purpose: understand the existing or planned WordPress system.

Key questions:

- What hosting, theme, builder, plugins, and content already exist?
- What access is available?
- Are backups, exports, and staging available?

Expected outputs:

- PROJECT_BRIEF.md
- PROJECT_RULES.md
- ISSUES_LOG.md for missing access or risks

Complete when: project state, access, risks, and constraints are documented.

### Site Architecture

Purpose: define routes, page hierarchy, navigation, menus, taxonomies, and core user journeys.

Key questions:

- What pages and menus are needed?
- What content types are required?
- Are redirects or legacy URLs involved?

Expected outputs:

- SITE_STRUCTURE.md
- SEO_PLAN.md
- DECISIONS_LOG.md where route decisions are made

Complete when: page structure, navigation, and redirect requirements are approved.

### Content Model

Purpose: define page content, post types, fields, reusable sections, and language requirements.

Key questions:

- What content is entered in WordPress admin?
- What content is stored in files?
- Are custom fields needed?
- What must be multilingual?

Expected outputs:

- CONTENT_MODEL.md
- SEO_PLAN.md
- ACF export plan if applicable

Complete when: page types, fields, content sections, and metadata requirements are clear.

### Theme/Page Builder Strategy

Purpose: choose the implementation approach before building pages.

Key questions:

- Custom theme, child theme, block theme, Elementor, or hybrid?
- Where will layouts live?
- What can be versioned in GitHub?
- What needs export?

Expected outputs:

- DESIGN_SYSTEM.md
- PROJECT_RULES.md
- DECISIONS_LOG.md

Complete when: the build approach and layout ownership are documented.

### Plugin Strategy

Purpose: define required plugins and avoid uncontrolled plugin growth.

Key questions:

- Which plugins are necessary?
- Which plugins overlap?
- Which are critical?
- Which settings need export or screenshots?

Expected outputs:

- PROJECT_RULES.md
- DEPLOYMENT_GUIDE.md
- Plugin register

Complete when: required plugins, licenses, criticality, and export needs are documented.

### Visual Asset Planning

Purpose: prepare images and media before page building.

Key questions:

- What image types are needed?
- What should be optimized before upload?
- What alt text is required?
- What must not be reused?

Expected outputs:

- IMAGE_ASSET_REGISTER.md
- SEO_PLAN.md

Complete when: required assets, filenames, alt text, and usage locations are documented.

### Development / Configuration

Purpose: implement file-based code and configure WordPress safely through staging or documented admin actions.

Key questions:

- What files are being changed?
- What admin settings are being changed?
- Is staging available?
- What rollback exists?

Expected outputs:

- GitHub code/docs updates
- Export updates where applicable
- CURRENT_STATUS.md

Complete when: implementation is done, validation is run, and changes are documented.

### Content Entry

Purpose: enter or migrate approved content into WordPress.

Key questions:

- Which pages are ready?
- What content needs approval?
- Are SEO titles and descriptions ready?
- Are media and alt text ready?

Expected outputs:

- Content entry checklist
- SEO_PLAN.md updates
- QA_CHECKLIST.md updates

Complete when: content is entered, structured, reviewed, and ready for QA.

### QA

Purpose: verify the WordPress site across routes, content, visuals, forms, plugins, SEO, performance, and deployment readiness.

Key questions:

- Do all key pages work?
- Are forms sending correctly?
- Are plugin settings correct?
- Are SEO and performance acceptable?

Expected outputs:

- QA_CHECKLIST.md
- ISSUES_LOG.md
- CURRENT_STATUS.md

Complete when: major issues are resolved or explicitly accepted for launch.

### Deployment / Migration

Purpose: move approved changes safely to production.

Key questions:

- Is backup complete?
- Is staging approved?
- What deployment method is used?
- What post-deploy checks are required?

Expected outputs:

- DEPLOYMENT_GUIDE.md
- CURRENT_STATUS.md
- ISSUES_LOG.md if deployment issues appear

Complete when: production is updated, smoke-tested, and documented.

### Post-launch

Purpose: monitor production, resolve launch issues, and capture follow-up work.

Key questions:

- Are forms, SEO, tracking, redirects, and performance working?
- Are there production-only issues?
- What should be improved next?

Expected outputs:

- CURRENT_STATUS.md
- NEXT_ACTIONS.md
- ISSUES_LOG.md
- PROJECT_RETROSPECTIVE.md

Complete when: post-launch checks are done and follow-up work is documented.

## 7. WordPress Intake Questions

Use this checklist during intake:

- Is this a new site or redesign?
- Is there existing hosting?
- Is there an existing WordPress installation?
- Is admin access available?
- Is FTP/cPanel access available?
- Is database access available?
- Is staging available?
- What theme is currently used?
- What page builder is used?
- Elementor, Gutenberg, custom theme, or another builder?
- Is WooCommerce involved?
- Is this a multilingual site?
- Which SEO plugin is used?
- Which forms plugin is used?
- What analytics/tracking is required?
- Are cookie consent requirements known?
- Which backup plugin is used?
- Which cache/performance plugin is used?
- What are the current pain points?
- What is the target launch date?

Missing access, missing backups, or unclear ownership should be recorded in ISSUES_LOG.md.

## 8. Theme And Builder Strategy

Choose the build approach before page building:

| Approach | Use When | GitHub Control | Export Need |
| --- | --- | --- | --- |
| Custom theme | The site needs a controlled, file-based implementation. | High | Low to medium |
| Child theme | A parent theme is required but customizations must be versioned. | Medium to high | Medium |
| Block theme | The project uses modern WordPress block templates and patterns. | Medium to high if file-based | Medium |
| Elementor-based build | Speed, editor control, or client editing is more important than full file control. | Low to medium | High |
| Hybrid approach | Some parts need code control and some need builder flexibility. | Mixed | Medium to high |

Guidance:

- Do not start with page building before PROJECT_BRIEF.md, SITE_STRUCTURE.md, and DESIGN_SYSTEM.md are clear.
- Avoid mixing too many design systems.
- If Elementor is used, define global colors, typography, spacing, and template structure first.
- If a custom theme is used, GitHub becomes more important.
- If page builder layout lives in the database, an export strategy is required.

## 9. Plugin Governance

Plugin rules:

- Install only necessary plugins.
- Document every plugin in PROJECT_RULES.md or DEPLOYMENT_GUIDE.md.
- Record each plugin purpose.
- Avoid overlapping plugin functionality.
- Avoid plugin bloat.
- Check compatibility before updates.
- Do not update plugins on production without backup.
- Document premium license dependencies.
- Record SEO, cache, security, forms, and multilingual plugins.

Sample plugin register:

| Plugin | Purpose | Critical? | License | Settings Exported? | Notes |
| --- | --- | --- | --- | --- | --- |
| Placeholder plugin | Placeholder purpose | Yes/No | Free/Premium | Yes/No | Placeholder notes |

## 10. Content Workflow

Content should be planned before page building:

- Define the content model before page creation.
- Approve the page list before page creation.
- Plan SEO titles and meta descriptions before launch.
- Avoid unsupported claims.
- Control Bulgarian/English language consistency.
- Make page builder sections follow the approved site structure.
- Give media assets naming and alt text rules.

Content entered only in WordPress admin should be reflected in docs at least as structure, page intent, and QA notes.

## 11. Visual Asset Workflow For WordPress

WordPress visual assets should be planned before implementation:

- Plan the image set before implementation.
- Use IMAGE_ASSET_REGISTER.md.
- Define hero, section, CTA, card, OG, and gallery images.
- Optimize images before upload.
- Avoid repeated generic visuals.
- Use descriptive English filenames.
- Localize alt text per language.
- Do not rely on external image URLs.
- Keep original/source images outside the live media library when needed.

The media library is not a strategy. It is the runtime asset store. Source, optimized, and usage decisions should be documented before upload.

## 12. Backup And Staging Strategy

Before major changes:

- Create a full database backup.
- Create a full files backup.
- Create or verify a media library backup.
- Export Elementor templates if applicable.
- Export ACF field groups if applicable.
- Export forms if applicable.
- Document plugin versions.

Use staging for:

- Redesigns.
- Theme changes.
- Plugin changes.
- WooCommerce changes.
- Migration testing.
- Performance changes.

Do not make large structural changes directly on production unless explicitly approved.

## 13. Codex Role In WordPress Projects

Codex can do well:

- Edit theme files.
- Create child theme files.
- Write custom plugin code.
- Prepare CSS/JS snippets.
- Create documentation.
- Review file structure.
- Prepare deployment checklists.
- Generate QA tasks.
- Inspect GitHub-based code.

Codex cannot reliably do without additional access:

- Inspect WordPress database state.
- See Elementor layouts unless exported.
- Verify admin settings unless documented.
- Know plugin settings unless exported or screenshotted.
- Manage media library unless files are provided.

Codex tasks must include:

- Allowed files.
- Forbidden files.
- Backup status.
- Staging/production target.
- Validation method.
- Rollback plan if relevant.

## 14. WordPress QA Gates

QA gates:

- Route/page QA.
- Navigation QA.
- Responsive QA.
- Form QA.
- SEO metadata QA.
- Schema QA if used.
- Image/alt QA.
- Plugin conflict QA.
- Performance QA.
- Cache QA.
- Cookie consent QA.
- Search Console readiness.
- Backup/restore readiness.
- Production smoke test.

Do not proceed to launch if major route, form, SEO, plugin conflict, backup, or deployment risks remain unresolved.

## 15. Deployment / Migration Protocol

Before deployment:

- Confirm backup.
- Confirm staging approval.
- Confirm plugin versions.
- Confirm theme files.
- Confirm exports.
- Confirm redirects if redesign.
- Confirm SEO metadata.
- Confirm analytics/cookie consent plan.

Deployment methods may include:

- Manual upload.
- Git-based deploy.
- Hosting file manager.
- Migration plugin.
- Staging-to-production push.
- Theme/plugin zip upload.

After deployment:

- Flush permalinks.
- Clear cache.
- Test homepage.
- Test key pages.
- Test forms.
- Test mobile.
- Test sitemap.
- Test robots.txt.
- Test SSL.
- Test redirects.
- Test admin access.
- Run Lighthouse / PageSpeed.
- Check console errors.

## 16. Post-launch Workflow

After launch:

- Set up or verify Google Search Console.
- Submit sitemap.
- Verify Analytics / Tag Manager.
- Check cookie consent.
- Set up uptime/basic monitoring where applicable.
- Test form submissions.
- Check 404s and redirects.
- Monitor Core Web Vitals.
- Plan content expansion.
- Update CURRENT_STATUS.md and PROJECT_RETROSPECTIVE.md.

## 17. Stop Conditions

Codex or the project operator should stop and report if:

- Working tree is dirty unexpectedly.
- Production backup is missing.
- Staging is unavailable for a risky change.
- Plugin update may break the site.
- Database migration is unclear.
- Elementor/ACF export is missing.
- WooCommerce data could be affected.
- Client approval is missing.
- Credentials are incomplete.
- Task requires modifying files outside allowed scope.
- Validation fails.

## 18. Operating Principle

Do not treat WordPress as only files.
Do not treat the database as invisible.
Do not edit production blindly.
Use GitHub for code and memory, staging for safe implementation, backups for recovery, and documentation for continuity.

