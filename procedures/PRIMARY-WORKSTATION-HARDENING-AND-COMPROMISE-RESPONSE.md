# Primary Workstation Hardening and Compromise Response

## Purpose

Define a non-secret security and response baseline for the primary Iron Signal
Systems development and administrative workstation.

This procedure supports `ISS-RISK-015`, `ISS-IAM-002`, `ISS-VUL-001`,
`ISS-IR-001`, `ISS-BCP-001`, and applicable `ISS-ENG-001` / ISRAS boundaries.

It does not publish passwords, private keys, passphrases, tokens, recovery
secrets, internal addresses, or other sensitive host-specific detail.

## Current boundary

Iron Signal Systems is currently operated as a solo-developed project.

The primary workstation is used for development, repository administration,
signed Git operations, local recovery administration, and other current ISS
administrative tasks.

No alternate administrator, security team, or independent workstation reviewer
is invented by this procedure.

## Normal security posture

The workstation should maintain, as applicable:

- a supported and intentionally maintained operating-system/package state;
- timely review and treatment of security-relevant operating-system and package
  vulnerabilities under `ISS-VUL-001`;
- normal operation as a non-root user with sudo/root used only for required
  administrative work;
- no routine direct root login;
- key-based remote administration where remote SSH is enabled;
- only intentionally required network-facing services;
- host or upstream filtering appropriate to the current exposure boundary;
- disabled or absent unused network, wireless, and Bluetooth surfaces;
- separate, passphrase-protected GitHub SSH and Git signing authorities;
- local protection of authentication/signing material against repository,
  ordinary cloud-sync, and unintended multi-user exposure;
- trusted package and software acquisition practices;
- controlled unattended physical access; and
- a defined compromise response path.

The exact host configuration may remain protected local supporting state when
publishing it would unnecessarily expose defensive posture.

## Security update and vulnerability relationship

`ISS-VUL-001` remains authoritative for vulnerability identification,
applicability, remediation, mitigation, and verification.

A current workstation treatment review shall not represent a stale scan,
unavailable scanner, or old package state as proof that no vulnerabilities
exist.

A previously triaged finding shall be reevaluated when the affected technical
state materially changes.

## Administrative privilege

Routine engineering work should occur through the normal user account.

sudo/root authority is retained for required system administration, package
maintenance, recovery, and other privileged tasks.

Retained privilege does not mean routine root operation is required or
authorized.

## Network and service exposure

Only services required for the current development or administration boundary
should listen on non-loopback interfaces.

Remote administration should use intentionally protected authentication.

Unused services and interfaces should be disabled rather than left enabled for
possible future convenience.

Filtering may be implemented locally or through an intentionally controlled
upstream boundary where that boundary actually limits exposure.

## Authentication and signing material

GitHub SSH authentication authority and Git signing authority remain separate.

Private authentication/signing material should be passphrase-protected where
supported and should not be committed to repositories or placed in ordinary
cloud-sync storage.

A valid signature or successful SSH authentication does not prove that the
workstation protecting the corresponding private authority is uncompromised.

## Suspected compromise

If the primary workstation is reasonably suspected compromised:

1. Treat the condition as a security incident under `ISS-IR-001`.
2. Isolate the workstation from unnecessary network access when practical.
3. Stop trust-sensitive signing, release acceptance, and repository
   administration from the suspect workstation.
4. Use a separate trusted system or trusted recovery context where practical for
   account security, revocation, and replacement actions.
5. Review GitHub authentication, signing authority, repository history, and
   other privileged authorities that may have been exposed.
6. Revoke or replace affected authentication/signing authorities according to
   their governed procedures.
7. Preserve useful non-secret technical state when doing so does not materially
   delay containment.
8. Rebuild from trusted source when continued trust in the installed system
   cannot be supported.
9. Verify the recovered system, access paths, package state, repository state,
   and replacement authorities before resuming trust-sensitive work.
10. Update applicable risk, vulnerability, incident, access, and continuity
    records.

The disappearance of visible symptoms does not by itself restore trust.

## Recovery relationship

Local snapshots may support recovery from accidental change or local corruption.

They are not automatically a trusted recovery source after system compromise.

Recovery after compromise must consider whether the source being restored could
contain attacker-controlled or otherwise untrusted state.

## Review

Perform a focused workstation treatment review at least when:

- `ISS-RISK-015` is reassessed;
- privileged authority materially changes;
- a material workstation security event occurs;
- the operating-system or network exposure boundary materially changes; or
- vulnerability state materially changes the risk decision.

Self-review shall remain explicitly labeled as self-review where no independent
person participated.

## Validation state

This procedure defines the current hardening and compromise-response baseline.

Creation of the procedure is not a penetration test, independent assessment,
malware-forensics exercise, destructive rebuild, or proof that compromise is
impossible.
