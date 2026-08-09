# ISS-AST-001 — Information and System Inventory

## Control identity

**Control ID:** ISS-AST-001  
**Control:** Information and System Inventory  
**Status:** Implemented  
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

The System Owner shall review material local systems and external dependencies
not visible from the public repository boundary, including domains, DNS, email,
recovery facilities, administrative services, hosted infrastructure, and other
systems actually in use.

Unknown or unreviewed material categories shall not be silently treated as
absent.

## Records

The authoritative non-sensitive asset inventory is retained in:

`registers/ASSET-REGISTER.md`

Inventory-review records are retained under:

`records/assets/`

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
- an incomplete inventory is knowingly represented as complete.

## Implementation state

The initial material asset and dependency boundary has been reviewed and the
inventory is operating.

ISS-AST-001 is `Implemented`.

Implementation means the inventory is maintained for the current operating
boundary. It does not mean every inventoried asset has completed risk,
supplier-security, continuity, or access-control review under other controls.
