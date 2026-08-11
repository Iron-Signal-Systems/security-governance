# ISS-RISK-015 — Workstation Remediation Reassessment

## Reassessment identity

**Risk:** ISS-RISK-015
**Reassessment date:** 2026-08-11
**Reassessment UTC:** `2026-08-11T10:53:15Z`
**Remediation commit:** `420c300fa569482c71d296e235db23d535a4798a`
**Protected supporting-state SHA-256:** `dcbc6b5b514268b1d84c1ae14711df07219235aa826b39209bf6bce27ab317cd`
**Authority:** Sole project operator acting as Security Authority
**Independence:** Self-review; not independent
**Outcome:** `TREATMENT_PROGRESS_CONFIRMED`

## Prior state

**Likelihood:** 2
**Impact:** 3
**Rating:** `HIGH (6)`
**Treatment:** `REDUCE`
**Status:** `OPEN`

The prior focused assessment identified exactly two negative categories in its
protected supporting state:

- current unmitigated Critical/High workstation vulnerability condition; and
- protected remote administration.

The historical assessment remains unchanged.

## Current decision

**Likelihood:** 1
**Impact:** 3
**Rating:** `MEDIUM (3)`
**Treatment:** `REDUCE`
**Status:** `MONITORING`
**Next required review:** 2026-11-09 or earlier upon material change

The two deficiencies from the earlier focused workstation assessment are now
addressed for the reviewed current state.

Effective remote administration verifies as key-only under the required
conditions. The current High workstation advisory candidates have accountable
technical dispositions: one is technically not applicable to the reviewed
installed/configured boundary and one remains installed but is mitigated by an
explicit operating restriction.

This supports reducing likelihood from 2 to 1. Impact remains 3 because
workstation compromise would still materially affect authentication, signing,
repository administration, and local development state.

The resulting residual rating is `MEDIUM (3)`. The risk remains under `REDUCE`
treatment and moves to `MONITORING`; it is not closed.

## Boundaries preserved

This reassessment does not:

- claim zero vulnerabilities;
- close the workstation risk;
- claim the affected package in the mitigated advisory was vendor-fixed;
- erase continuing scanner output;
- close `ISS-RISK-014`, `ISS-RISK-005`, or any other separate risk;
- claim that local snapshots are trusted compromise-recovery media;
- create independent review or personnel separation; or
- override applicable `ISS-VUL-001`, `ISS-IAM-002`, `ISS-IR-001`,
  `ISS-BCP-001`, `ISS-ENG-001`, or ISRAS authority.

## External assurance

This is internal organizational risk treatment and self-review.

It does not claim independent assessment, certification, attestation, or other
external assurance.
