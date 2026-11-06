# Testing, validation, and limitations

## Completed checks

| Check | Result | Classification |
| --- | --- | --- |
| Repository and dependency inventory | Completed | VERIFIED |
| Git chronology inspection | 27 commits, 9–29 October 2026 | VERIFIED |
| Production build | Passed with Next.js 16.4.3 | VERIFIED |
| TypeScript validation during build | Passed | VERIFIED |
| Route generation | Completed for login and operational dashboard routes | VERIFIED |
| Dependency vulnerability audit | Completed; unresolved findings reported | VERIFIED |
| Screenshot privacy inspection | Property identifier found; image withheld | VERIFIED |

The build emitted a framework deprecation warning for the legacy middleware file convention. This does not make the build fail, but it is a maintenance item.

## Checks not passed or not completed

- A full lint command was attempted twice but did not complete within the observation window and produced no diagnostic output. It is **INCONCLUSIVE**, not passed.
- No repository-owned unit, integration, or end-to-end test suite was found.
- No authenticated workflow was executed against an isolated demo database.
- No production deployment, uptime, performance, accessibility, browser compatibility, backup restoration, or disaster recovery test was independently validated.
- No payment reconciliation, concurrent allocation, or month-boundary scenario was dynamically tested for this publication.

## Security and dependency posture

The production dependency audit reported 21 findings: 10 high, 10 moderate, and 1 low. Several are transitive; at least one direct spreadsheet dependency has advisories without an automated fix in the installed line. The private security report records the actionable details. This public repository does not claim production security certification.

Static review also found that the documented Owner/Manager authorization model is not uniformly enforced at every layer. A future remediation should apply least privilege in database policies and repeat authorization checks in sensitive server operations.

## Product limitations

- Automatic scheduled monthly billing is documented but not verified as implemented; a manual generation flow exists.
- Excel export is implemented; documented PDF export was not found.
- Resident self-service, formal correction approval, and complete audit workflows were not verified.
- Measured business outcomes, customer research, and usability results are unavailable.
- Current screenshots cannot be published safely without an anonymized demo dataset.

## Evidence boundary

Code presence proves that a path was implemented, not that it works correctly in every environment. Historical notes and completion checklists are treated as documentation, not independent validation. No confidential record or credential was used as public evidence.
