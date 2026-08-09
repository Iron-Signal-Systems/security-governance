# ISS-IAM-002 — Privileged Access Review

## Control identity

**Control ID:** ISS-IAM-002  
**Control:** Privileged Access Review  
**Status:** Defined  
**Control owner:** Security Authority  
**Control operator:** Security Authority  
**Frequency:** At least quarterly and after material privileged-access change

## Objective

Ensure privileged access to material Iron Signal Systems systems and services
remains authorized, attributable, necessary, and no broader than the current
operational need requires.

## Privileged access

Privileged access includes authority that can materially alter:

- repository or organization administration;
- source or governance history;
- release or signing trust;
- system configuration or software;
- authentication or recovery authority;
- domain or DNS configuration;
- administrative email or account recovery;
- databases or protected development data;
- backup or recovery state; or
- other controls protecting material ISS assets.

Possession of a credential or key is not itself proof that the associated
privilege remains authorized.

## Requirement

At least quarterly, the Security Authority shall review material privileged
access and determine for each observed privileged identity or authority:

- the system or service;
- the identity or authority being reviewed;
- whether the identity is individually attributable where supported;
- the privilege level or administrative capability;
- the current operational need;
- whether the privilege remains necessary;
- whether a less-privileged alternative is practical;
- whether authentication and recovery authority remain appropriately protected;
- whether access shall be retained, reduced, rotated, revoked, or otherwise
  remediated; and
- any unresolved finding requiring follow-up.

A material privileged-access change shall trigger an earlier review when waiting
for the next quarterly review would leave the current authorization state
uncertain.

## Current review boundary

The initial review shall consider, at minimum:

- Iron Signal Systems GitHub organization administrative authority;
- GitHub SSH authentication authority;
- Git commit-signing authority where compromise would affect trusted history;
- privileged access on the primary development/administrative workstation;
- administrative authority for `ironsignalsystems.com` and its DNS service;
- administrative/recovery authority for `info@ironsignalsystems.com`;
- privileged authority over the active Atlas development PostgreSQL service; and
- privileged authority over the local `/src` snapshot/recovery boundary.

The review boundary shall expand when additional material systems or services are
introduced.

## Identity and attribution

Administrative access shall use an individually attributable identity where the
system supports it.

Shared credentials shall be avoided.

If a system requires shared or non-individual authority, the review record shall
identify the reason and how custody is controlled without publishing the secret.

## Least privilege

Privilege shall be limited to the minimum practical authority required for the
current operating model.

The current solo-project state may legitimately require one person to hold
multiple privileged roles.

That concentration shall be recorded as an operating fact and risk condition. It
shall not be represented as personnel separation or independent oversight.

## Access decisions

Each reviewed privileged authority shall receive one decision:

- `RETAIN` — current privilege remains necessary and appropriately bounded;
- `REDUCE` — current authority is broader than necessary and shall be reduced;
- `ROTATE` — credential or key material shall be replaced while authority
  remains required;
- `REVOKE` — privilege is no longer authorized;
- `REMEDIATE` — access remains temporarily necessary but a security or
  governance deficiency requires corrective action; or
- `PENDING_REVIEW` — insufficient information exists to make a final decision.

`PENDING_REVIEW` shall not be used to avoid resolving known privileged-access
questions.

## Findings and treatment

A privileged-access deficiency shall identify:

- affected system or authority;
- finding;
- required corrective action;
- accountable owner;
- target date;
- status; and
- related risk or control where applicable.

A High or Critical risk related to privileged authority shall not be silently
closed merely because the access review occurred.

## Required review record

Each completed review shall identify:

- control ID;
- review date;
- review authority;
- exact governed state reviewed;
- systems and services reviewed;
- identities or authorities observed;
- privilege retained, reduced, rotated, revoked, or remediated;
- unresolved findings;
- related risk-treatment impact;
- next required review date; and
- independence status.

## Registers and records

The current non-sensitive privileged-access boundary is retained in:

`registers/PRIVILEGED-ACCESS-REGISTER.md`

Review records are retained under:

`records/access/`

Secrets, private keys, recovery codes, passwords, token values, internal
addresses, or other restricted details shall not be committed merely to prove
that an access review occurred.

## Independence

ISS-IAM-002 is an operational access-governance control.

Under the current solo-project baseline, the Security Authority may review the
privileged access they personally hold.

That review is self-review and shall not be represented as independent review.

Where future requirements demand independent privileged-access review, a
qualified independent person must perform that review.

## Failure conditions

ISS-IAM-002 is not operating as required when:

- a known material privileged authority is intentionally omitted;
- an unauthorized or unnecessary privilege is knowingly retained without a
  recorded remediation or authorized exception;
- a shared credential is silently treated as individually attributable;
- secrets are published as part of the review;
- a quarterly or required change-triggered review becomes overdue;
- unresolved findings are omitted; or
- self-review is represented as independent review.

## Implementation state

This document defines ISS-IAM-002 and the initial privileged-access review
boundary.

ISS-IAM-002 remains `Defined` until:

1. the actual current privileged identities and authorities are reviewed;
2. each material privilege receives an explicit decision;
3. unresolved findings and corrective actions are recorded;
4. the first review record is retained; and
5. the catalog and machine-readable registry are updated consistently.
