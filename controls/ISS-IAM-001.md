# ISS-IAM-001 — Account Provisioning and Removal

## Control identity

**Control ID:** ISS-IAM-001
**Control:** Account Provisioning and Removal
**Status:** Implemented
**Control owner:** System Owner
**Control operator:** System Owner / Security Authority
**Frequency:** Event-driven and upon material identity-boundary change

## Objective

Ensure accounts and material service identities that can access Iron Signal
Systems-controlled systems or governed services are explicitly authorized,
appropriately scoped, attributable where supported, and removed or disabled when
their authorization ends.

## Relationship to ISS-IAM-002

ISS-IAM-001 governs the lifecycle of accounts and material service identities.

ISS-IAM-002 separately governs periodic privileged-access review.

A privileged account may therefore be governed by both controls:

- ISS-IAM-001 answers whether the account or identity should exist and retain
  access; and
- ISS-IAM-002 answers whether its privileged authority remains necessary and
  appropriately bounded.

Credential, key, token, and recovery-authority detail shall not be duplicated in
the account register merely to prove that an account exists.

## Current organizational boundary

Iron Signal Systems is currently operated as a solo-developed project.

The current control shall not invent employees, managers, departments,
termination workflows, or independent approvers that do not exist.

The System Owner and Security Authority may currently be the same person.

Where review is performed by the same person who holds the account, it is
self-review and is not independent review.

## Account scope

This control applies to material accounts and identities that can access or
operate current ISS-controlled systems or governed services, including as
applicable:

- human user accounts;
- administrative accounts;
- built-in administrative identities where their use affects ISS assets;
- database accounts or roles with material authority;
- operating-system service identities with material access;
- vendor-managed service accounts used to administer ISS assets; and
- future automation or service accounts with material access.

A cryptographic key, signing key, recovery code, or token is not by itself an
account. Its authority may be governed by ISS-IAM-002 or another applicable
control.

## Provisioning requirements

Before a new material account or identity receives access, the responsible
System Owner shall establish:

- the system or service;
- the identity type;
- the authorized person, service, or operating purpose;
- the access required;
- why that access is necessary;
- the minimum practical authority;
- the authorizing role;
- the provisioning date or effective state; and
- any required follow-up or expiration condition.

Access shall not be provisioned merely because a technical capability exists.

Where a provider or platform creates a built-in or service identity
automatically, the identity shall still have a legitimate operating purpose and
shall not be silently treated as authorized solely because it exists.

## Identity and attribution

Human access shall use an individually attributable identity where the system
supports it.

Shared human accounts shall be avoided.

If a shared account is technically unavoidable, the record shall state the
reason, authorized custody, and removal or replacement plan where applicable
without publishing the secret.

Non-human or service identities shall have a defined operating purpose and
accountable owner.

## Least privilege

Provisioned access shall be no broader than the minimum practical authority
required for the current operating purpose.

Privilege review for material administrative authority is additionally governed
by ISS-IAM-002.

## Change requirements

A material account or access change requires reevaluation when:

- the operating purpose changes;
- a system or service changes;
- authority is increased or reduced;
- a person or service changes role;
- a credential or account is suspected or confirmed compromised;
- a shared identity is replaced;
- a service identity is no longer required; or
- another material authorization condition changes.

The result shall be recorded as retained, modified, disabled, removed, or
pending review.

## Removal requirements

Access shall be disabled or removed promptly when authorization ends, including
after:

- loss of operational need;
- departure or termination where personnel later exist;
- role or responsibility change;
- service retirement;
- replacement of a shared or service identity;
- credential or account compromise when continued access cannot safely remain
  active; or
- another material authorization change.

Removal shall include the account, role, group membership, delegated authority,
or other access path necessary to end the governed authorization.

A removal shall not be represented as complete until the removed or disabled
state has been verified.

## Compromise handling

Suspected or confirmed compromise may require immediate disablement,
credential/key revocation, or authority reduction before ordinary lifecycle
review is complete.

Incident handling is governed separately where ISS-IR-001 applies.

The need for rapid containment does not remove the requirement to record the
resulting account state.

## Account decisions

Each material lifecycle review shall use one current decision:

- `RETAIN` — account and current access remain authorized;
- `MODIFY` — account remains authorized but access must change;
- `DISABLE` — access must be suspended while the account is retained;
- `REMOVE` — the account or governed access path is no longer authorized;
- `REPLACE` — an account or identity shall be replaced by another controlled
  identity; or
- `PENDING_REVIEW` — sufficient information is not yet available for a final
  decision.

`PENDING_REVIEW` shall not be used to conceal a known unauthorized account.

## Required lifecycle record

A material provisioning, modification, disablement, removal, or review record
shall identify:

- control ID;
- date;
- system or service;
- stable account or identity record ID;
- account or identity type;
- authorized operating purpose;
- authorizing role;
- current decision;
- completed action;
- verification result;
- unresolved finding where applicable; and
- independence status where a review occurred.

Exact usernames may be withheld from the public governance register when they
are not necessary to establish the control boundary.

## Register and records

The non-sensitive current identity boundary is retained in:

`registers/ACCOUNT-ACCESS-REGISTER.md`

Lifecycle and review records are retained under:

`records/access/`

Passwords, private keys, tokens, recovery codes, password hashes, secret
questions, or other authentication secrets shall not be committed to prove that
an account was provisioned or removed.

## Independence

ISS-IAM-001 is an operational identity-lifecycle control.

Under the current solo-project baseline, the System Owner or Security Authority
may authorize and review access they personally hold when no independent
approval requirement applies.

Such authorization or review is self-governance and shall not be represented as
independent review.

AI systems, alternate accounts, separate keys, automation, or separate sessions
do not create independent human review.

## Failure conditions

ISS-IAM-001 is not operating as required when:

- a known material account exists without an authorized operating purpose;
- access is provisioned without authorization;
- an account known to have lost its authorization is intentionally retained
  without remediation or a governed exception;
- a required disablement or removal is represented as complete without
  verification;
- a shared account is silently represented as individually attributable;
- a material service identity has no defined purpose or owner;
- secrets are published as lifecycle records;
- a known account-lifecycle finding is omitted; or
- self-review is represented as independent review.

## Implementation state

The initial account and material identity review has been completed for the
current operating boundary.

A current non-sensitive account-access register and initial lifecycle review
record are retained in the governance repository.

No currently identified material account was found to lack an authorized
operating purpose, and no current removal event was identified by the initial
review.

ISS-IAM-001 is `Implemented`.

Implementation does not mean every future account is automatically authorized,
that privileged-access risks are closed, or that independent review has
occurred.
