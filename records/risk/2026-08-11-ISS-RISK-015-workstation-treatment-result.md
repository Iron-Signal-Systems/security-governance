# ISS-RISK-015 — Primary Workstation Treatment Result

## Treatment identity

**Risk:** ISS-RISK-015
**Treatment review date:** 2026-08-11
**Treatment UTC:** `2026-08-11T09:48:34Z`
**Assessment commit:** `7a5562e148aafa35aeabe860c12a48fbc2e1b188`
**Protected supporting-state SHA-256:** `50a95651fcceda3fda4dbeaa0eb7fcfc6738046bfa9b642a3f79e1b598525871`
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

The detailed state remains protected locally.

Likelihood remains 2 and impact remains 3, so the risk remains `HIGH (6)` and
`OPEN` under `REDUCE` treatment.

Complete the identified remediation and perform another focused review before
lowering the risk rating.

## Privileged-access relationship

The primary workstation sudo/root authority remains retained under
`ISS-IAM-002` for required administration.

This treatment does not convert retained administrative privilege into routine
root operation and does not create personnel separation or independent review.

## Vulnerability relationship

The current `ISS-VUL-001` register remains authoritative for organizational
vulnerability findings.

This treatment does not claim zero vulnerabilities and does not supersede
existing technical applicability or mitigation records.

## Authentication and signing relationship

The workstation protects GitHub SSH authentication and Git signing authorities.

Their separate risk treatments remain authoritative and are not automatically
closed by this workstation review.

## Recovery relationship

Local snapshots and repository reconstruction may support recovery but are not
automatically trusted after compromise.

This treatment does not claim a destructive rebuild or compromise-recovery
exercise was performed.

## Security boundary

No secret material is committed.

The public record deliberately does not enumerate failed or unknown workstation
hardening details.

## External assurance

This is internal organizational risk treatment.

It does not claim independent assessment, certification, attestation, penetration
testing, or other external assurance.
