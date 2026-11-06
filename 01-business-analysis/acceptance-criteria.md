# Acceptance criteria

These criteria convert the available requirements into testable statements. Unless marked verified, they are **PROPOSED acceptance criteria**, not evidence that testing already occurred.

## Seat and allocation

- Given an available seat and resident without an active allocation, when an authorized operator allocates the seat, then a dated allocation is created and the seat is no longer available.
- Given an occupied seat without a valid future handover condition, when another allocation is attempted, then the operation is rejected.
- Given a resident with an active allocation, when a second active allocation is attempted, then the operation is rejected.
- Given a leaving notice, when it is recorded, then the planned date is retained and the seat is visible as leaving soon.

## Billing and payment

- Given an active allocation and a month without a bill, when monthly generation runs, then exactly one bill is created.
- Given an existing bill for the allocation and month, when generation is repeated, then no duplicate bill is created.
- Given earlier unpaid balances, when a later bill is generated, then the carried amount is calculated according to the approved business rule.
- Given an outstanding balance, when a valid partial payment is recorded, then the bill becomes partial and a receipt reference is created.
- Given a payment larger than the outstanding balance, when submitted, then it is rejected.

## Checkout

- Given unpaid bills and a recorded deposit, when checkout is processed with approved deduction, then dues, deduction, and refundable value reconcile.
- Given checkout completion with no next valid allocation, then the seat becomes available.

## Authorization and audit

- A Manager cannot perform an Owner-only operation through the UI, direct server request, or database client.
- Sensitive changes record actor, time, target, and before/after values where legally and operationally appropriate.

These authorization/audit criteria are not currently verified and should block a strong production-security claim.

## Reporting and recovery

- A yearly export reconciles to the source bills and payments for the selected year.
- A backup can be restored into an isolated environment with record counts and financial totals preserved.
- No export or screenshot intended for public use contains real personal, financial, credential, endpoint, or client-identifying data.
