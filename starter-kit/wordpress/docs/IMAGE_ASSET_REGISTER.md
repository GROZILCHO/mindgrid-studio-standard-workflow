# Image Asset Register

Status: Draft

## Purpose

Tracks WordPress media assets, source files, upload locations, optimized versions, alt text, image roles, and implementation status.

## Usage Notes

- Plan images before upload or page-builder placement.
- WordPress media library is runtime storage, not the full asset strategy.
- Keep original/source images outside the live media library when needed.

## Asset Governance Rules

- Use semantic filenames where possible.
- Localize alt text in WordPress media.
- Avoid duplicate generic media uploads.
- Avoid external fallback images unless approved.
- Optimize images before upload where possible.
- Track featured images, OG images, Elementor backgrounds, and WooCommerce product images if relevant.

## Folder / Media Model

| Location | Purpose | Notes |
| --- | --- | --- |
| WordPress media library | Runtime uploaded media | [TBD] |
| Source image storage | Original/source files | [TBD] |
| Optimized uploads | Compressed/converted upload files | [TBD] |
| Elementor/background images | Builder-specific media usage | [TBD] |
| WooCommerce product images | Product/gallery images | [TBD] |

## Naming Model

- Recommended structure: `[topic]-[specific-context]-[detail].[ext]`
- Anti-example: `image1.jpg`, `final-final.png`, `stock-photo.webp`
- Avoid duplicate filenames that make media library management unclear.

## Asset Register Table

| Image ID | Source Path | WordPress Media URL / ID | Page / Template | Component / Location | Role | Image Type | Status | Priority | Alt Text | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IMG-001 | [TBD] | [TBD] | [TBD] | [TBD] | Hero | [TBD] | planned | Medium | [TBD] | [TBD] |

## Status Model

- planned
- generated
- received
- approved
- approved-for-optimization
- optimized
- uploaded
- implemented
- rejected
- needs-replacement
- archived

## Image Roles

- Hero/PageHero.
- Section image.
- CTA background.
- Card image.
- Featured image.
- Product image.
- Gallery image.
- Elementor/background image.
- OG image.
- Icon/illustration.

## Optimization Requirements

- Required sizes/formats: [TBD]
- WebP/JPG/PNG considerations: [TBD]
- WordPress media optimization plugin/process: [TBD]
- Featured image sizes: [TBD]
- WooCommerce image sizes if relevant: [TBD]

## Visual QA Notes

- [ ] Image matches page intent.
- [ ] Crop works on desktop.
- [ ] Crop works on mobile.
- [ ] No fake readable text.
- [ ] No fake logos.
- [ ] No unsupported visual claims.
- [ ] No repeated generic image unless intentional.
- [ ] Alt text matches language and content.

