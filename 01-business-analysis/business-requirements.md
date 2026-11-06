# Business Requirements Document (BRD)

## Purpose

Define the business-level capabilities required to manage a single hostel or mess property while preserving operational and financial history.

## Business requirements

| ID | Requirement | Priority | Evidence status |
| --- | --- | --- | --- |
| BR-01 | Maintain room and seat capacity with current availability status | Must | DOCUMENTED and VERIFIED |
| BR-02 | Maintain resident identity and contact records appropriate to admission | Must | DOCUMENTED and VERIFIED |
| BR-03 | Preserve seat occupancy history through dated allocations | Must | DOCUMENTED and VERIFIED |
| BR-04 | Prevent conflicting active allocations for a resident or seat | Must | DOCUMENTED; partially VERIFIED |
| BR-05 | Generate monthly charges and carry outstanding amounts forward | Must | DOCUMENTED and VERIFIED in implementation |
| BR-06 | Support full and partial payments with traceable receipts | Must | DOCUMENTED and VERIFIED in implementation |
| BR-07 | Track security deposit settlement during checkout | Must | DOCUMENTED and VERIFIED in implementation |
| BR-08 | Provide occupancy, collection, dues, expense, and yearly views | Should | DOCUMENTED and VERIFIED in implementation |
| BR-09 | Export operational records for continuity and reporting | Should | DOCUMENTED and VERIFIED for spreadsheet output |
| BR-10 | Separate Owner and Manager permissions | Must | DOCUMENTED; partially VERIFIED |
| BR-11 | Preserve an audit trail for sensitive changes | Should | DOCUMENTED; incomplete or UNKNOWN |
| BR-12 | Operate within the selected managed-service cost constraint | Should | DOCUMENTED; financial feasibility UNKNOWN |

## Business rules

1. A resident should not hold more than one active allocation.
2. A seat should not have overlapping active occupancy periods.
3. A monthly bill should not be duplicated for the same allocation and month.
4. Payment cannot exceed the outstanding amount in the implemented collection flow.
5. A bill transitions among unpaid, partial, and paid according to collected value.
6. Checkout considers unpaid bills and the recorded deposit.
7. Selected destructive or security operations are intended to be Owner-only.

Rules 1–6 have identifiable implementation evidence. Rule 7 is only partially enforced and requires remediation.

## Dependencies

- Managed authentication and relational database service
- Web hosting/runtime compatible with the selected Next.js version
- Browser print and spreadsheet download capabilities
- Accurate operator-entered resident, rent, payment, and expense data
- Appropriate backup, access-control, and retention procedures

## Success measures

No measured baseline or target KPI was found. Proposed future measures include allocation error rate, billing completion time, overdue balance visibility, receipt retrieval time, and successful backup restoration. These are **PROPOSED**, not achieved outcomes.
