# Phase 07: Visual Asset Pipeline

Status: Draft

## Purpose

Plan, register, approve, optimize, and implement project visuals before they are used in pages, templates, or deployment packages.

## When To Use This Phase

Use this phase after the design system is clear and before image-heavy implementation, page building, SEO image mapping, or deployment optimization.

## Main Questions

- What image roles are needed?
- Which pages need hero, section, CTA, card, product, OG, or support images?
- What folder and naming rules apply?
- What alt text language is required?
- Which assets are source files, optimized derivatives, or runtime files?
- Are React/Vite AVIF/WebP derivatives required?
- Are WordPress media library uploads, featured images, or page builder backgrounds involved?
- Are repeated generic images being avoided?

## Required Inputs

- PROJECT_BRIEF.md.
- PROJECT_RULES.md.
- SITE_STRUCTURE.md.
- CONTENT_MODEL.md.
- DESIGN_SYSTEM.md.
- SEO_PLAN.md if image SEO or OG images are involved.
- Existing source assets if available.

## Expected Outputs

- IMAGE_ASSET_REGISTER.md updated.
- Image role list.
- Folder and filename rules.
- Alt text draft or rules.
- Source/optimized/runtime image mapping.
- React/Vite optimized derivative expectations where relevant.
- WordPress media library notes where relevant.
- Visual QA notes.

## Recommended Steps

1. Identify required image roles by page and component.
2. Record each planned image in IMAGE_ASSET_REGISTER.md.
3. Define folder and filename rules.
4. Define source, optimized, and runtime paths.
5. Draft localized alt text where needed.
6. Mark image status: Planned, In Progress, Review, Done, or Blocked.
7. Generate or collect assets only after roles are clear.
8. Optimize derivatives before runtime replacement.
9. Check repeated image usage and visual fit.
10. Record remaining visual issues.

## Codex / Agent Involvement

- Visual Prompt Designer may prepare visual direction and image prompt sets.
- ChatGPT Lead Assistant coordinates asset planning with content and SEO.
- Codex may update IMAGE_ASSET_REGISTER.md, inspect file paths, and implement image replacements only within scoped tasks.
- Rosen / MindGrid Studio approves image direction and final usage.

## Tracking Docs Update Rules

- Update CURRENT_STATUS.md after the asset plan becomes usable.
- Update NEXT_ACTIONS.md with concrete image generation, optimization, or replacement tasks.
- Update ISSUES_LOG.md for missing assets, broken paths, repeated generic images, or unresolved rights/approval risks.
- Update DECISIONS_LOG.md only for real image strategy, folder model, or optimization decisions.
- Update PROJECT_HANDOFF.md if pausing before implementation.

## Completion Criteria

- IMAGE_ASSET_REGISTER.md contains planned project visuals.
- Folder and naming rules are clear.
- Alt text and image SEO expectations are known.
- Optimization needs are documented.
- Visual QA risks are visible.

## Stop Conditions

- Image roles are unclear.
- Folder/naming rules are not approved.
- Required source assets are missing.
- Images may create unsupported claims.
- Runtime image paths cannot be verified.
- WordPress media or page builder image ownership is unclear.

## Handoff Notes

New sessions should inspect IMAGE_ASSET_REGISTER.md, DESIGN_SYSTEM.md, SEO_PLAN.md, CURRENT_STATUS.md, and ISSUES_LOG.md.
