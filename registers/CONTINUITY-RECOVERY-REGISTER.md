# Continuity and Recovery Register

## Current state

**ISS-BCP-001 status:** `Implemented`
**Register state:** Operating
**Initial exercise:** 2026-08-09
**Exercise result:** `PASS_WITH_OPEN_RECOVERY_ACTIONS`
**Focused completion review:** 2026-08-11 — `PASS`
**Next required exercise:** 2027-08-09 or earlier after material recovery-boundary change

The current register reflects the solo-project development and administrative
boundary and does not assert a customer-production recovery boundary.

## Recovery boundary

| Recovery ID | Boundary / asset | Classification | Current recovery source / method | Validation state | Limitation / governance disposition |
|---|---|---|---|---|---|
| ISS-BCP-REC-001 | GitHub-hosted source/governance/engineering repositories | REMOTE_RECONSTRUCTABLE | Canonical pushed Git history on GitHub | PARTIALLY_VALIDATED | `security-governance/dev` was reconstructed in the initial technical exercise. Other repositories were not individually restored. GitHub availability and administrative-account recovery are separate dependencies. |
| ISS-BCP-REC-002 | Primary development/admin workstation (`ISS-ASSET-009`) | REBUILD_REQUIRED | Replacement system plus reconstruction of required repositories, tools, configuration, and authorities | MINIMUM_REBUILD_PATH_VALIDATED | Minimum non-secret replacement-style reconstruction confirmed; no private-credential or full-disaster-recovery claim. |
| ISS-BCP-REC-003 | `/src` Btrfs/Snapper boundary (`ISS-ASSET-015`) | LOCAL_RECOVERY_ONLY | Local Btrfs RAID1 / Snapper point-in-time recovery | RECORDED_NOT_COMPLETE_HOST_VALIDATED | Same local failure domain; explicitly not an independent off-host backup against complete host/storage loss. |
| ISS-BCP-REC-004 | Local Atlas development PostgreSQL (`ISS-ASSET-012`) | REMOTE_RECONSTRUCTABLE | Current reviewed development-database recovery decision | RECONSTRUCTION_DECISION_COMPLETE | Current development DB contents are not authoritative persistent state; governed source/migrations and applicable development inputs are the recovery basis. |
| ISS-BCP-REC-005 | GitHub SSH authentication authority (`ISS-ASSET-010`) | REPLACEMENT_REQUIRED | Provider account control plus governed replacement/reauthorization | PROCEDURE_DEFINED_NOT_EXERCISED | Non-secret replacement/revocation procedure defined 2026-08-10. Private-key backup/recovery is not asserted and actual replacement/recovery was not exercised. |
| ISS-BCP-REC-006 | Git signing authority (`ISS-ASSET-011`) | REPLACEMENT_REQUIRED | Governed replacement/signing-authority transition where loss occurs | PROCEDURE_DEFINED_NOT_EXERCISED | Non-secret replacement/transition procedure defined 2026-08-11. No private signing-secret backup is asserted and actual replacement/transition was not exercised. Loss/compromise may trigger ISS-IR-001 and ISS-ENG-001. |
| ISS-BCP-REC-007 | Domain/DNS (`ISS-ASSET-013`) | PROVIDER_MANAGED | Squarespace service/account recovery | NOT_VALIDATED | Provider resilience is not represented as ISS-controlled recovery. |
| ISS-BCP-REC-008 | Administrative Gmail (`ISS-ASSET-014`) | PROVIDER_MANAGED | Google/Gmail provider/account recovery | NOT_VALIDATED | Provider resilience is not represented as ISS-controlled recovery. |
| ISS-BCP-REC-009 | Sole-operator availability | CURRENT_BOUNDARY_PAUSE_ALLOWED | Reconstructable records reduce context loss; no alternate internal operator exists | CURRENT_DECISION_COMPLETE | Current project work may pause during operator unavailability; future obligations requiring continuation trigger a new continuity/succession review. |

## Open recovery actions

| Action ID | Condition | Required treatment | Owner | Target / trigger | Status |
|---|---|---|---|---|---|
| ISS-BCP-ACT-001 | Local-only state may be lost with complete workstation/storage loss. | Current review identified no additional required non-secret local-only survival state; continue remote synchronization and do not represent unpushed work or local snapshots as off-host recovery. | System Owner | 2026-11-09 | COMPLETE |
| ISS-BCP-ACT-002 | Atlas development PostgreSQL persistence requirement is reviewed. | Current state is reproducible; reconstruct from governed source/migrations and applicable development inputs. | System Owner | 2026-11-09 | COMPLETE |
| ISS-BCP-ACT-003 | Replacement-workstation recovery requires a minimum non-secret rebuild path. | Maintain `procedures/MINIMUM-DEVELOPMENT-WORKSTATION-REBUILD.md` and repeat after material recovery-boundary change; do not represent it as private-credential recovery unless separately exercised. | System Owner | 2026-11-09 | COMPLETE |
| ISS-BCP-ACT-004 | No alternate internal operator exists. | Current-boundary decision is that project work may pause during sole-operator unavailability. Before future obligations require continuation, perform a new continuity/succession review appropriate to the actual organizational/legal state. | Governance Authority | MATERIAL_BOUNDARY_CHANGE | COMPLETE |
| ISS-BCP-ACT-005 | Provider recovery/alternate paths for GitHub, Squarespace, and Gmail require review. | Current provider recovery/strong-authentication review is complete; reevaluate after material provider/account change. | Governance Authority | 2026-11-09 | COMPLETE |

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
