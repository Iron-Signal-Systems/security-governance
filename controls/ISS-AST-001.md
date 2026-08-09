# ISS-AST-001 — Information and System Inventory

## Control identity

**Control ID:** ISS-AST-001  
**Control:** Information and System Inventory  
**Status:** Defined  
**Control owner:** System Owner  
**Control operator:** System Owner  
**Frequency:** Continuous maintenance and at least annual review

## Objective

Maintain an accurate inventory of material information systems, repositories,
services, credentials, infrastructure, and operational dependencies used to
develop, govern, secure, operate, or recover work conducted under the Iron
Signal Systems name.

## Requirement

The System Owner shall maintain an inventory sufficient to identify material
assets and dependencies that require security, recovery, access, supplier, or
risk-management decisions.

The inventory shall include, as applicable:

- source and governance repositories;
- repository-hosting and organization boundaries;
- development and administrative systems;
- material databases and data stores;
- authentication, signing, and cryptographic authority;
- material hosted services and external dependencies;
- backup and recovery locations;
- domains, DNS, email, and other identity or communications services;
- deployment, test, or production infrastructure; and
- other assets whose loss, compromise, unavailability, or unauthorized change
  could materially affect Iron Signal Systems work.

## Inventory fields

Each inventory entry shall identify, as applicable:

- stable asset identifier;
- asset or service name;
- asset type;
- accountable owner;
- information classification;
- criticality;
- lifecycle state;
- authoritative or canonical location;
- material dependency or recovery notes; and
- date or basis of the most recent review.

Sensitive values such as private keys, passwords, tokens, recovery codes,
customer secrets, internal addresses, or protected system details shall not be
placed in the public register merely to prove the asset exists.

## Classification

Information classifications shall use the values defined by the Iron Signal
Systems Information Classification Policy:

- `PUBLIC`;
- `INTERNAL`;
- `CONFIDENTIAL`; or
- `RESTRICTED`.

Where an asset processes multiple classifications, the register should identify
the highest material classification relevant to its protection requirements.

## Criticality

Criticality shall use:

- `CRITICAL` — compromise or loss could prevent trustworthy engineering,
  governance, release authority, or recovery;
- `HIGH` — compromise or loss could materially disrupt development, security,
  product integrity, or important operations;
- `MEDIUM` — important to normal operation but recoverable without material
  long-term impact; or
- `LOW` — limited operational or security effect.

Criticality is an organizational prioritization value and is not itself a risk
score.

## Lifecycle state

Lifecycle state shall use one of:

- `ACTIVE`;
- `ARCHIVED`;
- `RETIRED`; or
- `PENDING_REVIEW`.

An archived asset remains governed when it retains historical, recovery,
security, contractual, or engineering value.

## Maintenance

The inventory shall be updated when:

- a material asset or dependency is introduced;
- ownership materially changes;
- classification or criticality changes;
- an asset is archived or retired;
- a material hosting, recovery, or authority boundary changes; or
- review identifies a missing or inaccurate entry.

The complete inventory shall be reviewed at least annually.

## Completeness

An inventory is not complete merely because known repositories are listed.

Before ISS-AST-001 may transition to `Implemented`, the System Owner shall review
the inventory for material local systems and external dependencies not visible
from the public repository boundary, including domains, DNS, email, backups,
administrative services, and other infrastructure actually in use.

Unknown or unreviewed material categories shall not be silently treated as
absent.

## Records

The authoritative non-sensitive asset inventory is retained in:

`registers/ASSET-REGISTER.md`

Sensitive supporting details may be retained outside the public repository in an
appropriately protected location.

## Independence

Asset inventory maintenance is an operational control and does not require
independent review under the current baseline.

A self-review shall not be represented as independent review.

## Failure conditions

ISS-AST-001 is not operating as required when:

- a known material asset is intentionally omitted;
- an asset is materially misclassified in a way that weakens required
  protection;
- a retired or transferred asset remains represented as active;
- the annual review becomes overdue;
- sensitive asset secrets are published merely to demonstrate inventory
  completeness; or
- an incomplete inventory is represented as complete.

## Implementation state

This document defines the control.

The current asset register contains an initial substantiated inventory, but
ISS-AST-001 remains `Defined` until the System Owner confirms that the material
asset and dependency boundary has been reviewed for completeness and the initial
inventory review is retained.
