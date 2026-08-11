# ISS-RISK-002 — Signing Authority Treatment Result

## Treatment identity

**Risk:** ISS-RISK-002
**Treatment review date:** 2026-08-11
**Treatment UTC:** `2026-08-11T09:32:29Z`
**Assessment commit:** `d1b282d737b1a3660909d2ec5e0e0a0cd4909a09`
**Protected supporting-state SHA-256:** `b86b7109441bdd292abda2a91249184d31d8e3fcc4abfbe75e62a0dc2a8fefea`
**Treatment authority:** Sole project operator acting as Engineering Authority
**Independence:** Self-review; not independent
**Outcome:** `TREATMENT_PROGRESS_CONFIRMED`

## Rating decision

**Prior likelihood:** 2
**Prior impact:** 3
**Prior rating:** `HIGH (6)`

**Current likelihood:** 1
**Current impact:** 3
**Current rating:** `MEDIUM (3)`
**Treatment:** `REDUCE`
**Status:** `MONITORING`
**Next required review:** 2026-11-09 or earlier upon material change

Every required focused review category was affirmatively confirmed and current signed Git history verified successfully.

The operator-observed current state supports reducing likelihood from 2 to 1. Impact remains 3 because compromise of signing authority would still materially affect repository and engineering trust.

The resulting residual rating is `MEDIUM (3)`.

The risk is not closed. It remains under `REDUCE` treatment and moves to `MONITORING`. `ISS-RISK-015` remains separately open and shall continue to be treated under its own authority.

## Privileged-access relationship

The focused review covers the Git commit-signing authority already retained
under `ISS-IAM-002`.

The signing privilege remains necessary for the current operating model.

This treatment does not create personnel separation or independent review.

## Continuity relationship

A non-secret signing-authority revocation/replacement/transition procedure now
exists.

`ISS-BCP-REC-006` is updated from `NOT_VALIDATED` to
`PROCEDURE_DEFINED_NOT_EXERCISED`.

That is not the same as a successful signing-authority replacement or recovery
exercise.

Private-key backup is not asserted.

## Workstation relationship

`ISS-RISK-015` remains separately governed.

This treatment does not claim the primary development/administrative workstation
is fully hardened, independently assessed, or unable to expose signing authority
during compromise.

## Engineering relationship

Applicable `ISS-ENG-001` and ISRAS requirements remain authoritative.

This treatment does not override engineering release or signature requirements.

## Security boundary

No secret material is committed.

The public record deliberately does not enumerate any failed or unknown
signing-protection detail.

## External assurance

This is internal organizational risk treatment.

It does not claim independent assessment, certification, attestation, or other
external assurance.
