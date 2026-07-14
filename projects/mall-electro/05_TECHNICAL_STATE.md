# Technical State - Mall Electro

## Architecture Summary

- Platform: React / Vite / TypeScript.
- Styling: Tailwind CSS.
- Output model: SSR/prerendered static output.
- Public languages: Bulgarian, English, Romanian.
- Primary branch: `main`.

## Current Implementation Status

- Bulgarian site: active.
- English localization: active.
- Romanian localization: complete and merged.
- Romanian runtime routes: active.
- Romanian language switcher: active.
- Romanian sitemap: active.
- Romanian hreflang: active.
- Romanian indexing: active.
- Romanian legal routes: not implemented.

## Route And Sitemap State

- Prerendered routes: 76.
- Sitemap URLs: 75 total.
- English URLs: 24.
- Romanian URLs: 24.
- BG/EN/RO reciprocal hreflang: active on approved page groups.
- Canonicals: self-referencing.
- Romanian routes: indexable.
- BG legal routes: BG only.

## Validation State

| Check | Status |
| --- | --- |
| Content parity guard | Passed |
| Encoding guard | Passed |
| Typecheck | Passed |
| Build | Passed |
| i18n output guard | Passed |
| Git diff check | Passed |

## Release History

| Milestone | Summary |
| --- | --- |
| BG site baseline established | Bulgarian baseline site and routing established. |
| EN localization activated | English public language layer activated. |
| Responsive and visual stabilization | UI and responsive behavior stabilized through QA. |
| English runtime SEO title correction | English SEO title runtime issue corrected. |
| English solution hero-image corrections | English solution page hero-image issues corrected. |
| Romanian content batches completed | Romanian content batches completed and integrated. |
| Romanian runtime preview activated | Romanian runtime output activated for preview/QA. |
| Romanian language switcher activated | Romanian option added to language switching behavior. |
| Romanian editorial QA completed | Romanian content passed project editorial QA; native review remains advisable. |
| Romanian SEO, sitemap and hreflang activated | Romanian SEO visibility, sitemap entries, and hreflang activated. |
| `feature/ro-localization` merged into `main` | Localization branch integrated into primary branch. |

## Known Non-Blocking Technical Observations

- Stale Browserslist data warning.
- Large main bundle warning.
- Native Romanian editorial review remains advisable.

## Production Status

- Repository state: release-ready in `main`.
- Production deployment: not confirmed in this PMO instance.
- Live production verification: not confirmed in this PMO instance.

## Technical Boundary

This file records compact operational status. The application repository remains authoritative for source code, build scripts, assets, route implementation, and detailed technical evidence.

