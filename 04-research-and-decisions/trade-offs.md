# Trade-offs and alternatives

## Relational allocation history vs direct seat ownership

- **Chosen:** Separate allocation history.
- **Benefit:** Preserves turnover context.
- **Cost:** More joins, state transitions, and concurrency risk.
- **Alternative:** Store current resident directly on a seat; simpler but weak for history.

## Managed platform vs custom backend infrastructure

- **Chosen:** Managed authentication and PostgreSQL service.
- **Benefit:** Faster delivery and fewer infrastructure components.
- **Cost:** Vendor policy complexity, quotas, and service dependency.
- **Alternative:** Self-hosted API/database; more control and more operational burden.

## Manual billing trigger vs scheduler-only billing

- **Chosen current capability:** Manual trigger with duplicate protection.
- **Benefit:** Operator-controlled recovery and easier troubleshooting.
- **Cost:** Human dependency and possible delayed billing.
- **Alternative:** Scheduler-only; lower manual work but needs monitoring and failure recovery.

## Client-side spreadsheet export vs server-generated reports

- **Chosen:** Browser-side spreadsheet generation.
- **Benefit:** Direct download and limited server report infrastructure.
- **Cost:** Browser resource usage, data exposure in exports, dependency risk.
- **Alternative:** Server-side report jobs with controlled storage and access.

## Rapid feature breadth vs automated verification

- **Observed outcome:** Broad workflow delivery with no repository-owned automated test suite.
- **Benefit:** Fast functional coverage.
- **Cost:** Higher regression and correctness risk, especially around money and access control.

## Automatic publication vs approval-gated case-study publishing

- **Chosen for this repository:** Human approval before public push.
- **Benefit:** Prevents client identifiers, private architecture, stale claims, or secrets from being published automatically.
- **Cost:** Adds a review step.
- **Rejected:** Blind synchronization of private documentation on every push.
