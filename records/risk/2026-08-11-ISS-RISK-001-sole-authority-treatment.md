# ISS-RISK-001 — Sole Engineering-Authority Availability Treatment Review

## Review identity

**Risk:** ISS-RISK-001
**Review date:** 2026-08-11
**Authority:** Sole project operator acting as Governance Authority
**Independence:** Self-review; not independent
**Result:** `TREATMENT_PROGRESS_CONFIRMED`

## Current risk state

**Likelihood:** 2
**Impact:** 3
**Rating:** `HIGH (6)`
**Treatment:** `REDUCE`
**Status:** `OPEN`

ISS-RISK-001 addresses loss of availability of the sole current Engineering
Authority.

The current organizational state contains one operator. No alternate internal
operator, successor, recovery operator, or independent engineering authority
currently exists.

## Existing treatment

Current treatment reduces loss of engineering context and recoverable project
state through:

- canonical remotely pushed Git repository history;
- signed Git history where applicable;
- retained engineering and governance records;
- explicit repository and engineering-governance state;
- documented authentication and signing-authority replacement procedures;
- local recovery mechanisms for applicable development state; and
- governed continuity and recovery records.

These controls improve reconstructability and reduce loss of institutional
context.

They do not create another authorized human operator.

## Current continuity decision

Under the current solo-project boundary, Iron Signal Systems work may pause if
the sole operator is unavailable.

There is currently no customer-production, customer-critical operated service,
remote-support, or other established operating boundary that requires
uninterrupted continuation by another person.

No alternate operator, successor, escrow authority, or continuity arrangement
shall be represented as existing when it does not exist.

Before future customer, production, support, legal, contractual, public-safety,
or similar obligations require continued operation during sole-operator
unavailability, an appropriate continuity or succession path shall be
established and governed.

## Continuity relationship

`ISS-BCP-REC-009` remains the authoritative recovery-boundary record for
sole-operator availability.

`ISS-BCP-ACT-004` remains open.

The action shall not be closed by inventing an alternate authority or by
representing documentation, AI, automation, credentials, alternate accounts,
or cryptographic keys as another human operator.

## Treatment conclusion

Existing treatment materially improves reconstructability and limits loss of
project context.

It does not materially reduce the probability that the sole operator could
become unavailable, and it does not eliminate the possibility of sustained
inability to operate while no alternate authorized operator exists.

Accordingly, this treatment record does not lower the current risk score.

A separate reassessment shall confirm the residual likelihood, impact, rating,
treatment, and status.

## Boundaries preserved

This review does not:

- invent an employee, collaborator, successor, officer, or alternate operator;
- claim uninterrupted continuity;
- claim that repository history creates operational succession;
- claim local snapshots are independent off-host recovery;
- claim credential or signing-secret recovery that has not been exercised;
- create independent review or personnel separation;
- close `ISS-BCP-ACT-004`;
- close `ISS-RISK-001`; or
- claim certification, attestation, or external assurance.

## External assurance

This is internal organizational risk treatment and self-review.

It does not claim independent assessment, certification, attestation, or other
external assurance.
