# Engineering decisions

## ADR-001 — Use a relational history model for turnover

**Decision:** Represent occupancy through allocation records rather than a permanent resident-to-seat field.

**Evidence:** VERIFIED in schema and application workflow.

**Rationale:** Reconstructed from requirements. It preserves time context when the same seat changes occupants.

**Consequences:** Better traceability; more complex checkout, reporting, and conflict prevention.

## ADR-002 — Enforce monthly bill uniqueness in storage

**Decision:** Prevent more than one bill for the same allocation and billing month.

**Evidence:** VERIFIED database constraint and application pre-check.

**Consequences:** Safer retry behavior; generation still needs error reporting and concurrency tests.

## ADR-003 — Use server operations for mutations

**Decision:** Perform primary mutations on the server side and refresh affected views afterward.

**Evidence:** VERIFIED implementation pattern.

**Consequences:** Centralizes ordinary workflows, but every sensitive operation must perform its own authorization and input validation.

## ADR-004 — Generate spreadsheets in the browser

**Decision:** Build yearly reports and backups client-side.

**Evidence:** VERIFIED implementation.

**Rationale:** Reconstructed. It reduces backend report infrastructure and provides direct download.

**Consequences:** Large datasets may stress the browser; exported personal/financial data requires strict handling; the current spreadsheet dependency has unresolved advisories.

## ADR-005 — Use managed authentication and PostgreSQL services

**Decision:** Adopt managed identity and relational persistence.

**Evidence:** VERIFIED stack; cost rationale DOCUMENTED.

**Consequences:** Faster delivery and less custom infrastructure; introduces vendor dependency, quota considerations, and policy-configuration responsibility.

## ADR-006 — Add inactivity session handling

**Decision:** Add client/session inactivity controls and repair a subsequent login redirect loop.

**Evidence:** VERIFIED by current implementation and commit history.

**Consequences:** Improves shared-device hygiene; requires careful multi-tab, sleep/wake, and session-expiry testing.

## ADR-007 — Upgrade framework after a security concern

**Decision:** Move to Next.js 16.4.3.

**Evidence:** VERIFIED by dependency manifest, build output, and commit history.

**Consequences:** Addresses the recorded concern but introduces a middleware convention deprecation that should be migrated and retested.
