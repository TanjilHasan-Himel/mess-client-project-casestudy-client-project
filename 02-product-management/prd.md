# Product requirements overview

## Product vision

Provide a single operational workspace for a hostel or mess to understand capacity, manage resident turnover, calculate recurring charges, record collections, and retain usable history.

## Primary users

- **Owner:** oversight, settings, sensitive controls, and financial visibility.
- **Manager/Operator:** resident admission, allocation, billing, collection, receipts, and expenses.
- **Resident/Member:** managed subject of the workflow; no verified self-service experience.

## Core jobs to be done

1. Know which seats are available, occupied, under notice, or unavailable.
2. Place a resident into a seat without losing prior occupancy history.
3. Generate a monthly obligation that includes rent and approved adjustments.
4. Record full or partial collection and show the remaining balance.
5. Produce a receipt and retrieve historical collection information.
6. Complete checkout while considering dues and deposits.
7. Review occupancy and financial status without rebuilding reports manually.

## MVP reconstruction

The first usable product boundary is reconstructed as:

- authentication and dashboard shell;
- room/seat setup;
- resident profile;
- dated allocation and checkout;
- manual monthly billing;
- payment recording and printable receipt;
- basic occupancy and collection reporting.

Expense management, enhanced branding, security/session refinements, richer reporting, and vacancy presentation appear as later iterations in Git history.

## Product principles

- Preserve operational history where practical.
- Prevent obvious duplicate billing and overpayment.
- Keep daily actions accessible to non-technical operators.
- Make financial state visible through totals and status labels.
- Prefer managed infrastructure and browser-native outputs to limit operational overhead.

These principles are reconstructed from requirements and implementation. They were not found as a contemporaneous signed product manifesto.

## Success criteria

No measured success targets were documented. Proposed product measures include monthly billing completion rate, unmatched payment count, allocation conflict count, overdue visibility, receipt retrieval time, and successful backup restoration.
