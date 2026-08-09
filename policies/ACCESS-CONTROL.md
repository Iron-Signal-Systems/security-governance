# Access Control Policy

## Principles

- Access requires an authorized operational or governance need.
- Privilege shall be limited to the minimum practical authority.
- Administrative access shall use individually attributable identities where supported.
- Shared credentials and shared human accounts shall be avoided; when unavoidable, their use and custody shall be explicitly controlled.
- Non-human identities shall have a defined purpose and accountable owner.
- Authentication secrets shall not be committed to source repositories.
- Access shall be removed promptly when no longer required.
- Completed removal or disablement shall be verified.
- Privileged access shall be reviewed at least quarterly.
- Production and release authority shall be separated where independence is required and qualified personnel exist.

## Provisioning

New material access requires authorization by the applicable System Owner or
Governance Authority before access is provided.

Provisioned access shall be limited to the minimum practical authority required
for the approved purpose.

## Change

Material account or authorization changes require reevaluation when the operating
purpose, system, role, authority, service state, or security condition changes.

## Removal

Access shall be disabled or removed after loss of operational need, role change,
departure where personnel later exist, service retirement, credential or account
compromise, or another material authorization change.

Removal shall not be represented as complete until the disabled or removed state
has been verified.

## Non-human and shared identities

Service and automation identities shall have a defined purpose and accountable
owner.

Shared human accounts shall be avoided. Where technically unavoidable, their
authorization and custody shall be explicitly recorded without publishing the
secret.

## Review records

Account-lifecycle records shall identify the governed system, account or identity
record, authorization decision, action, verification result, date, and unresolved
finding where applicable.

Privileged-access reviews shall identify the systems reviewed, accounts or
authorities observed, authority retained or removed, reviewer, date, and
unresolved findings.
