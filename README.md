# SmartMess — Product, Business Analysis & Engineering Case Study

SmartMess is a private, web-based hostel and mess operations system designed around room and seat inventory, resident turnover, monthly billing, payment collection, receipts, expenses, and operational reporting.

This repository is a sanitized case-study package. It explains the problem, requirements, decisions, architecture, validation status, and limitations without publishing the application source code, credentials, private endpoints, database records, or client data.

> Evidence status: **VERIFIED** means confirmed in implementation, Git history, or a completed local check. **DOCUMENTED** means recorded in project material but not independently validated. **INFERRED** means a clearly labelled reconstruction from available evidence. **PROPOSED** is future work. **UNKNOWN** means evidence is unavailable.

## What this case study demonstrates

- Business analysis: problem framing, stakeholders, workflows, business rules, risks, acceptance criteria, and requirements traceability.
- Product management: scope, prioritization, roadmap reconstruction, and product trade-offs.
- Software engineering: high-level architecture, data integrity approach, implementation milestones, and technical decisions.
- Quality practice: build verification, evidence boundaries, security review, and explicit limitations.

## Evidence summary

| Claim | Status | Basis |
| --- | --- | --- |
| Core operational modules exist | VERIFIED | Static implementation inspection and successful production build |
| TypeScript production build succeeds | VERIFIED | Local Next.js 16.4.3 production build on 6 November 2026 |
| Automated test suite exists | UNKNOWN / NOT FOUND | No unit, integration, or end-to-end test files were found |
| System is deployed and used in production | DOCUMENTED | Historical project notes; no deployment or usage validation was performed for this publication |
| Measured business impact or ROI | UNKNOWN | No defensible measurement evidence was found |

## Case-study map

- [Executive case study](case-study.md)
- [Business analysis](01-business-analysis/problem-and-context.md)
- [Product management](02-product-management/prd.md)
- [Architecture](03-software-engineering/architecture.md)
- [Engineering decisions](03-software-engineering/engineering-decisions.md)
- [Research, trade-offs, and lessons](04-research-and-decisions/research-notes.md)
- [Testing and limitations](testing-and-limitations.md)
- [Screenshot privacy register](screenshots/README.md)
- [Publish-readiness review](publish-review.md)

## Authorship and AI assistance

Product direction, project decisions, implementation work, and repository history are attributed to **Tanjil Hasan Himel** where supported by project evidence. This public package was assembled with AI-assisted repository analysis and technical writing. Reconstructed explanations are not presented as contemporaneous decisions.

The private application remains private. Public access to this repository does not grant a license to reuse its content or the underlying application.
