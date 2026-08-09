# ISS-RSK-001 — Initial Security Risk Review

## Review identity

**Control ID:** ISS-RSK-001  
**Review date:** 2026-08-09  
**Review authority:** Sole project operator acting as Security Authority  
**Independence status:** Self-review; not independent  
**Reviewed repository commit:** `505acd889c91ebe7b32434bd19a2829106149d6e`  
**Review conclusion:** `COMPLETE_WITH_OPEN_RISKS`  
**Next required review:** 2026-11-09 or earlier upon material change

## Scope

The initial review considered:

- the operating asset boundary established by ISS-AST-001;
- the current solo-authority model;
- repository, authentication, and signing authority;
- the primary development/administrative workstation;
- local source recovery and remote repository synchronization;
- the active Atlas development PostgreSQL service;
- GitHub, Squarespace-managed domain/DNS, and Gmail dependencies;
- current engineering/dependency exposure;
- governance findings already recorded by ISS-GOV-001; and
- foreseeable future customer, deployment, service, and support boundaries.

## Assessment method

Likelihood and impact were assessed using the ISS-RSK-001 three-by-three model.

Where the current facts reasonably supported two adjacent values and the
uncertainty could not yet be resolved, the higher value was used.

Overall rating was derived mechanically from likelihood multiplied by impact.

## Currently applicable High risks

The following currently applicable risks are rated `HIGH (6)`:

- `ISS-RISK-001` — loss of sole engineering-authority availability;
- `ISS-RISK-002` — compromise of release-signing authority;
- `ISS-RISK-005` — dependency or build-system compromise;
- `ISS-RISK-014` — compromise of GitHub organization administrative authority;
- `ISS-RISK-015` — compromise of the primary development/administrative
  workstation.

None of these risks is accepted.

Each has a `REDUCE` treatment decision and a treatment target of 2026-11-09.

## Currently applicable Medium risks

The following currently applicable risks are rated `MEDIUM`:

- `ISS-RISK-003` — loss or corruption of source repositories: `MEDIUM (3)`;
- `ISS-RISK-010` — critical supplier or service outage: `MEDIUM (4)`;
- `ISS-RISK-011` — unauthorized domain/DNS change or compromise:
  `MEDIUM (4)`;
- `ISS-RISK-012` — compromise or loss of administrative email:
  `MEDIUM (4)`; and
- `ISS-RISK-013` — complete local work/recovery loss before remote
  synchronization: `MEDIUM (4)`.

These risks remain subject to treatment and quarterly review.

## Future-boundary risks

The following identified risks are not assigned current scores because the
underlying operating boundary does not currently exist:

- `ISS-RISK-004` — unauthorized access to customer information;
- `ISS-RISK-006` — security defect in an accepted product release;
- `ISS-RISK-007` — failed customer deployment or upgrade;
- `ISS-RISK-008` — inability to recover a customer-critical service; and
- `ISS-RISK-009` — compromise of remote-support credentials.

These risks remain `IDENTIFIED` and shall be assessed before their applicable
boundary becomes operational.

This is an explicit applicability decision, not an assertion that the future
risk is negligible.

## New risk identified

### ISS-RISK-015 — Primary workstation compromise

The asset inventory establishes the primary development workstation as a
Critical asset that also participates in repository administration and protects
authentication/signing authority.

A workstation compromise could therefore affect source integrity,
administrative authority, signing trust, and development data.

The risk is assessed:

- likelihood: `2 — POSSIBLE`;
- impact: `3 — SEVERE`;
- derived rating: `HIGH (6)`;
- treatment: `REDUCE`;
- owner: Security Authority;
- target: 2026-11-09.

## Treatment priorities

Before or during the next quarterly review, priority treatment work shall
include:

1. sole-authority continuity and recoverability;
2. signing-authority revocation and recovery;
3. dependency/build and vulnerability governance;
4. GitHub administrative-account and privileged-access governance;
5. primary workstation hardening and vulnerability governance;
6. supplier review for GitHub, Squarespace-managed domain/DNS, and Gmail; and
7. determining whether stronger independent backup/recovery is required beyond
   the current local snapshot and remote Git synchronization boundary.

These priorities identify treatment work. They do not silently mark the related
controls as implemented.

## Risk acceptance

No High or Critical risk was accepted during this review.

No exception to an organizational or engineering control was authorized.

## Overdue actions

No treatment action is overdue on the initial review date.

## Review conclusion

`COMPLETE_WITH_OPEN_RISKS`

The first formal ISS-RSK-001 assessment is complete for the current operating
boundary.

Open risk remains and requires treatment and review. Completion of this review
does not mean the operating environment is risk-free or that all planned
security controls are implemented.

## Independence statement

This review was performed by the same person currently exercising Security
Authority and therefore constitutes self-review.

AI assistance was used to structure and analyze the review record, but no AI
system is represented as an independent reviewer.

The signed commit accepting this record represents the Security Authority's
acceptance of the recorded assessment. No independent review is claimed.
