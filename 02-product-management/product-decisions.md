# Product decisions

## Decision 1 — Model seats independently from residents

**Status:** VERIFIED implementation; reconstructed rationale.

The product maintains seat inventory separately and connects a resident through an allocation period. This supports turnover and avoids treating occupancy as a permanent resident attribute.

**Trade-off:** More records and workflow complexity in exchange for historical integrity.

## Decision 2 — Support partial payment as a first-class state

**Status:** VERIFIED implementation and DOCUMENTED requirement.

Bills move among unpaid, partial, and paid states. This reflects collection reality more accurately than a binary paid/unpaid model.

**Trade-off:** Requires careful reconciliation between payment records and bill totals.

## Decision 3 — Provide a manual monthly billing trigger

**Status:** VERIFIED.

A manual generation action provides operational recovery when automatic scheduling is unavailable or fails.

**Trade-off:** Improves recoverability but depends on an operator and needs duplicate protection.

## Decision 4 — Offer both detailed and compact receipt layouts

**Status:** VERIFIED in UI implementation; physical printer validation UNKNOWN.

The product supports browser printing for different operational contexts.

**Trade-off:** Browser/printer differences require real-device testing.

## Decision 5 — Add expense management after core collection flows

**Status:** VERIFIED by Git chronology.

Expense management was introduced after the initial operational modules, extending the product from rent collection toward a broader property view.

## Decision 6 — Remove a dense expense trend visualization

**Status:** VERIFIED by Git chronology; rationale reconstructed.

A later refactor removed the trend graph from the current-month expense card, suggesting a preference for simpler operational presentation.

## Decision 7 — Add, then remove, a rate-limit overlay

**Status:** VERIFIED by commit history; detailed rationale not preserved.

The sequence demonstrates iteration and reversal rather than presenting every security idea as permanent. The final security posture must be assessed from current behavior, not earlier commit messages.
