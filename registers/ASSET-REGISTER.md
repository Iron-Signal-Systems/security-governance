# Asset Register

## Purpose

This register identifies material Iron Signal Systems information systems,
repositories, services, credentials, infrastructure, and operational
dependencies.

The register intentionally records only non-sensitive information suitable for
the public governance repository. Private keys, tokens, internal addresses,
recovery secrets, and similarly sensitive values are not recorded here.

## Current completeness state

**State:** Initial inventory under review  
**ISS-AST-001 status:** `Defined`  
**Last inventory preparation:** 2026-08-09

The repository and GitHub organization entries below are substantiated by the
current GitHub organization boundary. The local development and credential
entries are limited to the operational facts required to describe the boundary
without publishing secrets.

This inventory shall not be represented as complete until the System Owner has
reviewed material non-GitHub dependencies such as domains, DNS, email, backup
targets, administrative services, hosted infrastructure, and other systems
actually in use.

## Inventory

| Asset ID | Asset | Type | Owner | Classification | Criticality | State | Canonical location / boundary | Notes |
|---|---|---|---|---|---|---|---|---|
| ISS-ASSET-001 | Iron Signal Systems GitHub organization | Hosted development / administrative service | System Owner | CONFIDENTIAL | CRITICAL | ACTIVE | `github.com/Iron-Signal-Systems` | Canonical organization boundary for current ISS repositories; administrative credentials are not recorded here. |
| ISS-ASSET-002 | `Iron-Signal-Systems/atlas` | Source repository | Engineering Authority | PUBLIC | HIGH | ACTIVE | GitHub | Atlas source and engineering history. |
| ISS-ASSET-003 | `Iron-Signal-Systems/domain-neutral-platform` | Source repository | Engineering Authority | PUBLIC | HIGH | ACTIVE | GitHub | Product/platform source and engineering history. |
| ISS-ASSET-004 | `Iron-Signal-Systems/engineering-standards` | Engineering-standard repository | Engineering Authority | PUBLIC | CRITICAL | ACTIVE | GitHub | Authoritative ISRAS source and accepted engineering-standard history. |
| ISS-ASSET-005 | `Iron-Signal-Systems/engineering-standards-legacy` | Historical repository | Engineering Authority | PUBLIC | MEDIUM | ARCHIVED | GitHub | Archived historical engineering-standard source; retained for history and verification. |
| ISS-ASSET-006 | `Iron-Signal-Systems/file-intelligence` | Source repository | Engineering Authority | PUBLIC | HIGH | ACTIVE | GitHub | File Intelligence source and engineering history. |
| ISS-ASSET-007 | `Iron-Signal-Systems/module-families` | Engineering / module repository | Engineering Authority | PUBLIC | MEDIUM | ACTIVE | GitHub | Shared module-family source and engineering history. |
| ISS-ASSET-008 | `Iron-Signal-Systems/security-governance` | Governance repository | Governance Authority | PUBLIC | HIGH | ACTIVE | GitHub | Authoritative public organizational-security governance source. |
| ISS-ASSET-009 | Primary ISS development workstation | Development / administrative system | System Owner | RESTRICTED | CRITICAL | ACTIVE | Local controlled system | Used for ISS development, repository administration, and signed Git operations. Host-specific security details are intentionally not published here. |
| ISS-ASSET-010 | GitHub authentication and Git signing authority | Authentication / cryptographic authority | System Owner | RESTRICTED | CRITICAL | ACTIVE | Local protected credential boundary | Private key material and recovery secrets are not recorded in this public register. |
| ISS-ASSET-011 | Local Atlas development PostgreSQL service | Development database service | System Owner | INTERNAL | HIGH | ACTIVE | Local development boundary | Used by Atlas development and validation. This entry does not imply production or customer-data use. |

## Review gaps before implementation

The System Owner shall confirm whether any material assets exist in the
following categories and either add them to the register or record that the
category is currently not used:

- domains and DNS;
- email or collaboration services used for ISS administration;
- backup and recovery targets;
- additional development, build, test, or administrative systems;
- hosted CI/CD or artifact-storage services beyond the GitHub organization
  boundary;
- external identity, credential, or secret-management services;
- hosted databases, cloud services, or virtual machines;
- customer-facing or remotely administered systems;
- code-signing, release-signing, or additional cryptographic authorities not
  already represented by ISS-ASSET-010; and
- other operational dependencies whose loss or compromise would materially
  affect ISS work.

## Maintenance rule

New material assets shall receive a stable `ISS-ASSET-NNN` identifier.

Existing identifiers shall not be reused for different assets after retirement.
Historical entries shall remain reconstructable through signed Git history.
