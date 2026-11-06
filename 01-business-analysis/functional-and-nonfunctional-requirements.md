# Functional and non-functional requirements

## Functional requirements

| ID | Requirement | Status |
| --- | --- | --- |
| FR-01 | Create rooms with one or more seats and monthly rent | VERIFIED in implementation |
| FR-02 | Display and filter seat availability states | VERIFIED in implementation |
| FR-03 | Create resident/member profiles | VERIFIED in implementation |
| FR-04 | Allocate a resident to a seat with a start date | VERIFIED in implementation |
| FR-05 | Record notice and checkout details | VERIFIED in implementation |
| FR-06 | Calculate deposit-versus-dues settlement | VERIFIED in implementation; runtime accuracy UNVERIFIED |
| FR-07 | Generate missing monthly bills without duplication | VERIFIED in implementation |
| FR-08 | Add utility charges and discounts | VERIFIED in implementation |
| FR-09 | Record partial/full payments and payment method | VERIFIED in implementation |
| FR-10 | Produce printable receipts | VERIFIED in implementation; printer compatibility UNVERIFIED |
| FR-11 | Record and summarize operational expenses | VERIFIED in implementation |
| FR-12 | Display occupancy, collection, dues, and channel summaries | VERIFIED in implementation |
| FR-13 | Export yearly matrix and backup spreadsheets | VERIFIED in implementation; downloaded output not inspected |
| FR-14 | Export PDF reports | DOCUMENTED; NOT FOUND in implementation |
| FR-15 | Automatically schedule monthly billing | DOCUMENTED; NOT FOUND as a scheduler |
| FR-16 | Allow formal Manager correction request and Owner approval | DOCUMENTED; NOT VERIFIED |

## Non-functional requirements

| ID | Requirement | Status |
| --- | --- | --- |
| NFR-01 | Responsive web interface | DOCUMENTED; not systematically device-tested |
| NFR-02 | Preserve historical allocation and payment records | Architecture supports it; deletion behavior requires review |
| NFR-03 | Role-based least privilege | Partially implemented; hardening required |
| NFR-04 | Secure session handling | Inactivity controls exist; security certification not performed |
| NFR-05 | Reliable duplicate prevention for monthly bills | Database uniqueness rule exists |
| NFR-06 | Recoverable data export | Export exists; restore procedure not tested |
| NFR-07 | Production build compatibility | VERIFIED on 6 November 2026 |
| NFR-08 | Dependency security maintenance | Current audit has unresolved findings |
| NFR-09 | Performance on slow networks | DOCUMENTED aspiration; no measurements found |
| NFR-10 | Accessibility | UNKNOWN; no audit found |

## Requirement quality notes

Several original statements describe desired technology or completion rather than measurable acceptance conditions. This case study separates capability evidence from quality assurance and avoids converting aspirations into verified outcomes.
