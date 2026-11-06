# Roadmap and delivery chronology

## Delivered chronology reconstructed from Git

| Date | Milestone | Evidence status |
| --- | --- | --- |
| 9 Oct 2026 | Foundation and broad operational feature set | VERIFIED by commits; quality level not implied |
| 9–10 Oct | Profile expansion, reporting, billing fixes, print and RBAC refinements | VERIFIED by commits |
| 11–12 Oct | Login redesign, expense management, deletion behavior changes | VERIFIED by commits |
| 13 Oct | Vacancy/notice ticker and branding refinement | VERIFIED by commits |
| 19 Oct | Inactivity logout, login-loop fix, requirements documentation | VERIFIED by commits |
| 20 Oct | Temporary security overlay and login clock changes | VERIFIED by commits |
| 29 Oct | Overlay removal and Next.js security upgrade | VERIFIED by commits |

Commit history records what changed; it does not prove stakeholder acceptance or production usage.

## Recommended next roadmap

### P0 — Security and correctness

- Harden Owner/Manager authorization at database and server boundaries.
- Review and remediate dependency advisories, including spreadsheet export risk.
- Add transactional safeguards to financial and allocation workflows.
- Add automated tests for billing, partial payments, checkout, and concurrent allocation.

### P1 — Verification and operability

- Build a sanitized demo environment and repeatable seed dataset.
- Test backup restoration, not only export.
- Complete accessibility and responsive-device review.
- Replace the deprecated framework middleware convention after regression testing.

### P2 — Product validation

- Interview actual operators and validate reconstructed workflows.
- Define measurable operational KPIs.
- Decide whether scheduled billing, PDF output, and formal correction approval remain required.

All roadmap items above are **PROPOSED** and are not represented as commitments.
