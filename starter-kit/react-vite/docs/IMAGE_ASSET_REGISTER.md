# Image Asset Register

Status: Draft

## Purpose

Tracks React/Vite image assets, source files, optimized derivatives, runtime paths, alt text, and implementation status.

## Usage Notes

- Plan images as a visual system.
- Separate source assets from optimized derivatives.
- Runtime image paths must match actual files.

## Asset Governance Rules

- Use semantic folders.
- Use English filenames.
- Localize alt text.
- Avoid repeated generic images unless intentional.
- Avoid external fallback images unless approved.
- Generate AVIF/WebP derivatives when required.
- Confirm files exist before runtime replacement.
- Check hosting MIME behavior for AVIF/WebP.

## Folder Model

| Folder | Purpose | Notes |
| --- | --- | --- |
| images/ | Main image folder | [TBD] |
| images/hero or semantic equivalent | Hero images | [TBD] |
| images/shared | Shared images | [TBD] |
| optimized/ | Optimized derivatives | [TBD] |
| icons/ | Icons | [TBD] |
| patterns/ | Backgrounds/patterns | [TBD] |

## Naming Model

- Recommended structure: `[topic]-[specific-context]-[detail].[ext]`
- Anti-example: `image1.jpg`, `hero-final-final.png`, `stock-photo.webp`
- Keep derivative basenames tied to source basenames.

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
- React/Vite optimized derivative notes: [TBD]
- Runtime path checks: [TBD]
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

