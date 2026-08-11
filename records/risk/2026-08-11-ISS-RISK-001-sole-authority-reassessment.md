# ISS-RISK-001 — Sole Engineering-Authority Availability Reassessment

## Reassessment identity

**Risk:** ISS-RISK-001
**Reassessment date:** 2026-08-11
**Treatment commit:** `f21b6e021376fd1d8484ab40b02a2cab28c090dc`
**Authority:** Sole project operator acting as Governance Authority
**Independence:** Self-review; not independent
**Outcome:** `RESIDUAL_HIGH_RISK_CONFIRMED`

## Prior state

**Likelihood:** 2
**Impact:** 3
**Rating:** `HIGH (6)`
**Treatment:** `REDUCE`
**Status:** `OPEN`

## Treatment result considered

The focused treatment review confirmed that current controls preserve
reconstructable engineering and governance context through remotely retained
repository history, signed history where applicable, governance records,
engineering records, and defined continuity procedures.

Those controls materially reduce loss of project context and improve
reconstruction capability.

They do not create another authorized human operator and do not prevent the
sole current Engineering Authority from becoming unavailable.

## Current decision

**Likelihood:** 2
**Impact:** 3
**Rating:** `HIGH (6)`
**Treatment:** `REDUCE`
**Status:** `OPEN`
**Next required review:** 2026-11-09 or earlier upon material change

Likelihood remains 2 because loss of sole-operator availability remains a
credible current condition while exactly one authorized operator exists.

Impact remains 3 because sufficiently prolonged unavailability could cause
sustained inability to perform engineering, governance, administrative, or
other trust-sensitive work.

The resulting rating therefore remains `HIGH (6)`.

The score is not reduced merely because treatment work was reviewed.

## Current continuity boundary

The current project may pause if the sole operator is unavailable.

There is no current alternate internal operator.

There is no current customer-production, customer-critical operated-service,
remote-support, or other established boundary that requires uninterrupted
continuation by another person.

That current limitation is explicitly governed rather than concealed.

## Continuing treatment

`ISS-BCP-REC-009` remains the authoritative sole-operator recovery-boundary
record.

`ISS-BCP-ACT-004` remains `OPEN`.

Before future obligations require continuation during sole-operator
unavailability, an appropriate continuity or succession mechanism shall be
established based on the actual organizational and legal state at that time.

No alternate authority shall be invented merely to lower this risk score.

## Boundaries preserved

This reassessment does not:

- lower the risk without factual support;
- close ISS-RISK-001;
- close ISS-BCP-ACT-004;
- invent an employee, collaborator, successor, or alternate operator;
- claim uninterrupted continuity;
- treat AI, automation, accounts, keys, or documentation as a second person;
- claim independent review or separation of personnel; or
- claim certification, attestation, or external assurance.

## External assurance

This is internal organizational risk treatment and self-review.

It does not claim independent assessment, certification, attestation, or other
external assurance.
