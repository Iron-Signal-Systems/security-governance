# Asset Register

## Purpose

This register identifies material Iron Signal Systems information systems,
repositories, services, credentials, infrastructure, and operational
dependencies.

The register intentionally records only non-sensitive information suitable for
the public governance repository. Private keys, tokens, internal addresses,
recovery secrets, and similarly sensitive values are not recorded here.

## Current completeness state

**State:** Operating inventory  
**ISS-AST-001 status:** `Implemented`  
**Last inventory review:** 2026-08-09  
**Next required review:** 2027-08-09 or earlier upon material change

The current material asset boundary was reviewed for the present solo-project
operating state.

No additional material Iron Signal Systems development or administrative
machines were identified beyond the primary development workstation.

New material assets and dependencies shall be added when introduced.

## Inventory

| Asset ID | Asset | Type | Owner | Classification | Criticality | State | Canonical location / boundary | Notes |
|---|---|---|---|---|---|---|---|---|
| ISS-ASSET-001 | Iron Signal Systems GitHub organization | Hosted development / administrative service | System Owner | CONFIDENTIAL | CRITICAL | ACTIVE | `github.com/Iron-Signal-Systems` | Canonical organization boundary for current ISS repositories; administrative credentials are not recorded here. |
| ISS-ASSET-002 | `Iron-Signal-Systems/atlas` | Source repository | Engineering Authority | PUBLIC | HIGH | ACTIVE | GitHub | Atlas source and engineering history. |
| ISS-ASSET-003 | `Iron-Signal-Systems/domain-neutral-platform` | Source repository | Engineering Authority | PUBLIC | HIGH | ACTIVE | GitHub | Product/platform source and engineering history. |
| ISS-ASSET-004 | `Iron-Signal-Systems/engineering-standards` | Engineering-standard repository | Engineering Authority | PUBLIC | CRITICAL | ACTIVE | GitHub | Authoritative ISRAS source and accepted engineering-standard history. |
| ISS-ASSET-005 | `Iron-Signal-Systems/engineering-standards-legacy` | Historical repository | Engineering Authority | PUBLIC | MEDIUM | ARCHIVED | GitHub | Archived historical engineering-standard source retained for history and verification. |
| ISS-ASSET-006 | `Iron-Signal-Systems/file-intelligence` | Source repository | Engineering Authority | PUBLIC | HIGH | ACTIVE | GitHub | File Intelligence source and engineering history. |
| ISS-ASSET-007 | `Iron-Signal-Systems/module-families` | Engineering / module repository | Engineering Authority | PUBLIC | MEDIUM | ACTIVE | GitHub | Shared module-family source and engineering history. |
| ISS-ASSET-008 | `Iron-Signal-Systems/security-governance` | Governance repository | Governance Authority | PUBLIC | HIGH | ACTIVE | GitHub | Authoritative public organizational-security governance source. |
| ISS-ASSET-009 | Primary ISS development workstation | Development / administrative system | System Owner | RESTRICTED | CRITICAL | ACTIVE | Local controlled system | Used for ISS development, repository administration, and signed Git operations. Host-specific security details are intentionally not published here. |
| ISS-ASSET-010 | GitHub SSH authentication authority | Authentication authority | System Owner | RESTRICTED | CRITICAL | ACTIVE | Local protected credential boundary | Used for authenticated GitHub repository access. Private key material and recovery secrets are not recorded here. |
| ISS-ASSET-011 | Git commit-signing authority | Cryptographic signing authority | Engineering Authority | RESTRICTED | CRITICAL | ACTIVE | Local protected credential boundary | Used for signed Git history. Signing-key material is not recorded here. |
| ISS-ASSET-012 | Local Atlas development PostgreSQL service | Development database service | System Owner | INTERNAL | HIGH | ACTIVE | Local development boundary | Actively used by Atlas development and validation. This entry does not imply production or customer-data use. |
| ISS-ASSET-013 | `ironsignalsystems.com` domain and DNS service | External domain / DNS service | System Owner | PUBLIC | HIGH | ACTIVE | Squarespace-managed service boundary | Public ISS domain and DNS dependency. Administrative credentials are not recorded here. |
| ISS-ASSET-014 | `info@ironsignalsystems.com` Gmail service | External email service | System Owner | CONFIDENTIAL | HIGH | ACTIVE | Gmail service boundary | Current ISS administrative/contact email service. Mailbox credentials and recovery data are not recorded here. |
| ISS-ASSET-015 | `/src` local snapshot and recovery boundary | Local recovery storage | System Owner | CONFIDENTIAL | HIGH | ACTIVE | Btrfs RAID1 with Snapper | Provides local point-in-time protection for source/work. This is not represented as an independent off-host backup against complete host/storage loss. |

## Boundary review

The initial inventory review considered:

- the current GitHub organization and repositories;
- the primary development and administrative workstation;
- GitHub SSH authentication authority;
- Git commit-signing authority;
- the active Atlas development PostgreSQL service;
- the `ironsignalsystems.com` domain and DNS service;
- the `info@ironsignalsystems.com` Gmail service;
- the current local `/src` snapshot/recovery boundary; and
- whether additional material ISS development or administrative machines are
  currently in use.

No additional material development or administrative machines were identified.

The adequacy of backup durability, recovery objectives, supplier security,
access-control operation, or risk treatment is governed separately and is not
implied by inclusion in this inventory.

## Maintenance rule

New material assets shall receive a stable `ISS-ASSET-NNN` identifier.

Existing identifiers shall not be reused for different assets after retirement.
Historical entries shall remain reconstructable through signed Git history.
