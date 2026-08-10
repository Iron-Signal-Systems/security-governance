# Continuity and Recovery Register

## Current state

**ISS-BCP-001 status:** `Implemented`
**Register state:** Operating
**Initial exercise:** 2026-08-09
**Exercise result:** `PASS_WITH_OPEN_RECOVERY_ACTIONS`
**Next required exercise:** 2027-08-09 or earlier after material recovery-boundary change

The current register reflects the solo-project development and administrative
boundary and does not assert a customer-production recovery boundary.

## Recovery boundary

| Recovery ID | Boundary / asset | Classification | Current recovery source / method | Validation state | Limitation / governance disposition |
|---|---|---|---|---|---|
| ISS-BCP-REC-001 | GitHub-hosted source/governance/engineering repositories | REMOTE_RECONSTRUCTABLE | Canonical pushed Git history on GitHub | PARTIALLY_VALIDATED | `security-governance/dev` was reconstructed in the initial technical exercise. Other repositories were not individually restored. GitHub availability and administrative-account recovery are separate dependencies. |
| ISS-BCP-REC-002 | Primary development/admin workstation (`ISS-ASSET-009`) | REBUILD_REQUIRED | Replacement system plus reconstruction of required repositories, tools, configuration, and authorities | NOT_FULLY_VALIDATED | No complete replacement-workstation rebuild has been performed under ISS-BCP-001. |
| ISS-BCP-REC-003 | `/src` Btrfs/Snapper boundary (`ISS-ASSET-015`) | LOCAL_RECOVERY_ONLY | Local Btrfs RAID1 / Snapper point-in-time recovery | RECORDED_NOT_COMPLETE_HOST_VALIDATED | Same local failure domain; explicitly not an independent off-host backup against complete host/storage loss. |
| ISS-BCP-REC-004 | Local Atlas development PostgreSQL (`ISS-ASSET-012`) | REQUIREMENT_REVIEW_REQUIRED | Required persistence outcome not yet established | NOT_VALIDATED | Development-only boundary; determine whether state is reproducible or requires backup/restore. |
| ISS-BCP-REC-005 | GitHub SSH authentication authority (`ISS-ASSET-010`) | REPLACEMENT_REQUIRED | Provider account control plus governed replacement/reauthorization | NOT_VALIDATED | Private-key backup/recovery is not asserted. |
| ISS-BCP-REC-006 | Git signing authority (`ISS-ASSET-011`) | REPLACEMENT_REQUIRED | Governed replacement/signing-authority transition where loss occurs | NOT_VALIDATED | No private signing-secret backup is asserted. Loss/compromise may trigger ISS-IR-001 and ISS-ENG-001. |
| ISS-BCP-REC-007 | Domain/DNS (`ISS-ASSET-013`) | PROVIDER_MANAGED | Squarespace service/account recovery | NOT_VALIDATED | Provider resilience is not represented as ISS-controlled recovery. |
| ISS-BCP-REC-008 | Administrative Gmail (`ISS-ASSET-014`) | PROVIDER_MANAGED | Google/Gmail provider/account recovery | NOT_VALIDATED | Provider resilience is not represented as ISS-controlled recovery. |
| ISS-BCP-REC-009 | Sole-operator availability | REQUIREMENT_REVIEW_REQUIRED | Reconstructable records reduce context loss; no alternate internal operator exists | OPEN_LIMITATION | Current project work may pause. Establish an appropriate continuity path before future obligations require continuation during operator unavailability. |

## Open recovery actions

| Action ID | Condition | Required treatment | Owner | Target / trigger | Status |
|---|---|---|---|---|---|
| ISS-BCP-ACT-001 | Local-only state may be lost with complete workstation/storage loss. | Identify which local-only state must survive complete host loss and establish an appropriate independent off-host recovery mechanism for that state. Do not back up secrets indiscriminately. | System Owner | 2026-11-09 | OPEN |
| ISS-BCP-ACT-002 | Atlas development PostgreSQL persistence requirement is undefined. | Decide whether the current database state is reproducible or requires backup. If persistence is required, implement and exercise backup/restore appropriate to the development boundary. | System Owner | 2026-11-09 | OPEN |
| ISS-BCP-ACT-003 | Replacement-workstation recovery is not fully validated. | Document the minimum non-secret rebuild/reconstruction path and perform an appropriate replacement/rebuild exercise without representing it as credential recovery unless actually tested. | System Owner | 2026-11-09 | OPEN |
| ISS-BCP-ACT-004 | No alternate internal operator exists. | Establish a continuity decision and protected recovery/succession mechanism appropriate to actual future obligations. Do not invent a successor or alternate authority. | Governance Authority | 2026-11-09 or before obligations require continuity | OPEN |
| ISS-BCP-ACT-005 | Provider recovery/alternate paths for GitHub, Squarespace, and Gmail are not validated by ISS. | Review provider recovery dependencies and practical alternate/recovery paths with ISS-SUP-001 and applicable access controls. | Governance Authority | 2026-11-09 | OPEN |

## Risk relationship

This register directly informs `ISS-RISK-001`, `ISS-RISK-003`,
`ISS-RISK-010`, and `ISS-RISK-013`.

ISS-BCP-001 implementation does not automatically close or lower those risks.

Risk status remains authoritative under `ISS-RSK-001`.

`ISS-RISK-008` remains a `FUTURE_BOUNDARY` risk. Before a customer-critical
service exists, its actual RTO/RPO, backup, restoration, ownership, and recovery
exercise requirements shall be defined.

## Maintenance

New recovery boundaries use the next stable `ISS-BCP-REC-NNN`.

New recovery actions use the next stable `ISS-BCP-ACT-NNN`.

Identifiers shall not be reused.
