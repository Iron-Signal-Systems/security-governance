# ISS-IAM-002 — Initial Privileged Access Review

## Review identity

**Control ID:** ISS-IAM-002  
**Review date:** 2026-08-09  
**Review authority:** Sole project operator acting as Security Authority  
**Independence status:** Self-review; not independent  
**Reviewed repository commit:** `694e217e304fd005a0e4f4ed8bd688f1d8b9dba3`  
**Review result:** `PASS_WITH_OPEN_RISK_TREATMENT`  
**Next required review:** 2026-11-09 or earlier upon material privileged-access change

## Objective

Determine whether the currently identified material privileged authorities are
authorized, attributable, necessary, and appropriately represented for the
current solo-project operating model.

## Scope reviewed

The review covered:

- GitHub organization/repository administration;
- GitHub SSH authentication authority;
- Git commit-signing authority;
- sudo/root authority on the primary development workstation;
- Squarespace-managed domain/DNS administration and recovery;
- Gmail mailbox administration and recovery for `info@ironsignalsystems.com`;
- PostgreSQL administrative/superuser authority for the active local Atlas
  development service; and
- sudo/root administration of the `/src` Btrfs/Snapper recovery boundary.

No usernames, passwords, private keys, recovery codes, tokens, or secret values
are retained in this public review record.

## Review decisions

### ISS-PRIV-001 — GitHub organization administration

**Decision:** `RETAIN`

The sole project operator personally controls the current individually
attributable administrative account.

The authority remains necessary to administer the Iron Signal Systems GitHub
organization and repositories.

This decision does not close `ISS-RISK-014`; GitHub administrative compromise
remains a High open risk requiring continued treatment.

### ISS-PRIV-002 — GitHub SSH authentication authority

**Decision:** `RETAIN`

The current SSH authority is personally controlled and remains necessary for
authenticated repository operations.

Secret key material is not recorded.

### ISS-PRIV-003 — Git commit-signing authority

**Decision:** `RETAIN`

The signing authority is personally controlled and remains necessary for signed
repository history and governance acceptance.

This decision does not close `ISS-RISK-002`; signing-authority compromise remains
a High open risk requiring revocation/recovery treatment.

### ISS-PRIV-004 — Primary workstation sudo/root

**Decision:** `RETAIN`

The normal workstation account uses sudo/root elevation for administrative tasks
including software installation and system updates.

The review does not represent the workstation as routinely operated as root.

This decision does not close `ISS-RISK-015`; compromise of the primary
development/administrative workstation remains a High open risk.

### ISS-PRIV-005 — Domain and DNS administration

**Decision:** `RETAIN`

The sole project operator personally controls the administrative and recovery
authority for the current Squarespace-managed `ironsignalsystems.com` domain/DNS
boundary.

The authority remains necessary for current operation.

### ISS-PRIV-006 — Administrative Gmail authority

**Decision:** `RETAIN`

The sole project operator personally controls the mailbox and recovery authority
for `info@ironsignalsystems.com`.

The authority remains necessary for current operation.

### ISS-PRIV-007 — Atlas PostgreSQL administration

**Decision:** `RETAIN`

The sole project operator currently holds PostgreSQL administrative/superuser
authority for the active local Atlas development service.

That administrative authority remains necessary for development administration.

This review does not claim that application or runtime access requires
superuser authority.

### ISS-PRIV-008 — `/src` recovery administration

**Decision:** `RETAIN`

The `/src` Btrfs/Snapper recovery boundary is administered through the sole
project operator's sudo/root authority.

The privilege remains necessary for snapshot administration and recovery.

This decision does not establish that the current recovery design is sufficient
against complete host/storage loss; continuity and backup adequacy are governed
separately.

## Least-privilege conclusion

No currently reviewed privilege was identified as unnecessary for the current
one-person operating model.

The concentration of administrative authority is real and remains a material
risk condition.

The review therefore retains the necessary privileges rather than creating
artificial separation or claiming independence that does not exist.

## Open findings

### IAM-REVIEW-001 — GitHub administrative authority risk remains open

**Related risk:** `ISS-RISK-014`  
**Status:** Open  
**Target:** 2026-11-09

The first privileged-access review confirms the current GitHub administrative
authority is necessary and attributable, but it does not by itself establish the
full account-recovery, revocation, and hardening treatment required by the High
risk.

### IAM-REVIEW-002 — Signing-authority recovery remains open

**Related risk:** `ISS-RISK-002`  
**Status:** Open  
**Target:** 2026-11-09

The signing authority remains necessary. Revocation and recovery handling remain
part of the High-risk treatment plan.

### IAM-REVIEW-003 — Primary workstation hardening remains open

**Related risk:** `ISS-RISK-015`  
**Status:** Open  
**Target:** 2026-11-09

Administrative elevation is limited to required system administration in the
reviewed operating model, but workstation hardening and vulnerability governance
remain open treatment work.

## Risk-treatment impact

This review establishes the current privileged-access boundary and confirms
which authorities are necessary.

It advances treatment of `ISS-RISK-002`, `ISS-RISK-014`, and `ISS-RISK-015` by
making the privileged authority explicit and reviewable.

It does not reduce their current risk ratings and does not mark those risks
closed or accepted.

## Review result

`PASS_WITH_OPEN_RISK_TREATMENT`

ISS-IAM-002 is operating for the current privileged-access boundary.

The PASS result applies to completion and truthfulness of the privileged-access
review. It does not mean all associated security risks or future access controls
are complete.

## Independence statement

This review was performed by the same person who currently holds the reviewed
privileged authorities.

The review is therefore self-review and is not represented as independent
review.

AI assistance was used to structure and analyze the record, but no AI system is
represented as an independent reviewer.

The signed commit accepting this record represents the Security Authority's
acceptance of the review.
