# Mall Electro Decisions Log Example

Status: Draft

## Purpose

This is an example/reference decisions log based on Mall Electro as a practical case study for MindGrid Studio Standard Workflow. It shows how real project decisions can be recorded without turning DECISIONS_LOG.md into a daily changelog.

## Usage Note

Use this document as a reference pattern only. Future projects should adapt the table structure, decision categories, and level of detail to their own context. Do not treat Mall Electro decisions as required decisions for other projects.

## Example Decision Table

| Date / Phase | Decision | Reason | Alternatives Considered | Impact | Related Files / Areas | Follow-up |
|---|---|---|---|---|---|---|
| Project setup | Use GitHub as project memory. | The project needed durable context across ChatGPT Lead Assistant, Codex, and Rosen / MindGrid Studio. | Keep context only in chat; use Notion as the main technical memory. | GitHub became the source of truth for docs, implementation files, audit results, and handoff context. | AGENTS.md, CURRENT_STATUS.md, PROJECT_HANDOFF.md | Keep docs current when project state changes. |
| Workflow extraction | Use Variant B workflow model. | One master workflow repository with reusable starter kits allows React/Vite, WordPress, and general projects to coexist. | One direct template repository for all projects; separate unrelated workflow repositories. | Starter kits can evolve independently while the master workflow stays clean. | workflow/, starter-kit/, platform-workflows/ | Review after more projects. |
| Image pipeline | Separate runtime PageHero image implementation from SEO `ogImage` updates. | Runtime images and Open Graph images have different QA needs and risk profiles. | Update all image usage in one task. | Reduced accidental SEO drift and made validation easier. | IMAGE_ASSET_REGISTER.md, SEO_PLAN.md, PageHero usage | Keep image and SEO tasks scoped separately when possible. |
| Image governance | Use semantic image folders and reusable filenames. | Generated images created folder and naming ambiguity during implementation. | Use image role names directly in every filename; place images wherever convenient. | Improved asset traceability and reduced broken runtime paths. | IMAGE_ASSET_REGISTER.md, assets/images, optimized images | Define folder rules before implementation. |
| Content safety | Avoid unsupported response-time claims. | Claims like fast response promises require proof or approval. | Keep stronger marketing claims without evidence. | Reduced legal/content risk and made copy safer for launch. | CONTENT_MODEL.md, PROJECT_RULES.md, page copy | Mark uncertain claims for Rosen / MindGrid Studio review. |
| QA method | Use read-only audit tasks before implementation tasks. | Audits clarified route, SEO, asset, and performance risks before Codex changed files. | Let Codex audit and fix in one broad task. | Better scope control and clearer issue reporting. | CODEX_AUDIT_TEMPLATE.md, ISSUES_LOG.md, QA_CHECKLIST.md | Keep audit-only tasks explicit. |
| Platform workflow | Keep WordPress and React/Vite workflows separate. | React/Vite is file-based, while WordPress depends on database/admin/media/plugin state. | Use one generic deployment workflow for both platforms. | Made future project guidance more accurate and reduced dangerous assumptions. | REACT_VITE_WORKFLOW.md, WORDPRESS_WORKFLOW.md | Update platform notes after future projects. |
| Operations layer | Use Notion as operations layer, not implementation source of truth. | Notion is useful for task visibility, but GitHub should store implementation rules and durable docs. | Store detailed implementation requirements only in Notion. | Improved continuity for Codex and new ChatGPT sessions. | NOTION_TASK_MAPPING.md, TASK_STATUS_MODEL.md | Mirror task status at an operational level only. |

## Adaptation Notes

- Record only real strategic, architectural, technical, content, SEO, design, workflow, or deployment decisions.
- Do not use DECISIONS_LOG.md as a daily activity log.
- Link decisions to files, tasks, or affected areas when useful.
- Record follow-up work in NEXT_ACTIONS.md or Notion if operational tracking is needed.
