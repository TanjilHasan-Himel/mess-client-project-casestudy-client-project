# Feasibility and risk analysis

## Feasibility

### Technical feasibility

**Supported with evidence.** The selected web stack can represent the required entities and workflows, and the current repository completes a production build. Managed authentication, relational storage, and client-side reporting reduce the need for a separate custom backend service.

Limitations include unresolved dependency findings, partial authorization enforcement, absence of automated tests, and an upcoming framework convention migration.

### Operational feasibility

**INFERRED.** A browser-based operator interface and printable/exportable outputs fit a property office workflow. No observed usability study, training record, support history, or backup-restore drill was found.

### Financial feasibility

**UNKNOWN.** Project material records a free-tier preference, but no current vendor quota review, cost forecast, growth model, support cost, or ROI calculation was found. “Free-tier” is therefore treated as a constraint/intent, not a guaranteed long-term cost.

## Risk register

| ID | Risk | Likelihood | Impact | Current response / recommendation | Status |
| --- | --- | --- | --- | --- | --- |
| R-01 | Authorization does not consistently enforce Owner/Manager boundaries | Medium | High | Apply least privilege in database policies and sensitive server operations | VERIFIED concern |
| R-02 | Dependency vulnerabilities remain unresolved | High | High | Review direct/transitive dependencies, replace or upgrade where safe, retest | VERIFIED concern |
| R-03 | Financial updates span multiple operations without verified transactions | Medium | High | Add transactional or database-function boundaries and tests | INFERRED from implementation |
| R-04 | No automated regression suite | High | High | Prioritize billing, payment, turnover, and authorization tests | VERIFIED concern |
| R-05 | Spreadsheet backup cannot be proven restorable | Medium | High | Define and test restoration procedure | VERIFIED gap |
| R-06 | Personal and financial data could appear in screenshots or exports | High | High | Use demo data, masking, metadata checks, and human approval | VERIFIED publication risk |
| R-07 | Client-side random receipt suffix could collide under scale | Low/Medium | Medium | Use database-generated sequence or retry on uniqueness failure | INFERRED |
| R-08 | Free-tier limits may change or be exceeded | Medium | Medium | Monitor quotas and define paid-tier thresholds | UNKNOWN |
| R-09 | Documentation and implementation drift | High | Medium | Add evidence review and version/date labels | VERIFIED concern |
| R-10 | Framework convention becomes unsupported | Medium | Medium | Migrate deprecated middleware convention after regression testing | VERIFIED warning |

Likelihood labels are qualitative and reconstructed; no historical incident dataset was available.
