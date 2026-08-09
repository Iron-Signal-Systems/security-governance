# Security Risk Register

## Current state

**ISS-RSK-001 status:** `Defined`  
**Register state:** Initial risks identified; first formal assessment pending  
**Prepared:** 2026-08-09

`UNASSESSED` and `PENDING_REVIEW` are deliberate. They indicate that the risk is
known but has not yet completed the initial ISS-RSK-001 assessment.

No risk in this register shall be represented as fully assessed merely because
it has been identified.

## Register

| ID | Risk | Affected boundary / assets | Owner | Likelihood | Impact | Rating | Treatment | Target | Status | Next review |
|---|---|---|---|---|---|---|---|---|---|---|
| ISS-RISK-001 | Loss of sole engineering-authority availability | Engineering Authority; all active engineering repositories | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-002 | Compromise of release-signing authority | Git commit-signing authority; engineering repositories | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-003 | Loss or corruption of source repositories | GitHub organization; active and archived repositories | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-004 | Unauthorized access to customer information | Future or current customer-controlled information boundary where applicable | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-005 | Dependency or build-system compromise | Engineering repositories; build and dependency boundary | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-006 | Security defect in an accepted product release | Product repositories; accepted release boundary | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-007 | Failed customer deployment or upgrade | Future or current deployment boundary where applicable | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-008 | Inability to recover customer-critical service | Future or current customer service and recovery boundary where applicable | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-009 | Compromise of remote-support credentials | Future or current remote-support authority where applicable | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-010 | Critical supplier or service outage | GitHub; Squarespace-managed domain/DNS; Gmail; other material suppliers | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-011 | Unauthorized change or compromise of domain/DNS authority | `ironsignalsystems.com`; Squarespace-managed service boundary | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-012 | Compromise or loss of administrative email access | `info@ironsignalsystems.com`; Gmail service boundary | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-013 | Complete loss of local work or recovery state before remote synchronization | Primary development workstation; `/src` Btrfs/Snapper recovery boundary | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |
| ISS-RISK-014 | Compromise of GitHub organization administrative authority | Iron Signal Systems GitHub organization; GitHub SSH authentication authority | PENDING_REVIEW | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | PENDING_REVIEW | IDENTIFIED | PENDING_REVIEW |

## Assessment rule

During the first formal ISS-RSK-001 review, every currently applicable material
risk shall receive:

- an accountable owner;
- likelihood;
- impact;
- derived rating;
- treatment decision;
- target date where treatment is required;
- status; and
- next review date.

A risk that is identified for a future boundary but is not currently applicable
shall be explicitly recorded as such during the review rather than silently
deleted or given an invented score.

## Register maintenance

New risks shall receive the next stable `ISS-RISK-NNN` identifier.

Identifiers shall not be reused after a risk is closed or becomes
non-applicable.

Historical risk decisions shall remain reconstructable through signed repository
history.
