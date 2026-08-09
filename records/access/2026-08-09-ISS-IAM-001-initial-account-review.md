# ISS-IAM-001 — Initial Account and Identity Lifecycle Review

## Review identity

**Control ID:** ISS-IAM-001
**Review date:** 2026-08-09
**Review authority:** Sole project operator acting as System Owner / Security Authority
**Independence status:** Self-review; not independent
**Definition commit:** `fbcd21f79c3d9a64f35a6e0a1aec1b4b6ef80b4e`
**Protected supporting-state SHA-256:** `6fb3f13ab09453c9282ab76514db3261dc284fc2e23f111afd27888b5d4c893b`
**Review result:** `PASS`

## Purpose

This record establishes the initial operating baseline for ISS-IAM-001.

The review determines whether the currently identified material account and
identity boundaries have an authorized operating purpose and whether any current
identity requires modification, disablement, removal, replacement, or further
review.

## Current organizational state

Iron Signal Systems is currently operated as a solo-developed project.

No employee, department, manager, personnel termination, or separate internal
approval structure is represented by this review.

The same person currently performs the System Owner and Security Authority
responsibilities.

## Reviewed boundary

The initial review covered the currently identified material identity boundaries
associated with:

- GitHub organization and repository administration;
- the primary development/admin workstation;
- built-in local administrative authority;
- domain and DNS administration;
- the current administrative/contact mailbox and its recovery authority;
- local Atlas PostgreSQL database administration; and
- the local PostgreSQL operating-system service identity.

Credential-only authorities such as SSH keys and Git signing keys are not
duplicated as accounts. Their privileged authority remains governed where
applicable by ISS-IAM-002.

## Review method

The review used:

- the current privileged-access register as the existing non-sensitive
  administrative authority boundary;
- the current workstation operating state;
- the local PostgreSQL service configuration;
- the current solo-project organizational state; and
- direct review of whether each current identity still has an operating need.

Exact local usernames and the resolved PostgreSQL service identity are retained
in the protected local supporting state and are not published in this record.

No password, token, private key, recovery code, password hash, or authentication
secret was collected for this review.

## Decisions

The resulting public account-access register contains seven stable identity
records.

All seven receive `RETAIN`.

No current identity was identified as requiring:

- `MODIFY`;
- `DISABLE`;
- `REMOVE`;
- `REPLACE`; or
- `PENDING_REVIEW`.

No account was provisioned merely to complete this control.

## Removal state

No current removal-triggering event was identified.

In particular, the current solo-project baseline has no departed personnel whose
access must be removed.

This statement does not create a future personnel assumption. If additional
people later receive access, departure or role change becomes an event-driven
removal trigger under ISS-IAM-001.

## Verification

The current local human workstation identity was observed.

The built-in root identity exists as an operating-system administrative
authority.

The PostgreSQL service identity was resolved from the installed service
configuration.

The current privileged-access register continues to identify the existing remote
and administrative authority boundaries used by this review.

The resulting account-access register therefore represents the currently known
material identity boundary without publishing sensitive account identifiers.

## Risk relationship

This review does not reduce or close existing risks associated with:

- GitHub organization administration;
- signing or authentication authority;
- primary workstation compromise;
- supplier/provider compromise;
- concentrated solo-operator authority; or
- database administration.

Where privileged authority is involved, ISS-IAM-002 remains independently
required as a separate operational control.

## Lifecycle trigger

ISS-IAM-001 is event-driven.

A new operating record is required when a material account is provisioned,
materially changed, disabled, removed, replaced, compromised, or otherwise
changes authorization state.

A material identity-boundary change also requires reevaluation of this register.

## Independence statement

This review was performed by the same person who currently holds the human
accounts and administrative responsibilities in the reviewed boundary.

It is self-review and is not represented as independent review.

AI assistance was used to structure the control and review record, but no AI
system is represented as an independent reviewer.

## Conclusion

The current account and material identity boundary is explicitly recorded and
authorized for the current solo-project operating model.

No unauthorized or obsolete material account was identified by this initial
review.

ISS-IAM-001 has completed its initial operating review and is `Implemented`.
