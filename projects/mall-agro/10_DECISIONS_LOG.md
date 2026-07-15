# Decisions Log - Mall Agro Redesign

Only confirmed decisions from the source report are recorded here. Draft or inferred decisions must remain separate until PM approval.

| ID | Title | Status | Confirmed Meaning | Source Reference | Operational Effect |
| --- | --- | --- | --- | --- | --- |
| DEC-007 | Domain-based localization model | Approved | Domain-based localization with shared internal IDs and separate localized route/content/metadata configs is approved. | Application `docs/DECISIONS_LOG.md` per source report | Use domains and localized configs; do not introduce `/ro` route-prefix model. |
| DEC-008 | Design-system reference scope | Approved | Current design-system reference is approved as visual direction only, not final implementation source of truth. | Application `docs/DECISIONS_LOG.md` per source report | Do not treat reference visuals as automatic implementation authority. |
| DEC-009 | Temporary category `noindex` | Approved | English category pages temporarily use `noindex`. | Application `docs/DECISIONS_LOG.md` per source report | Do not make pages indexable casually before SEO/runtime approval. |
| DEC-010 | Separate domain-specific language versions | Approved | `mallagro.com` and `mallagro.ro` are separate domain-specific language versions. | Application `docs/DECISIONS_LOG.md` per source report | Language/domain architecture is approved; hosting and concrete deployment implementation remain unconfirmed. |
| DEC-011 | Approved-equivalent language switcher | Approved | Language switcher must only link approved equivalents; no guessed fallback. | Application `docs/DECISIONS_LOG.md` per source report | Do not create fallback links without approved route/content pairs. |
| DEC-012 | Agriculture benchmark accepted | Approved | Agriculture is accepted as Category Benchmark v1 in commit `80c3e30`. | Application `docs/DECISIONS_LOG.md` and commit `80c3e30` per source report | Future category pages should follow the Agriculture editorial/UX workflow, not copy wording directly. |

