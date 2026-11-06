# Stakeholder analysis

## Evidence-backed stakeholders

| Stakeholder or role | Need | Influence | Evidence status |
| --- | --- | --- | --- |
| Property Owner | Operational visibility, sensitive settings, financial oversight, selected destructive controls | High | DOCUMENTED; partially VERIFIED |
| Manager / Operator | Fast daily enrollment, allocation, collection, receipt, and expense workflows | High | DOCUMENTED and VERIFIED as an application role |
| Resident / Student / Member | Correct profile, seat, bill, payment, deposit, and checkout records | Medium | DOCUMENTED as a managed business subject |
| Project engineer | Deliver, troubleshoot, maintain, and hand over the system | High during delivery | VERIFIED by Git authorship and project history |

## Assumed or unconfirmed stakeholders

| Stakeholder | Why it may matter | Status |
| --- | --- | --- |
| Accountant or external auditor | Could consume collection and expense exports | INFERRED; no role or interview evidence |
| Prospective resident | Could be affected by vacancy information | INFERRED |
| Hosting/database providers | Operational dependency | VERIFIED as technical dependencies, not business stakeholders |

## Role boundaries

The documented model assigns broad control to the Owner and day-to-day operations to the Manager. Residents do not have a verified authenticated workflow.

Static review indicates that some sensitive Owner checks exist, especially around settings and expense deletion, while other core data policies are broader. Therefore the role model is treated as an intended control requiring further hardening, not a fully validated authorization guarantee.

## Missing discovery evidence

No interview transcript, signed requirements workshop, persona study, market survey, or customer feedback dataset was found. This package does not invent any of them.
