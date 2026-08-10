# Supplier Register

## Current state

**ISS-SUP-001 status:** `Implemented`
**Register state:** Operating
**Initial review:** 2026-08-09
**Review result:** `PASS_WITH_OPEN_DEPENDENCY_ACTIONS`
**Next required review:** 2027-08-09 or earlier upon material supplier/boundary change or relevant incident

The current register covers material hosted services in the present solo-project
development and administrative boundary.

It does not establish suitability for a future customer, production, regulated,
public-safety, or remote-support boundary.

## Current material suppliers

| Supplier ID | Provider / service | Current ISS boundary | Criticality | Review basis | Current decision | Material limitation / related action | Next review |
|---|---|---|---|---|---|---|---|
| ISS-SUP-001 | GitHub / GitHub organization and hosted Git repositories | `ISS-ASSET-001`; canonical remote source/governance/engineering history; organization administration | CRITICAL | Provider documentation for organization security controls, 2FA enforcement, audit logging, and compliance-report availability; ISS asset/risk/continuity records | `CONTINUE_CURRENT_USE` | Provider capability does not prove current ISS configuration. GitHub outage/account-recovery and alternate-path limitations remain under `ISS-BCP-ACT-005`; `ISS-RISK-003`, `ISS-RISK-010`, and `ISS-RISK-014` remain authoritative. | 2027-08-09 or earlier trigger |
| ISS-SUP-002 | Squarespace / domain and DNS service | `ISS-ASSET-013`; public domain/DNS and administrative authority | HIGH | Provider documentation for account 2FA/passkeys/recovery codes, domain/DNS security features, and security measures; ISS asset/risk/continuity records | `CONTINUE_CURRENT_USE` | Exact ISS account security/recovery configuration is not established by supplier review. Provider recovery/alternate path remains under `ISS-BCP-ACT-005`; `ISS-RISK-010` and `ISS-RISK-011` remain authoritative. | 2027-08-09 or earlier trigger |
| ISS-SUP-003 | Google / Gmail administrative email service | `ISS-ASSET-014`; ISS administrative/contact email | HIGH | Google account documentation for 2-Step Verification/passkeys and ISS asset/risk/continuity records | `CONTINUE_CURRENT_USE` | Exact account edition, security configuration, and recovery path are not established by supplier review. Provider recovery/alternate path remains under `ISS-BCP-ACT-005`; `ISS-RISK-010` and `ISS-RISK-012` remain authoritative. | 2027-08-09 or earlier trigger |

## Decision meaning

`CONTINUE_CURRENT_USE` means the current provider remains suitable for the
present reviewed boundary based on currently available information and existing
controls.

It is not an acceptance of every supplier-related risk and does not authorize a
future materially different use.

## Current dependency action

No duplicate supplier action is created for provider recovery.

`ISS-BCP-ACT-005` already requires review of provider recovery dependencies and
practical alternate/recovery paths for GitHub, Squarespace, and Gmail.

That action remains OPEN.

Supplier review completion does not close it.

## Related access-control boundary

Provider support for 2FA, passkeys, logs, recovery methods, or other controls does
not prove the applicable ISS account configuration.

Account and privileged-access state remain governed by `ISS-IAM-001` and
`ISS-IAM-002`.

## Risk relationship

This register directly informs current risks including:

- `ISS-RISK-003` — source repository loss/corruption;
- `ISS-RISK-010` — critical supplier/service outage;
- `ISS-RISK-011` — domain/DNS authority compromise;
- `ISS-RISK-012` — administrative email compromise/loss; and
- `ISS-RISK-014` — GitHub organization administrative compromise.

ISS-SUP-001 implementation does not automatically close, lower, or accept those
risks.

Risk status remains authoritative under `ISS-RSK-001`.

## Maintenance

New material suppliers use the next stable `ISS-SUP-NNN` identifier.

Identifiers shall not be reused.

A materially different service or future use may require a new register entry or
a new review of the existing entry before use.
