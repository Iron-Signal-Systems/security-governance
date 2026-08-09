# Account Access Register

## Current state

**ISS-IAM-001 status:** `Implemented`
**Register state:** Operating
**Initial review:** 2026-08-09
**Next required action:** Event-driven upon provisioning, material change, loss of need, compromise, disablement, or removal

This register intentionally excludes passwords, private keys, tokens, recovery
codes, password hashes, and other authentication secrets.

Exact usernames and provider-specific account identifiers are withheld where
they are not necessary to establish the governance boundary.

## Register

| Account ID | System / service | Identity type | Authorized purpose | Authority boundary | Current decision | Verification / note |
|---|---|---|---|---|---|---|
| ISS-ACC-001 | Iron Signal Systems GitHub organization | Human provider account | Administer current ISS organization and repositories | Organization/repository administration as separately reviewed by ISS-IAM-002 | RETAIN | Current administrative authority is already present in the privileged-access boundary; exact account identifier is not published here. |
| ISS-ACC-002 | Primary ISS development/admin workstation | Human local account | Daily development and administration through bounded elevation when required | Normal interactive account with administrative elevation capability governed separately by ISS-IAM-002 | RETAIN | Current local identity was observed during the initial review; exact username is retained only in protected local supporting state. |
| ISS-ACC-003 | Primary ISS development/admin workstation | Built-in administrative identity | Required operating-system administrative authority | Root administrative authority; routine direct-root use is not asserted | RETAIN | Built-in authority remains required for system administration. Normal operation continues through the human account with elevation as needed. |
| ISS-ACC-004 | `ironsignalsystems.com` / DNS provider | Human provider account | Administer current domain and DNS configuration | Provider administrative/recovery authority | RETAIN | Current authority is required. Exact provider account identifier is not published. |
| ISS-ACC-005 | `info@ironsignalsystems.com` / Google account boundary | Human provider account | Operate and recover the current ISS administrative/contact mailbox | Mailbox and recovery administration | RETAIN | Current authority is required. Recovery secrets are not recorded. |
| ISS-ACC-006 | Local Atlas PostgreSQL development service | Database administrative identity / role boundary | Administer the local Atlas development database | Administrative/superuser database authority | RETAIN | Administrative authority remains required for development administration. Exact database role names are not published. |
| ISS-ACC-007 | Local Atlas PostgreSQL development service | Operating-system service identity | Run the local PostgreSQL service under its configured service identity | Local service execution and database-file access required by the service | RETAIN | Service identity was resolved from local service configuration during the initial review; exact identity is retained in protected local supporting state. |

## Initial review result

All seven currently identified material account or identity boundaries have a
current authorized operating purpose.

No current account was identified as requiring `MODIFY`, `DISABLE`, `REMOVE`,
`REPLACE`, or `PENDING_REVIEW`.

No departed-personnel account exists in the current solo-project baseline.

This result does not close risks associated with concentrated administrative,
authentication, signing, workstation, or supplier authority.

## Relationship to privileged access

Where these identities hold privileged authority, that privilege remains
separately governed by ISS-IAM-002 and the privileged-access register.

ISS-IAM-001 does not replace quarterly privileged-access review.

## Maintenance rule

New material account or identity boundaries shall receive the next stable:

`ISS-ACC-NNN`

identifier.

Identifiers shall not be reused.

A material lifecycle event shall update the applicable account record and create
a lifecycle record under `records/access/`.

Removed identifiers remain historically reserved and shall not be reassigned.
