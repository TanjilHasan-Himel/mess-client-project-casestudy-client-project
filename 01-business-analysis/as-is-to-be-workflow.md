# As-Is and To-Be workflows

## Evidence note

No formal observation of the previous operating process was found. The As-Is flows below are **INFERRED** from the documented requirements and should be validated with the property owner and manager.

## 1. Resident admission and seat allocation

### As-Is — reconstructed

```mermaid
flowchart LR
    A[Collect resident details] --> B[Check room availability]
    B --> C[Assign a seat]
    C --> D[Record deposit and start date]
    D --> E[Maintain separate register or sheet]
```

Risks inferred from the requirement set include duplicate allocation, inconsistent identifiers, and loss of history when a seat changes residents.

### To-Be — implemented workflow

```mermaid
flowchart LR
    A[Create resident profile] --> B[Choose available seat]
    B --> C[Validate active allocation]
    C --> D[Create dated allocation]
    D --> E[Update seat status]
    E --> F[Create initial bill where applicable]
```

Status: **VERIFIED in implementation structure; runtime workflow not end-to-end tested for this publication.**

## 2. Monthly billing and collection

### As-Is — reconstructed

```mermaid
flowchart LR
    A[Calculate monthly rent] --> B[Add utilities]
    B --> C[Find previous dues]
    C --> D[Collect full or partial payment]
    D --> E[Write receipt and update ledger]
```

### To-Be — implemented workflow

```mermaid
flowchart LR
    A[Select billing month] --> B[Find active allocations]
    B --> C[Skip existing bills]
    C --> D[Add rent and previous due]
    D --> E[Record payment]
    E --> F[Update paid/partial/unpaid state]
    F --> G[Produce printable receipt]
```

Manual bill generation is **VERIFIED**. Automatic scheduling is **DOCUMENTED but UNVERIFIED**.

## 3. Notice, checkout, and deposit settlement

### To-Be — implemented workflow

```mermaid
flowchart LR
    A[Record leaving notice] --> B[Mark seat leaving soon]
    B --> C[Review unpaid bills]
    C --> D[Compare dues with deposit]
    D --> E[Record settlement]
    E --> F[Close allocation]
    F --> G[Release seat if no next allocation]
```

The calculation path exists in implementation. Accounting correctness and exception handling have not been dynamically validated.

## Proposed improvements

- Validate the reconstructed As-Is workflows with real operators.
- Add transactional guarantees around multi-step financial and allocation updates.
- Introduce a formal correction/void approval workflow.
- Create an anonymized training/demo environment for repeatable acceptance tests.
