# Security Incident Response Policy

## Purpose

Iron Signal Systems shall respond to suspected or confirmed security incidents
through a controlled process that prioritizes containment, truthful uncertainty,
safe recovery, and reconstructable decisions.

## Current organizational state

Iron Signal Systems is currently operated as a solo-developed project. Response
responsibilities are governance roles, not an invented SOC, team, legal
department, or on-call organization.

## Requirements

A material security event shall be triaged when it may affect confidentiality,
integrity, availability, authenticity, recoverability, or trusted authority.

The response shall distinguish event from incident, preserve unknown facts as
unknown, assign severity, contain active risk, retain material records without
publishing secrets, investigate/eradicate sufficiently for safe recovery,
verify recovery, resolve notification applicability, update related controls
where required, and retain supported closure.

For critical/high incidents, containment shall not be delayed merely to complete
administrative documentation.

Where a system is suspected compromised, high-trust recovery should use a
separate trusted context where practical. Emergency use of the suspected system
shall be recorded as a limitation.

External notification shall be based on an actual applicable obligation. The
current baseline shall not invent customer or production notification duties.

The response process shall be exercised at least annually and after material
boundary change. A tabletop validates decision flow only; it does not prove
destructive or provider-dependent actions were executed.
