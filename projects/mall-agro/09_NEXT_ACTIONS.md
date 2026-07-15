# Next Actions - Mall Agro Redesign

## Immediate Action

| Priority | Action | Owner | Status | Dependencies | Acceptance Criteria |
| --- | --- | --- | --- | --- | --- |
| High | QA-only pre-commit review of the current Grain Processing implementation | Codex / QA under PM direction | Planned | Application repository access and current dirty worktree preserved | QA report confirms intended dirty files, copy-map match, shared renderer behavior, route safety, build/lint results, and artifact handling. |

## Stop Conditions

Stop the QA task if:

- The application working tree differs from the source report in unexpected ways.
- More files are dirty than expected.
- `grain-processing-local-diff.txt` is at risk of being committed accidentally.
- Grain Processing copy cannot be compared to `GRAIN_PROCESSING_PUBLIC_PAGE_COPY_MAP_v1.0`.
- Shared renderer changes appear to regress Agriculture, Food Industry, or Romanian placeholder routes.
- Build or lint fails.
- The task requires implementation edits instead of audit-only review.

## Recommended Next Codex Task Summary

```md
TASK - Mall Agro QA-only pre-commit review of Grain Processing implementation

Run a read-only QA review of the current uncommitted Grain Processing implementation in `GROZILCHO/mall-agro-redesign`.

Mandatory first step:
git status --short

Expected dirty state from PMO source report:
- `src/app/products/components/CategoryLandingPage.js`
- `src/lib/content/categoryPages.js`
- `grain-processing-local-diff.txt`

Audit only. Do not edit, stage, commit, delete, move, or rename files.

Verify:
- only intended files are dirty;
- Grain Processing copy matches `docs/editorial/GRAIN_PROCESSING_PUBLIC_PAGE_COPY_MAP_v1.0.md`;
- operating context index labels are not publicly rendered;
- 4-card grid works on desktop/tablet/mobile;
- Agriculture benchmark is not regressed;
- Food Industry route still renders;
- Romanian placeholder routes still render;
- build/lint pass;
- no source artifacts like `grain-processing-local-diff.txt` are committed unless intentionally approved.

Return findings, blockers, validation output, and recommended next safe task.
```

## Do Not Start Yet

- Food Industry editorial/implementation.
- Homepage visual work.
- Product import/migration.
- Romanian runtime/localization implementation.
- SEO runtime/canonical/hreflang/sitemap/robots work.
