# Image Asset Register

Status: Draft

## Purpose

Tracks image assets, image roles, filenames, locations, optimized derivatives, alt text, and implementation status.

## Usage Notes

- Plan images as a visual system, not as random replacements.
- Separate source, optimized, and runtime usage.
- Use `[TBD]` until files and roles are confirmed.

## Asset Governance Rules

- Use semantic folders.
- Use English filenames.
- Localize alt text.
- Avoid repeated generic images unless intentional.
- Avoid external fallback images unless approved.
- Generate optimized derivatives when required.
- Confirm files exist before runtime replacement.
- Do not move assets without mapping.

## Folder Model

| Folder | Purpose | Notes |
| --- | --- | --- |
| images/ | Main image folder | [TBD] |
| images/hero or semantic equivalent | Hero images | [TBD] |
| images/shared | Shared images | [TBD] |
| images/services | Service images | [TBD] |
| images/products | Product images | [TBD] |
| images/industries | Industry images | [TBD] |
| images/about | About/company images | [TBD] |
| optimized/ | Optimized derivatives | [TBD] |
| icons/ | Icons | [TBD] |
| patterns/ | Backgrounds/patterns | [TBD] |

## Naming Model

- Recommended structure: `[topic]-[specific-context]-[detail].[ext]`
- Example: `[project-topic]-[page-context]-[detail].webp`
- Anti-example: `image1.jpg`, `final-final.png`, `stock-photo.webp`
- Collision notes: keep derivative basenames tied to source basenames and avoid duplicated flattened filenames.

## Asset Register Table

| Image ID | Source Path | Optimized Path / Base | Route / Page | Component / Location | Role | Image Type | Status | Priority | Alt Text | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IMG-001 | [TBD] | [TBD] | [TBD] | [TBD] | PageHero / hero | [TBD] | planned | Medium | [TBD] | [TBD] |

## Status Model

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

## Image Roles

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

## Optimization Requirements

- Required sizes/formats: [TBD]
- AVIF/WebP/JPG/PNG considerations: [TBD]
- Responsive image notes: [TBD]
- WordPress media optimization notes: [TBD]
- React/Vite optimized derivative notes: [TBD]
- MIME/server checks: [TBD]

## Visual QA Notes

- [ ] Image matches page intent.
- [ ] Crop works on desktop.
- [ ] Crop works on mobile.
- [ ] No fake readable text.
- [ ] No fake logos.
- [ ] No unsupported visual claims.
- [ ] No repeated generic image unless intentional.
- [ ] Alt text matches language and content.

