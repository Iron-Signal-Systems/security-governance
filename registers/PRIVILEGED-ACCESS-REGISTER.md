# Privileged Access Register

## Current state

**ISS-IAM-002 status:** `Implemented`  
**Register state:** Operating  
**Initial review:** 2026-08-09  
**Focused treatment review:** 2026-08-10 — GitHub administrative / SSH authority
**Next required review:** 2026-11-09 or earlier upon material privileged-access change

This register intentionally contains no passwords, private keys, tokens, recovery
codes, usernames, or other authentication secrets.

The current solo project operator personally controls the reviewed privileged
authorities. Specific account identifiers are withheld from this public register
where they are not necessary to establish the governance boundary.

## Register

| Access ID | System / authority | Privileged capability | Identity / authority | Current need | Decision | Finding / action | Next review |
|---|---|---|---|---|---|---|---|
| ISS-PRIV-001 | Iron Signal Systems GitHub organization | Organization/repository administration | Individually controlled account of the sole project operator | Administer organization settings and current ISS repositories | RETAIN | Focused 2026-08-10 treatment review completed with remediation required. Detailed negative/unknown state is protected locally. `ISS-RISK-014` remains HIGH and open. | 2026-11-09 |
| ISS-PRIV-002 | GitHub SSH authentication authority | Authenticated repository access using SSH authority | Local protected SSH authority controlled by the sole project operator | Push/pull and authenticated repository administration | RETAIN | Focused 2026-08-10 treatment review completed with remediation required; replacement/revocation procedure is defined but actual recovery was not exercised. | 2026-11-09 |
| ISS-PRIV-003 | Git commit-signing authority | Produce signed Git history under trusted signing identity | Local protected signing authority controlled by the sole project operator | Sign accepted repository history and governance changes | RETAIN | Authority remains necessary. `ISS-RISK-002` remains HIGH and open; signing revocation/recovery treatment is not closed by this review. | 2026-11-09 |
| ISS-PRIV-004 | Primary ISS development workstation | sudo/root system administration | Normal user account with sudo/root elevation for administrative tasks | Install software, update the system, and perform required system administration | RETAIN | Privilege is retained for administrative tasks rather than represented as routine root operation. `ISS-RISK-015` remains HIGH and open. | 2026-11-09 |
| ISS-PRIV-005 | `ironsignalsystems.com` / DNS | Domain and DNS administration | Personally controlled administrative/recovery authority | Maintain the ISS domain and DNS configuration | RETAIN | Authority remains necessary. Administrative and recovery protection remains subject to access and supplier governance. | 2026-11-09 |
| ISS-PRIV-006 | `info@ironsignalsystems.com` | Mailbox administration and account recovery | Personally controlled mailbox/recovery authority | Operate and recover the current ISS administrative/contact mailbox | RETAIN | Authority remains necessary. Mailbox and recovery protection remains subject to access and supplier governance. | 2026-11-09 |
| ISS-PRIV-007 | Local Atlas PostgreSQL development service | PostgreSQL administrative/superuser authority | Personally controlled local database administrative authority | Administer the active Atlas development PostgreSQL service | RETAIN | Administrative authority remains necessary for development administration. This review does not claim that application/runtime use requires superuser authority. | 2026-11-09 |
| ISS-PRIV-008 | `/src` Btrfs/Snapper recovery boundary | Snapshot, deletion, restore, and recovery administration | sudo/root authority controlled by the sole project operator | Administer snapshots and perform required recovery operations | RETAIN | Privilege remains necessary for recovery administration. Backup/recovery adequacy is governed separately. | 2026-11-09 |

## Review result

No currently identified material privileged authority was found to be
unauthorized or unnecessary for the present solo-project operating model.

All eight reviewed authorities receive `RETAIN`.

This does not close the risks associated with concentrated administrative,
authentication, signing, or workstation authority.

## Maintenance rule

New material privileged boundaries shall receive the next stable
`ISS-PRIV-NNN` identifier.

Identifiers shall not be reused.

A material change to privileged authority triggers review before the normal
quarterly date when necessary.
