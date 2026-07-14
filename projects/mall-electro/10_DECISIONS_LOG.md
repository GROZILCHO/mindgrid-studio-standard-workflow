# Decisions Log - Mall Electro

| Decision ID | Date | Decision | Reason | Status | Impact | Reversal Condition |
| --- | --- | --- | --- | --- | --- | --- |
| DEC-0001 | 2026-07-14 | BG remains the default locale. | Bulgarian is the original primary public language. | Accepted | Root and language behavior remain anchored around BG-first structure. | Rosen / MindGrid Studio approves a different default-locale strategy. |
| DEC-0002 | 2026-07-14 | Root redirects to `/bg/`. | Keeps entry behavior aligned with BG default locale. | Accepted | Supports consistent language routing. | Default locale strategy changes. |
| DEC-0003 | 2026-07-14 | Legal routes remain BG-only until separately approved. | Romanian legal routes are absent and should not be invented. | Accepted | Prevents unsupported legal/localization content. | EN/RO legal strategy is approved. |
| DEC-0004 | 2026-07-14 | Locale-neutral route keys are used across languages. | Keeps route/content mapping stable across BG/EN/RO. | Accepted | Reduces localization drift. | Routing model is redesigned. |
| DEC-0005 | 2026-07-14 | New locales require content, runtime, switcher, and SEO phase gates. | Multilingual activation must be validated end to end. | Accepted | Prevents partial public locale activation. | PM approves a different localization gate model. |
| DEC-0006 | 2026-07-14 | New locale preview may use `noindex` before public activation. | Preview should not expose incomplete localization to search. | Accepted | Supports controlled QA before indexing. | SEO strategy changes. |
| DEC-0007 | 2026-07-14 | Sitemap and hreflang activation occur only after content and runtime QA. | SEO publication should follow validated content/runtime state. | Accepted | Reduces indexing and canonical mistakes. | PM approves emergency SEO publication. |
| DEC-0008 | 2026-07-14 | GitHub is the durable implementation source of truth. | The application repository stores implementation state and evidence. | Accepted | PMO docs link to, but do not replace, application source. | Repository ownership model changes. |
| DEC-0009 | 2026-07-14 | The central project instance is PMO metadata, not a source-code mirror. | Prevents duplication and stale technical copies. | Accepted | `projects/mall-electro/` stays compact and operational. | PM approves a different documentation architecture. |
| DEC-0010 | 2026-07-14 | `examples/mall-electro/` remains a reusable case study, not an operational project folder. | Preserves examples as sanitized reusable lessons. | Accepted | Operational status belongs in `projects/mall-electro/`. | Repository architecture changes. |

