# ISS-BCP-001 — Business Continuity and Recovery

## Control identity

**Control ID:** ISS-BCP-001
**Control:** Business Continuity and Recovery
**Status:** Implemented
**Control owner:** Governance Authority
**Control operator:** Governance Authority / applicable System Owner
**Frequency:** Annual + material change
**Exercise frequency:** At least annually and after material recovery-boundary change

## Objective

Ensure material Iron Signal Systems assets, repositories, authorities, and
operational dependencies have truthful continuity and recovery requirements,
known recovery sources, known limitations, and exercised recovery procedures
proportionate to the current operating boundary.

## Current organizational boundary

Iron Signal Systems is currently operated as a solo-developed project.

There is currently no customer-production, customer-information, or
customer-critical operated-service boundary established by this governance
baseline.

This control therefore shall not invent customer service-level commitments,
production RTO/RPO values, a disaster-recovery site, a recovery team, alternate
personnel who do not exist, a validated off-host backup that does not exist, or
provider failover that has not been tested.

The current ISS project may pause if the sole operator is unavailable. That
limitation must be reevaluated before future obligations make uninterrupted
continuation necessary.

## Recovery classifications

A material recovery boundary may be classified as:

- `REMOTE_RECONSTRUCTABLE`;
- `LOCAL_RECOVERY_ONLY`;
- `REBUILD_REQUIRED`;
- `REPLACEMENT_REQUIRED`;
- `PROVIDER_MANAGED`;
- `REQUIREMENT_REVIEW_REQUIRED`;
- `FUTURE_BOUNDARY`; or
- `NOT_APPLICABLE`.

The classification shall describe what is actually recoverable and shall not
overstate a capability.

## Recovery objectives

Recovery requirements shall be proportionate to real operating impact.

Where a material boundary requires a recovery-time objective (`RTO`) or
recovery-point objective (`RPO`), the value shall be based on actual operational,
contractual, customer, safety, or business need.

No RTO or RPO shall be invented merely to populate a governance record.

Before a future customer-production or customer-critical service is activated,
applicable recovery objectives shall be defined and validated.

## Backup and reconstruction boundary

A backup, replica, snapshot, remote repository, or provider copy is not treated
as equivalent merely because it contains similar data.

A local snapshot in the same host/storage failure domain is not an independent
off-host backup against complete loss of that domain.

GitHub remote repository history is an off-host reconstruction source for Git
objects that were actually pushed and retained remotely.

It is not represented as recovery for unpushed work, local-only databases,
local-only configuration, local snapshots, private keys, or other state not
retained in the remote repository.

## Source and repository recovery

Where GitHub is the authoritative remote repository, recovery may include
cloning the canonical repository, verifying expected refs or accepted
boundaries, verifying signed history where applicable, comparing known commit
identities, validating object integrity, and restoring local development state
from authoritative remote history.

A successful clone does not prove provider availability under every outage
scenario, administrative-account recovery, or recovery of unpushed work.

## Workstation and local-state recovery

Loss of the primary development/admin workstation is a material continuity event
because it currently contains or provides access to development, administrative,
signing, authentication, and local recovery boundaries.

Recovery shall distinguish replacement workstation construction, repository
reconstruction, local-only work, development databases, system configuration,
authentication authority, signing authority, and local snapshots.

The existence of Btrfs RAID1 or Snapper does not establish recovery from complete
host/storage loss.

## Authentication and signing authority

Private authentication or signing secrets shall not be copied into the public
governance repository as a recovery mechanism.

Recovery may instead require provider account recovery, revocation of lost or
compromised authority, generation and authorization of replacement keys,
governed signing-authority transition, and verification of trusted history
affected by an authority-loss event.

## Local development database recovery

The local Atlas PostgreSQL service is a development boundary and does not imply
production or customer data.

Its required persistence and restore capability shall be explicitly determined.

If the database contains only reproducible development state, governed
reconstruction may be sufficient.

If material non-reproducible state must survive complete host loss, an
appropriate backup and restore mechanism shall be defined and exercised.

## Supplier-dependent recovery

GitHub, domain/DNS, Gmail, and other material hosted services may provide their
own resilience and recovery capabilities.

ISS-BCP-001 shall not represent provider-managed resilience as an ISS-controlled
or independently validated recovery capability unless actually validated.

Supplier recovery and alternate-path requirements may be governed jointly with
`ISS-SUP-001`.

## Sole-operator continuity

The current project has no alternate internal operator.

The governance repository, signed engineering history, asset/risk records, and
other reconstructable records reduce loss of institutional context but do not
create another authorized human operator.

Before future customer, production, support, legal, contractual, or
public-safety obligations require continuation during sole-operator
unavailability, an appropriate continuity path shall be established.

No succession, escrow, or alternate-authority arrangement shall be represented
as existing before it actually exists.

## Exercises

Material recovery procedures shall be exercised at least annually and after a
material recovery-boundary change.

An exercise may be technical, tabletop, or combined.

The record shall distinguish actions actually executed from actions only
discussed.

A successful partial recovery test shall not be represented as full disaster
recovery.

## Related controls

Continuity and recovery may consume or trigger `ISS-AST-001`, `ISS-RSK-001`,
`ISS-IAM-001`, `ISS-IAM-002`, `ISS-IR-001`, `ISS-ENG-001` / applicable ISRAS,
`ISS-SUP-001`, and `ISS-EXC-001` where applicable.

ISS-BCP-001 does not silently close a risk merely because a continuity procedure
exists.

## Independence

Current continuity review and exercises may be self-performed where independent
review is not required and shall be labeled as self-review.

AI, automation, alternate accounts, keys, or sessions do not create independent
human review.

## Failure conditions

ISS-BCP-001 is not operating as required when local snapshots are represented as
independent off-host backup without support, GitHub is represented as containing
unpushed/local-only state, a backup is represented as recoverable without a
supported restore basis, customer/production objectives are invented for a
boundary that does not exist, provider resilience is represented as
ISS-controlled recovery without support, a partial exercise is represented as
complete disaster recovery, sole-operator limitations are concealed, material
recovery gaps are omitted, or self-review is represented as independent.

## Implementation state

The continuity policy is active.

The current material recovery boundary has been classified in the continuity and
recovery register.

Initial exercise `ISS-BCP-EX-001` completed a read-only remote Git reconstruction
test and retained the current limitations and open recovery actions.

ISS-BCP-001 is `Implemented`.

Implementation does not mean complete workstation recovery, independent off-host
backup, database restore, credential recovery, supplier failover, or
sole-operator succession has been fully validated.
