# Requirements traceability matrix

| Business objective | Requirement | Implemented capability | Test/evidence | Status |
| --- | --- | --- | --- | --- |
| View capacity | BR-01 / FR-01–02 | Room/seat creation and status views | Static implementation + successful build | VERIFIED implementation |
| Preserve turnover | BR-03 / FR-04–05 | Dated allocation, notice, checkout | Static implementation + schema history model | VERIFIED implementation; runtime UNVERIFIED |
| Avoid allocation conflict | BR-04 | Active allocation checks | Static business-logic inspection | PARTIALLY VERIFIED |
| Generate recurring charges | BR-05 / FR-07–08 | Manual monthly generation, carry-forward, charges | Static implementation + uniqueness rule | VERIFIED implementation; calculation tests absent |
| Record collection | BR-06 / FR-09–10 | Partial/full payment state and receipt | Static implementation | VERIFIED implementation; runtime UNVERIFIED |
| Settle checkout | BR-07 / FR-06 | Deposit and due comparison | Static implementation | VERIFIED implementation; accounting tests absent |
| Provide management visibility | BR-08 / FR-11–12 | Dashboard, expense, dues, channel summaries | Static implementation + build | VERIFIED implementation |
| Export records | BR-09 / FR-13 | Spreadsheet matrix and backup | Static implementation | VERIFIED implementation; restore UNKNOWN |
| Separate duties | BR-10 / NFR-03 | Owner/Manager model and selected checks | Static authorization review | PARTIAL; remediation required |
| Preserve audit trail | BR-11 | Payment collector and timestamps in parts | Static review | INCOMPLETE / UNKNOWN |
| Control operating cost | BR-12 | Managed-service architecture | Historical documentation | DOCUMENTED only |
| Automate monthly billing | FR-15 | Manual fallback exists; scheduler not found | Repository search | NOT VERIFIED |
| Provide PDF export | FR-14 | Spreadsheet export found | Repository search | NOT IMPLEMENTED/UNKNOWN |

This matrix links public claims to evidence categories without exposing private file paths or source code. Exact references are retained in a separate private evidence index.
