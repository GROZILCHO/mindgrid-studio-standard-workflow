# Image Asset Register

Status: Draft

## Purpose

This document tracks image assets, image roles, filenames, locations, optimized derivatives, alt text, and implementation status.

Images should be planned as a visual system, not added randomly during implementation.

## Usage Notes

- Use this before changing image paths or replacing runtime visuals.
- Keep source, optimized, and runtime usage separate.
- Update status as assets move from planning to implementation.
- Use this for React/Vite static assets and WordPress media-library planning.

## 1. Asset Governance Rules

- Use semantic folders.
- Use English filenames.
- Avoid role words in filenames when possible unless project chooses otherwise.
- Localize alt text.
- Avoid repeated generic images unless intentional.
- Avoid external fallback images unless approved.
- Generate optimized derivatives when required.
- Confirm files exist before runtime replacement.
- Separate source, optimized, and runtime usage.

## 2. Folder Model

| Folder | Purpose | Notes |
| --- | --- | --- |
| images/ | Main source/runtime image folder | Adapt per project |
| images/hero or semantic equivalent | Hero/PageHero images | Use semantic naming where possible |
| images/shared | Shared reusable images | Avoid overuse |
| images/services | Service-related images | Project-specific |
| images/products | Product-related images | Project-specific |
| images/industries | Industry-related images | Project-specific |
| images/about | Company/team/about images | Project-specific |
| optimized/ | Optimized derivatives | AVIF/WebP/JPG outputs if used |
| icons/ | Icons | Prefer approved icon system |
| patterns/ | Backgrounds/patterns | Keep lightweight |

Exact folder model should be adapted per project.

## 3. Naming Model

Recommended filename structure:

- `brand-or-topic-specific-description.ext`
- `product-or-service-context-detail.ext`
- `page-or-cluster-specific-visual.ext`

Examples:

- `industrial-control-panel-assembly.webp`
- `solar-inverter-installation-detail.avif`
- `company-team-workshop-review.jpg`

Anti-examples:

- `image1.jpg`
- `hero-final-final.png`
- `stock-photo-business.webp`
- `new-image-copy-2.jpg`

Collision prevention notes for optimized derivatives:

- Keep derivative basename tied to the source basename.
- Avoid duplicate basenames across folders when build tools flatten output.
- Document generated size/format variants if used.

## 4. Asset Register Table

| Image ID | Source Path | Optimized Path / Base | Route / Page | Component / Location | Role | Image Type | Status | Priority | Alt Text | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IMG-001 | Placeholder | Placeholder | Placeholder | Placeholder | PageHero / hero | Photo/Illustration/Icon | planned | Medium | Placeholder | Placeholder |

## 5. Status Model

- planned
- generated
- received
- approved
- approved-for-optimization
- optimized
- implemented
- rejected
- needs-replacement
- archived

## 6. Image Roles

- PageHero / hero.
- Section image.
- CTA background.
- Card image.
- Product image.
- Process image.
- Support image.
- OG image.
- Icon/illustration.
- Background/pattern.

## 7. Optimization Requirements

- Required sizes/formats:
- AVIF/WebP/JPG/PNG considerations:
- Responsive image notes:
- WordPress media optimization notes:
- React/Vite optimized derivative notes:
- MIME/server checks:

## 8. Visual QA Notes

- [ ] Image matches page intent.
- [ ] Crop works on desktop.
- [ ] Crop works on mobile.
- [ ] No fake readable text.
- [ ] No fake logos.
- [ ] No unsupported visual claims.
- [ ] No repeated generic image unless intentional.
- [ ] Alt text matches language and content.

