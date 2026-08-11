# ISS-RISK-014 — GitHub Administrative Authority Treatment Result

## Treatment identity

**Risk:** ISS-RISK-014
**Treatment review date:** 2026-08-10
**Treatment UTC:** `2026-08-11T08:37:56Z`
**Assessment commit:** `ab8fbb073e0a7b1af01092d8f795a437eb0d05c5`
**Protected supporting-state SHA-256:** `f6229cae7f03687e8dc0847236b2aa6f2ba9bdf987448817977a0e7414570754`
**Treatment authority:** Sole project operator acting as Security Authority
**Independence:** Self-review; not independent
**Outcome:** `TREATMENT_REMEDIATION_REQUIRED`

## Rating decision

**Prior likelihood:** 2
**Prior impact:** 3
**Prior rating:** `HIGH (6)`

**Current likelihood:** 2
**Current impact:** 3
**Current rating:** `HIGH (6)`
**Treatment:** `REDUCE`
**Status:** `OPEN`
**Next required review:** 2026-11-09 or earlier upon material change

One or more required focused review categories was `NO` or `UNKNOWN`.

Detailed state remains protected locally and is not published. Likelihood remains 2 and impact remains 3, so the risk remains `HIGH (6)` and `OPEN` under `REDUCE` treatment. Complete the identified remediation and repeat the focused review before lowering the rating.

## Privileged-access relationship

The focused review covers the GitHub organization administrative authority and
GitHub SSH authentication authority already retained under `ISS-IAM-002`.

The privileges remain necessary for the current solo-project operating model.
This treatment does not create personnel separation or independent approval.

## Recovery relationship

A non-secret recovery/revocation procedure now exists for GitHub administrative
and SSH authentication authority.

`ISS-BCP-REC-005` is updated to `PROCEDURE_DEFINED_NOT_EXERCISED`.
That is not the same as a successful recovery exercise.

`ISS-BCP-ACT-005` remains open because the broader provider-recovery action also
covers additional provider boundaries and because full provider/account recovery
has not been exercised.

## Security boundary

No secrets are committed. The public record deliberately does not enumerate any
failed or unknown authentication-control detail.

## External assurance

This is internal organizational risk treatment. It does not claim independent
assessment, certification, attestation, or other external assurance.
