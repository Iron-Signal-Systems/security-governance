# Security Risk Register

## Current state

**ISS-RSK-001 status:** `Implemented`  
**Register state:** Operating  
**Initial review:** 2026-08-09  
**Focused treatment review:** 2026-08-10 — `ISS-RISK-014`
**Focused treatment review:** 2026-08-11 — `ISS-RISK-002`
**Focused treatment review:** 2026-08-11 — `ISS-RISK-015`
**Focused treatment review:** 2026-08-11 — `ISS-RISK-015` remediation reassessment
**Focused treatment review:** 2026-08-11 — `ISS-RISK-005` dependency/build treatment
**Focused treatment review:** 2026-08-11 — `ISS-RISK-001` sole-authority treatment
**Next required review:** 2026-11-09 or earlier upon material change

The current operating boundary has completed its first ISS-RSK-001 assessment.

Risks tied only to future customer, deployment, service, or support boundaries
remain explicitly identified as `FUTURE_BOUNDARY` and `UNASSESSED`. They shall
be assessed when the applicable boundary becomes current.

## Register

| ID | Risk | Applicability | Affected boundary / assets | Owner | Likelihood | Impact | Rating | Treatment | Treatment basis / action | Target | Status | Next review |
|---|---|---|---|---|---:|---:|---|---|---|---|---|---|
| ISS-RISK-001 | Loss of sole engineering-authority availability | CURRENT | Engineering Authority; all active engineering repositories | Governance Authority | 2 | 3 | HIGH (6) | REDUCE | Focused 2026-08-11 treatment review confirmed reconstructable repository and governance state reduces context loss but does not create another authorized human operator. The current solo-project boundary may pause during sole-operator unavailability. ISS-BCP-ACT-004 remains open and shall establish an appropriate continuity or succession path before future obligations require continued operation during operator unavailability. | 2026-11-09 | OPEN | 2026-11-09 |
| ISS-RISK-002 | Compromise of release-signing authority | CURRENT | Git commit-signing authority; engineering repositories | Engineering Authority | 1 | 3 | MEDIUM (3) | REDUCE | Focused 2026-08-11 treatment review confirmed the required signing-authority separation, custody, passphrase, deliberate-use, duplicate-copy review, and verification conditions; a non-secret revocation/replacement/transition procedure is defined. Continue monitoring and separately treat workstation risk. | 2026-11-09 | MONITORING | 2026-11-09 |
| ISS-RISK-003 | Loss or corruption of source repositories | CURRENT | GitHub organization; active and archived repositories; local source boundary | System Owner | 1 | 3 | MEDIUM (3) | REDUCE | Maintain remote Git repository history and local snapshots; evaluate stronger independent backup/recovery requirements under continuity controls. | 2026-11-09 | MONITORING | 2026-11-09 |
| ISS-RISK-004 | Unauthorized access to customer information | FUTURE_BOUNDARY | Future customer-controlled information boundary | Security Authority | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | No current customer-information boundary has been established in this governance baseline; assess before such data is handled. | BOUNDARY_ACTIVATION | IDENTIFIED | 2026-11-09 |
| ISS-RISK-005 | Dependency or build-system compromise | CURRENT | Engineering repositories; build and dependency boundary | Engineering Authority | 1 | 3 | MEDIUM (3) | REDUCE | Focused 2026-08-11 treatment review demonstrated that current dependency/build controls detected a reachable DNP dependency vulnerability, required remediation, preserved governed dependency history, and returned the reviewed DNP boundary to 29 PASS / 0 FAIL with the governed govulncheck v1.6.0 reporting no vulnerabilities. Atlas and File Intelligence remain governed by their exact accepted ISRAS pins; DNP remains explicitly non-adopted pending ISS-ENG-ACT-001. Continue dependency, vulnerability, build-input, and engineering-governance monitoring. | 2026-11-09 | MONITORING | 2026-11-09 |
| ISS-RISK-006 | Security defect in an accepted product release | FUTURE_BOUNDARY | Future accepted product-release boundary | Engineering Authority | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | No accepted customer product-release boundary is established in the current governance state; assess before first such release. | BOUNDARY_ACTIVATION | IDENTIFIED | 2026-11-09 |
| ISS-RISK-007 | Failed customer deployment or upgrade | FUTURE_BOUNDARY | Future customer deployment boundary | System Owner | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | No current customer deployment/upgrade boundary is established; assess before first governed customer deployment. | BOUNDARY_ACTIVATION | IDENTIFIED | 2026-11-09 |
| ISS-RISK-008 | Inability to recover customer-critical service | FUTURE_BOUNDARY | Future customer-critical service and recovery boundary | Governance Authority | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | No customer-critical operated service is currently established in this governance boundary; assess before such service operation. | BOUNDARY_ACTIVATION | IDENTIFIED | 2026-11-09 |
| ISS-RISK-009 | Compromise of remote-support credentials | FUTURE_BOUNDARY | Future remote-support authority | Security Authority | UNASSESSED | UNASSESSED | UNASSESSED | PENDING_REVIEW | No current remote-support authority is established in this governance baseline; assess before remote-support access is introduced. | BOUNDARY_ACTIVATION | IDENTIFIED | 2026-11-09 |
| ISS-RISK-010 | Critical supplier or service outage | CURRENT | GitHub; Squarespace-managed domain/DNS; Gmail; other material suppliers | Governance Authority | 2 | 2 | MEDIUM (4) | REDUCE | Establish supplier review and document recovery/alternative paths for material hosted services. | 2026-11-09 | OPEN | 2026-11-09 |
| ISS-RISK-011 | Unauthorized change or compromise of domain/DNS authority | CURRENT | `ironsignalsystems.com`; Squarespace-managed service boundary | System Owner | 2 | 2 | MEDIUM (4) | REDUCE | Protect administrative access, review account recovery, and include domain/DNS in supplier and access-control reviews. | 2026-11-09 | OPEN | 2026-11-09 |
| ISS-RISK-012 | Compromise or loss of administrative email access | CURRENT | `info@ironsignalsystems.com`; Gmail service boundary | System Owner | 2 | 2 | MEDIUM (4) | REDUCE | Protect mailbox and recovery authority and include the service in supplier and access-control reviews. | 2026-11-09 | OPEN | 2026-11-09 |
| ISS-RISK-013 | Complete loss of local work or recovery state before remote synchronization | CURRENT | Primary development workstation; `/src` Btrfs/Snapper recovery boundary | System Owner | 2 | 2 | MEDIUM (4) | REDUCE | Continue frequent remote synchronization and local snapshots; determine independent backup requirements under continuity/recovery governance. | 2026-11-09 | OPEN | 2026-11-09 |
| ISS-RISK-014 | Compromise of GitHub organization administrative authority | CURRENT | Iron Signal Systems GitHub organization; GitHub SSH authentication authority | Security Authority | 2 | 3 | HIGH (6) | REDUCE | Focused 2026-08-10 treatment review found one or more required conditions incomplete or unknown. Detailed state is protected locally; complete the identified remediation and repeat the focused review. Recovery/revocation procedure is defined. | 2026-11-09 | OPEN | 2026-11-09 |
| ISS-RISK-015 | Compromise of primary development and administrative workstation | CURRENT | Primary ISS development workstation; GitHub authentication; signing authority; local development data | Security Authority | 1 | 3 | MEDIUM (3) | REDUCE | Focused 2026-08-11 remediation reassessment confirmed the two prior deficiencies were addressed: key-only remote administration now verifies and current High workstation advisory candidates have accountable technical dispositions under ISS-VUL-001. Continue monitoring and reevaluate upon material patch, exposure, privilege, authority, or vulnerable-workflow change. | 2026-11-09 | MONITORING | 2026-11-09 |

## Assessment notes

The initial review deliberately uses the higher adjacent level where meaningful
uncertainty exists.

High risks are not accepted. Each High risk has a `REDUCE` treatment plan and a
target date no later than the next quarterly review.

No risk acceptance in this register authorizes deviation from a mandatory
organizational or engineering control.

## Future-boundary candidates

`ISS-RISK-004`, `ISS-RISK-006`, `ISS-RISK-007`, `ISS-RISK-008`, and
`ISS-RISK-009` are retained because they are foreseeable risks for planned
product/customer operations.

They are not assigned invented likelihood or impact scores before the applicable
boundary exists.

## Register maintenance

New risks shall receive the next stable `ISS-RISK-NNN` identifier.

Identifiers shall not be reused after a risk is closed or becomes
non-applicable.

Historical risk decisions shall remain reconstructable through signed repository
history.
