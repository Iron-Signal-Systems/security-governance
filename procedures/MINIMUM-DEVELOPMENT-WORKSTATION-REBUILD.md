# Minimum Development Workstation Rebuild

## Purpose

Define the minimum non-secret reconstruction path for the current Iron Signal
Systems development and administrative workstation boundary.

This is a reconstruction procedure. It is not a credential-backup,
private-key-backup, full-system-image, or disaster-recovery claim.

## Minimum reconstruction sequence

1. Build a supported workstation operating-system boundary from a trusted source.
2. Apply current operating-system and package updates.
3. Install only tooling required by the current repository boundary.
4. Configure required storage and host protections.
5. Establish network access required for repository reconstruction.
6. Reestablish GitHub authentication using provider account control and a
   governed existing or replacement authentication authority.
7. Reestablish Git signing using the governed existing or replacement signing
   authority and verify signer trust before trust-sensitive use.
8. Clone required canonical repositories from authoritative remote Git locations.
9. Verify expected branches, commit identities, and signed history where applicable.
10. Restore only non-secret configuration that is actually required.
11. Reconstruct development databases from governed source when classified as reproducible.
12. Run repository-specific validation before resuming trust-sensitive work.

## Boundary

This path does not claim recovery of unpushed Git work, lost local snapshots,
private keys that were not separately recoverable, local-only data not classified
as reproducible or separately backed up, unavailable provider accounts, or any
customer-production state.

A future material workstation, authority, repository, or persistence change
triggers reevaluation.
