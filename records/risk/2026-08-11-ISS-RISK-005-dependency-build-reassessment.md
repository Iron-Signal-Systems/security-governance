# ISS-RISK-005 — Dependency and Build-System Reassessment

## Reassessment identity

**Risk:** ISS-RISK-005
**Reassessment date:** 2026-08-11
**Treatment commit:** `7851fb38e9f8f9a3c2ecde1383319166042f8e34`
**Authority:** Sole project operator acting as Engineering Authority
**Independence:** Self-review; not independent
**Outcome:** `TREATMENT_PROGRESS_CONFIRMED`

## Prior state

**Likelihood:** 2
**Impact:** 3
**Rating:** `HIGH (6)`
**Treatment:** `REDUCE`
**Status:** `OPEN`

The prior risk state reflected meaningful uncertainty across the current
engineering dependency and build-system boundary.

## Treatment result considered

The focused treatment review established that:

- Atlas remains governed by its exact accepted ISRAS project pin;
- File Intelligence remains governed by its exact accepted ISRAS project pin;
- Domain Neutral Platform remains explicitly non-adopted pending
  `ISS-ENG-ACT-001`;
- the existing DNP validation boundary completed with 29 PASS and 0 FAIL;
- a governed vulnerability scan identified reachable `GO-2026-5970`;
- the affected selected `golang.org/x/text v0.29.0` dependency was remediated;
- the remediation was committed and merged to canonical DNP `dev`;
- post-remediation DNP validation again completed with 29 PASS and 0 FAIL; and
- the exact governed `govulncheck v1.6.0` rerun reported no vulnerabilities
  with exit status 0.

The treatment therefore demonstrated an operating ability to identify,
remediate, and revalidate a real dependency vulnerability rather than relying
only on documented intent.

## Current decision

**Likelihood:** 1
**Impact:** 3
**Rating:** `MEDIUM (3)`
**Treatment:** `REDUCE`
**Status:** `MONITORING`
**Next required review:** 2026-11-09 or earlier upon material change

Likelihood is reduced from 2 to 1 because current controls across the reviewed
dependency/build boundary have demonstrated actual detection and remediation
behavior.

Impact remains 3 because compromise of a trusted dependency, build input,
toolchain, validation mechanism, or engineering authority could still materially
affect repository integrity and accepted engineering output.

The residual rating is therefore `MEDIUM (3)`.

The risk remains under `REDUCE` treatment and moves to `MONITORING`. It is not
closed.

## Continuing conditions

The reduced likelihood depends on continued operation of the reviewed control
boundary, including:

- exact accepted ISRAS pins where projects are adopted;
- explicit review of dependency and module changes;
- integrity verification and build validation;
- applicable vulnerability analysis;
- constrained trusted build inputs;
- truthful handling of repositories that are not ISRAS-adopted; and
- reevaluation when a material dependency, toolchain, build, profile, or
  engineering-governance boundary changes.

`ISS-ENG-ACT-001` remains open for Domain Neutral Platform.

DNP shall not be represented as ISRAS-adopted unless that separate engineering
governance action is completed truthfully.

## Boundaries preserved

This reassessment does not:

- close ISS-RISK-005;
- claim zero vulnerabilities;
- claim the dependency supply chain cannot be compromised;
- claim DNP is ISRAS-adopted;
- close ISS-ENG-ACT-001;
- silently upgrade Atlas or File Intelligence to a newer ISRAS release;
- duplicate authoritative ISRAS controls in organizational governance;
- create independent review or personnel separation; or
- claim certification, attestation, or external assurance.

## External assurance

This is internal organizational risk treatment and self-review.

It does not claim independent assessment, certification, attestation, or other
external assurance.
