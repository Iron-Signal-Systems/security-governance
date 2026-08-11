# ISS-EXC-001 — Security Exception Governance

## Control identity

**Control ID:** ISS-EXC-001
**Control:** Security Exception Governance
**Status:** Implemented
**Control owner:** Security Authority
**Control operator:** Security Authority
**Approval authority:** Governance Authority
**Frequency:** Event-driven

## Objective

Ensure an intentional temporary deviation from a mandatory Iron Signal Systems
security requirement is explicit, bounded, risk-informed, approved by the
applicable authority, time-limited, reviewable, and closed or renewed through a
new decision rather than silently becoming permanent.

## Current organizational boundary

Iron Signal Systems is currently operated as a solo-developed project.

The same person currently performs the Security Authority and Governance
Authority responsibilities.

Where that person evaluates and approves an exception, the record is
self-approval and is not independent review.

AI, automation, alternate accounts, keys, or sessions do not create independent
human approval.

## What is an exception

An exception is an intentional, authorized, time-bounded deviation from a
mandatory organizational security requirement when the deviation is permitted
to be governed through this control.

An exception is not automatically created by an open risk, treatment action,
vulnerability, recovery limitation, supplier limitation, future boundary,
supported `NOT_APPLICABLE` decision, or pending engineering action.

## Fail-closed rule

When a mandatory requirement applies and cannot be satisfied, the dependent
activity shall not proceed unless the governing requirement permits an exception
path and an applicable approved exception is active and unexpired.

Absence of a documented applicable exception is not implicit approval.

## ISRAS boundary

ISS-EXC-001 does not override authoritative ISRAS requirements.

If an accepted applicable ISRAS release does not permit the proposed deviation
through its own governed mechanism, organizational exception authority cannot
convert the project into a conforming or releasable state.

## Required exception record

An exception record shall identify the requirement, scope, rationale, start and
expiration dates, risk impact, compensating measures, treatment/closure plan,
Security Authority evaluation, Governance Authority decision, independence
status, related records, lifecycle status, and closure or renewal basis.

Sensitive support may remain protected and be referenced by identifier or
digest.

## Duration

A normal approved exception shall expire no later than 90 days after activation.

A shorter duration shall be used when appropriate.

Exceptions do not renew automatically.

Continued deviation requires a new review and approval decision before the prior
exception expires.

## High and Critical risk

An exception that creates or materially increases High or Critical risk requires
explicit Governance Authority approval, corresponding current risk treatment
under `ISS-RSK-001`, compensating measures where reasonably available, a defined
treatment/closure plan, fixed expiration, and reevaluation if conditions worsen.

Approval of an exception does not silently accept or close the corresponding
risk.

## Emergency security action

During a real security incident or urgent recovery condition, immediate
containment or recovery may occur before normal exception paperwork when delay
would materially increase harm.

If the emergency action creates an actual deviation from a mandatory
requirement, the deviation shall be evaluated and recorded within 24 hours once
conditions permit.

## Decisions and lifecycle

Decisions are `APPROVE`, `REJECT`, or `WITHDRAW`.

Lifecycle status is `REQUESTED`, `ACTIVE`, `REJECTED`, `WITHDRAWN`, `EXPIRED`,
`REVOKED`, or `CLOSED`.

Only an approved, active, unexpired exception authorizes the recorded scope.

## Public and protected records

Public exception records may contain the control affected, rationale, scope,
risk, compensating measures, authority, dates, status, and closure basis.

Passwords, private keys, tokens, recovery codes, customer secrets, sensitive
support communications, and inappropriate exploit detail shall not be published.

## Current-state review

The initial operating review shall explicitly determine whether any active
intentional control exceptions are known.

`NO_ACTIVE_EXCEPTIONS_IDENTIFIED` means none were identified in the reviewed
current boundary. It does not claim no exception has ever existed historically
or that every possible deviation has been disproved.

## Related controls

Exception governance may interact with `ISS-GOV-001`, `ISS-RSK-001`,
`ISS-IAM-001`, `ISS-IAM-002`, `ISS-ENG-001`, applicable ISRAS, `ISS-VUL-001`,
`ISS-IR-001`, `ISS-BCP-001`, `ISS-SUP-001`, and `ISS-TRN-001`.

## Failure conditions

ISS-EXC-001 is not operating as required when a mandatory requirement is
intentionally bypassed without an applicable active exception, an organizational
exception is used to override ISRAS, an exception has no expiration, a normal
exception exceeds 90 days without a new decision, an expired exception is
treated as active, renewal is automatic, High/Critical risk is silently accepted,
an emergency deviation is not reviewed within 24 hours once conditions permit,
secrets are unnecessarily published, or self-approval is represented as
independent approval.

## Implementation state

The security-exception policy is active.

The exception register is operating.

Initial review `ISS-EXC-REV-001` retained result
`NO_ACTIVE_EXCEPTIONS_IDENTIFIED`.

ISS-EXC-001 is `Implemented`.

Implementation does not mean exceptions can override authoritative ISRAS
requirements, that open risks/actions are exceptions, or that future deviations
are pre-approved.
