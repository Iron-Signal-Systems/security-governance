# Privileged Access Register

## Current state

**ISS-IAM-002 status:** `Defined`  
**Register state:** Initial privileged boundaries identified; first formal review pending  
**Prepared:** 2026-08-09

This register intentionally contains no passwords, private keys, tokens, recovery
codes, or other authentication secrets.

The entries identify privileged boundaries that must be reviewed. Exact account
identifiers shall be added only where doing so is appropriate for the public
governance repository.

## Register

| Access ID | System / authority | Privileged capability | Identity / authority | Current need | Decision | Finding / action | Next review |
|---|---|---|---|---|---|---|---|
| ISS-PRIV-001 | Iron Signal Systems GitHub organization | Organization/repository administration | PENDING_REVIEW | PENDING_REVIEW | PENDING_REVIEW | Confirm current administrative identity, recovery path, and minimum required organization authority. | PENDING_REVIEW |
| ISS-PRIV-002 | GitHub SSH authentication authority | Authenticated repository access using SSH authority | Local protected SSH authority; secret not recorded | PENDING_REVIEW | PENDING_REVIEW | Confirm authorized use, custody, and revocation/recovery path. | PENDING_REVIEW |
| ISS-PRIV-003 | Git commit-signing authority | Produce signed Git history under trusted signing identity | Local protected signing authority; secret not recorded | PENDING_REVIEW | PENDING_REVIEW | Confirm authorized signing scope, custody, and revocation/recovery path. | PENDING_REVIEW |
| ISS-PRIV-004 | Primary ISS development workstation | Root/sudo and system administration | PENDING_REVIEW | PENDING_REVIEW | PENDING_REVIEW | Confirm current administrative identity, privilege path, and necessity. | PENDING_REVIEW |
| ISS-PRIV-005 | `ironsignalsystems.com` / DNS | Domain and DNS administration | PENDING_REVIEW | PENDING_REVIEW | PENDING_REVIEW | Confirm current administrative and recovery authority for the Squarespace-managed boundary. | PENDING_REVIEW |
| ISS-PRIV-006 | `info@ironsignalsystems.com` | Mailbox administration and account recovery | PENDING_REVIEW | PENDING_REVIEW | PENDING_REVIEW | Confirm current mailbox/recovery authority and whether broader account administration exists. | PENDING_REVIEW |
| ISS-PRIV-007 | Local Atlas PostgreSQL development service | Database administration | PENDING_REVIEW | PENDING_REVIEW | PENDING_REVIEW | Confirm current PostgreSQL administrative role(s), scope, and operational need. | PENDING_REVIEW |
| ISS-PRIV-008 | `/src` Btrfs/Snapper recovery boundary | Snapshot, deletion, restore, and recovery administration | PENDING_REVIEW | PENDING_REVIEW | PENDING_REVIEW | Confirm current privileged identity and minimum required recovery authority. | PENDING_REVIEW |

## Review rule

During the first formal review, each `PENDING_REVIEW` field shall be resolved
from the actual operating state.

If a listed boundary does not provide a distinct privileged account or role, the
review shall record the actual authority model rather than inventing one.

New material privileged boundaries shall receive the next stable
`ISS-PRIV-NNN` identifier.

Identifiers shall not be reused.
