# Engineering validation report

## Static inspection

Reviewed application routes, server operations, domain migrations, dependency manifest, documentation, and Git history. Static inspection verified the presence of core domain workflows but was not treated as proof of runtime correctness.

## Build verification

Command: production build using the repository-defined build script.

Result on 6 November 2026:

- Next.js 16.4.3 recognized.
- Application compiled successfully.
- TypeScript validation completed successfully.
- Static/dynamic route generation completed.
- Exit status: success.
- Warning: legacy middleware convention is deprecated in this framework version.

## Lint verification

The repository lint command and a source-targeted lint command were attempted. Both remained active without producing diagnostics during the observation window and were stopped. Result: **INCONCLUSIVE**.

## Automated tests

No unit, integration, browser, or end-to-end test files were found. No coverage figure is claimed.

## Dependency review

The production dependency audit returned 21 findings: 10 high, 10 moderate, and 1 low. Some are transitive, and some do not have an automated fix in the installed dependency line. No dependency was changed as part of this documentation task.

## Runtime evidence

A local production server was started only to inspect the unauthenticated login interface. No real account was used and no live business record was opened. Captured screenshots contained a property identifier and were rejected from public output.

## Priority test plan

1. Authorization matrix for Owner versus Manager at UI, server, and database boundaries.
2. Duplicate and concurrent allocation attempts.
3. Monthly bill retries and month-boundary behavior.
4. Previous-due calculation and prevention of double counting.
5. Partial/full/overpayment and receipt collision behavior.
6. Deposit settlement and checkout failure recovery.
7. Spreadsheet formula/data safety and backup restoration.
