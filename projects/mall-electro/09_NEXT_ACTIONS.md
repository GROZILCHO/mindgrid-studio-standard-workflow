# Next Actions - Mall Electro

## Immediate Operational Actions

| Action | Owner | Expected output | PM decision required |
| --- | --- | --- | --- |
| Confirm production deployment of current `main` build | Rosen / MindGrid Studio | Deployment status confirmed | Yes if deployment is not already complete |
| Verify live `/bg/`, `/en/`, and `/ro/` routes | QA / PM Assistant | Live route smoke-test notes | No, unless failures appear |
| Verify live `sitemap.xml` | QA / PM Assistant | Sitemap availability and URL checks | No, unless sitemap is wrong |
| Verify live hreflang and canonicals | SEO/AEO Specialist or QA | Hreflang/canonical check notes | No, unless SEO defects appear |
| Submit or refresh sitemap in Google Search Console | Rosen / MindGrid Studio | Search Console submission status | Yes if access or timing is unclear |
| Perform native Romanian editorial review when available | Native reviewer / Rosen | Editorial notes or approval | Yes if corrections are needed |

## Future Improvement Actions

| Action | Owner | Expected output | PM decision required |
| --- | --- | --- | --- |
| Evaluate bundle splitting | Codex / Performance QA | Controlled performance audit and task recommendation | Yes before implementation |
| Update Browserslist data in a controlled maintenance task | Codex | Maintenance task with validation | Yes |
| Monitor indexing and multilingual search performance | SEO/AEO Specialist | Search Console observations | No, unless issues appear |
| Define EN/RO legal-page strategy if required | Rosen / MindGrid Studio / SEO | Decision on legal routes by language | Yes |

## Not Release Blockers By Default

- Stale Browserslist data warning.
- Large main bundle warning.
- Native Romanian editorial review, unless Rosen / MindGrid Studio decides it blocks launch.

## Next Milestone

- Milestone: production deployment and live multilingual verification.
- Exit criteria: live `/bg/`, `/en/`, `/ro/`, sitemap, canonicals, hreflang, and Search Console status are confirmed or issues are logged.

