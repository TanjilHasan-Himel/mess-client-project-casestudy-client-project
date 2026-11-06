# Lessons learned

## 1. Historical data changes the domain model

A room-management interface can look simple while the real engineering problem is preserving who occupied what, when, and under which financial records.

## 2. Financial workflows need explicit invariants

Duplicate prevention, outstanding-balance checks, partial status, deposit settlement, and receipt uniqueness should be expressed as database rules and automated tests—not only UI behavior.

## 3. RBAC must be defense in depth

Hiding controls from a Manager is insufficient. Sensitive operations need server authorization and least-privilege database policies.

## 4. Export is not the same as recovery

A downloadable workbook is useful, but operational continuity is only demonstrated after a documented restoration test.

## 5. Completion checklists are not test evidence

Project notes may record “completed” or “tested,” but a recruiter-facing case study should distinguish documentation from reproducible validation.

## 6. Security features can introduce usability defects

The inactivity-control work was followed by a login-loop fix. Security behavior needs scenario testing across refresh, multi-tab, sleep/wake, and re-authentication.

## 7. Public evidence needs its own privacy review

Even an unauthenticated screenshot exposed a property identifier. A safe publication workflow must review text, images, diagrams, filenames, and metadata before release.

## 8. AI assistance should be disclosed accurately

AI-assisted analysis and writing can accelerate evidence organization, but it must not turn inferred rationale into invented history or imply independently hand-written implementation.
