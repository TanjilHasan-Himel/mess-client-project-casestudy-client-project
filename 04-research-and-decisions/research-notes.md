# Research and discovery notes

## Evidence sources used

- Existing product requirements and progress documentation
- Historical project/chat log
- Current source structure and domain migrations
- Git commit history
- Dependency manifest and local production build
- Local unauthenticated interface inspection

## Sources not available

- Formal stakeholder interviews
- Market or competitor research
- Analytics or support-ticket exports
- Production monitoring and incident history
- Financial model or cost report
- Signed acceptance-test results
- Customer testimonial or satisfaction survey

## Discovery themes

### Turnover is the central modeling challenge

The requirement set repeatedly connects a physical seat with changing residents and historical bills. This makes temporal allocation—not just CRUD—the strongest domain theme.

### Financial state needs progressive status

Partial payments, arrears, deposit settlement, and receipts require more than a paid/unpaid checkbox. The implementation reflects this through bill state and separate payment records.

### Operational recovery matters

Manual bill generation, spreadsheet export, and offline-style backup indicate concern for continuity when automation or cloud access is imperfect. Backup restoration, however, remains unverified.

### Documentation drift is material

The repository includes stale version references and completion claims that exceed current verification evidence. Public claims therefore require evidence classification and dates.

## Research conclusion

The repository is strong evidence of implementation breadth and iterative problem solving. It is not evidence of market validation, measured business impact, or complete security assurance. Those boundaries are deliberately visible throughout this case study.
