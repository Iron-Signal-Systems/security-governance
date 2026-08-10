# ISS-BCP-EX-001 — Initial Continuity and Recovery Exercise

## Exercise identity

**Control:** ISS-BCP-001
**Exercise ID:** ISS-BCP-EX-001
**Exercise date:** 2026-08-09
**Exercise authority:** Sole project operator acting as Governance Authority / System Owner
**Exercise type:** Combined technical recovery check + tabletop
**Independence status:** Self-review; not independent
**Definition commit:** `3bf87ad234f906f84cfa78e56446561c30ce7508`
**Reviewed asset-register SHA-256:** `8d5104b5987c6afce481ac7b3572805bd37f193175c8cd0e6467a1156633099b`
**Reviewed risk-register SHA-256:** `44552e69b7402c6a66b5d3a657f297423e54783589a62e1fdcff981ac00d2b4e`
**Technical test UTC:** `2026-08-10T00:25:41Z`
**Recovered remote:** `https://github.com/Iron-Signal-Systems/security-governance.git`
**Recovered branch:** `dev`
**Recovered commit:** `6fcd290adf0ee406af67bcfecd874e296ad6e221`
**Git object validation:** `PASS`
**Exercise result:** `PASS_WITH_OPEN_RECOVERY_ACTIONS`
**Next required exercise:** 2027-08-09 or earlier after material recovery-boundary change

## Scenario

Assume the primary development/admin workstation and all storage local to that
workstation become unavailable.

Assume the `/src` Btrfs/Snapper recovery boundary is unavailable with the lost
host/storage.

Assume GitHub remains reachable from a replacement environment.

No real workstation or storage loss is asserted.

## Technical action actually executed

The exercise performed a read-only reconstruction of the canonical
`security-governance` `dev` branch into a newly created temporary directory
outside the active working repository.

The recovered repository was required to resolve to the exact expected pre-BCP
`dev` commit:

`6fcd290adf0ee406af67bcfecd874e296ad6e221`

Observed recovered commit:

`6fcd290adf0ee406af67bcfecd874e296ad6e221`

The recovered repository then completed:

`git fsck --full --no-reflogs`

successfully.

The temporary recovery directory was deleted after validation.

This demonstrates that the tested pushed `security-governance/dev` Git history
could be reconstructed from the remote source at exercise time.

## What the technical test does not prove

The technical test does not prove recovery of every ISS repository, GitHub outage
recovery, GitHub administrative recovery, unpushed work, complete-host local
snapshot recovery, Atlas PostgreSQL restoration, full workstation
reconstruction, SSH/signing authority recovery, Squarespace/Gmail recovery,
alternate-operator availability, or customer-production disaster recovery.

## Current recovery analysis

Pushed Git history has an off-host reconstruction source on GitHub, but this does
not make GitHub an independent backup of every ISS state.

The asset register records `/src` Btrfs RAID1 with Snapper as local point-in-time
recovery and explicitly states it is not independent off-host backup against
complete host/storage loss.

The Atlas PostgreSQL service is development-only; this exercise does not establish
that its contents must survive host loss and does not claim a restore capability.

The exercise does not copy or restore private authentication/signing keys. A real
loss may require provider recovery, replacement authority, and governed
transition.

Squarespace and Gmail remain provider-hosted dependencies whose administrative
recovery paths were not exercised.

Repository reconstruction preserves project history but does not create a second
authorized person. Current project work may pause if the sole operator is
unavailable.

## Related risks

The exercise addresses the decision path for `ISS-RISK-001`, `ISS-RISK-003`,
`ISS-RISK-010`, and `ISS-RISK-013`.

It does not close or reduce those risks by itself.

`ISS-RISK-008` remains future-boundary and is not assigned invented
customer-production recovery objectives.

## Result

`PASS_WITH_OPEN_RECOVERY_ACTIONS`

The control distinguished what can currently be reconstructed, what is
local-only, what depends on provider recovery, what requires replacement, and
what remains undefined.

One real technical Git reconstruction check passed.

Complete workstation recovery, independent off-host recovery of required
local-only state, database restore, protected-authority recovery, provider
recovery, and sole-operator continuity remain open or unvalidated as recorded in
the continuity and recovery register.
