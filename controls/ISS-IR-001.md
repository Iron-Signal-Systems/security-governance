# ISS-IR-001 — Security Incident Response

## Control identity

**Control ID:** ISS-IR-001
**Control:** Security Incident Response
**Status:** Implemented
**Control owner:** Security Authority
**Control operator:** Security Authority / applicable System Owner
**Frequency:** Event-driven + annual exercise

## Objective

Ensure suspected or confirmed security incidents affecting Iron Signal Systems
assets, identities, repositories, information, software, or governed services are
triaged, contained, investigated, recovered from, and closed through a controlled
and reconstructable process.

## Current organizational boundary

Iron Signal Systems is currently operated as a solo-developed project.

This control shall not invent a SOC, incident-response team, on-call rotation,
employees, managers, internal legal department, public-relations function, or a
customer-breach process for customer boundaries that do not yet exist.

The Security Authority and System Owner may currently be the same person.
Self-review is not independent review.

## Event and incident distinction

A `SECURITY_EVENT` is an observed condition requiring possible review.

A `SECURITY_INCIDENT` is an event or set of events that has caused, or is
reasonably suspected to have caused, unauthorized access, loss of control,
material confidentiality/integrity/availability impact, compromise of trusted
authority, or another material security effect.

Unknown facts remain unknown. Uncertainty shall not be converted into a claim
that no incident occurred.

## Scope

This control applies as relevant to:

- unauthorized access or account compromise;
- suspected compromise of authentication, signing, or recovery authority;
- malware or hostile code execution;
- repository, source, release, or build-integrity compromise;
- vulnerability exploitation;
- unauthorized disclosure, alteration, deletion, or loss of governed
  information;
- material security-related service or recoverability impact;
- supplier incidents materially affecting ISS-controlled assets or authority;
- unauthorized domain, DNS, or administrative-email change; and
- loss of control over privileged services, databases, workstations, or recovery
  boundaries.

Routine defects or outages are not automatically security incidents unless
security impact or hostile activity is reasonably suspected.

## Severity

Use one current severity:

- `SEV-1 — CRITICAL`: critical trust/administrative boundary may be compromised,
  severe impact may be uncontrolled, or immediate containment is required.
- `SEV-2 — HIGH`: material compromise with significant but bounded impact.
- `SEV-3 — MEDIUM`: contained or limited material security impact.
- `SEV-4 — LOW`: confirmed low-impact security incident requiring retained
  closure.
- `NON_INCIDENT`: supported triage disposition for an event determined not to be
  an incident.

A suspected compromise of GitHub organization administration, release-signing
authority, or the primary development/admin workstation where protected
authorities may be exposed is normally `SEV-1` until facts support reduction.

## Response states

A governed incident may move through:

`DETECTED` → `TRIAGE` → `CONTAINMENT` → `ERADICATION` → `RECOVERY` →
`MONITORING` → `CLOSED`

A retained event may instead end as `NON_INCIDENT`.

New facts may return the response to an earlier state.

## Triage

Triage shall establish, as available:

- incident/event ID;
- UTC detection time and source;
- affected or potentially affected assets;
- severity;
- known and unknown facts;
- potentially compromised identities/authorities;
- active-threat state;
- immediate containment need;
- continuity/recovery need;
- provider involvement; and
- possible external-notification applicability.

For `SEV-1` and `SEV-2`, containment takes priority over administrative
completeness when delay would materially increase harm.

## Containment

Containment may include isolation, account suspension, credential/key
revocation, access blocking, service disablement, release freeze, repository
authority restriction, or provider containment.

Containment should preserve material technical state when a safer path exists,
but preservation shall not delay urgent action that prevents additional harm.

Where a system is suspected compromised, high-trust recovery actions should use
a separate trusted context where practical.

If no safer context exists and urgent action must use the suspected system, the
decision and limitation shall be recorded.

## Records

Retain enough information to reconstruct material decisions and actions,
including as applicable UTC timestamps, asset IDs, detection source,
administrative actions, relevant logs, useful hashes, access/key actions,
containment/recovery decisions, notification decisions, validation results,
findings, and closure rationale.

Do not commit passwords, private keys, tokens, recovery codes, customer secrets,
or other authentication secrets to the public governance repository.

Sensitive incident material shall be protected separately and may be referenced
by non-sensitive identifier or digest.

Incident records are control records. They are not automatically legal evidence,
forensic evidence, or chain-of-custody records.

## Investigation, eradication, and recovery

Investigation shall determine the practical extent and cause required for safe
recovery.

Eradication may include rebuild from trusted source, patch/configuration change,
credential or key replacement, account/privilege change, dependency replacement,
repository repair through governed history, or provider corrective action.

A system is not trusted merely because the visible symptom disappears.

Recovery shall verify applicable account/privilege state, repository/source
integrity, signing/authentication authority, corrected system state, service
configuration, data integrity, access paths, and follow-up monitoring.

Broader continuity and recovery remain governed by `ISS-BCP-001`.

## External notification

External notification shall be based on an actual contractual, legal,
regulatory, customer, provider, insurer, or other applicable obligation.

No notification duty shall be invented.

The current solo-project baseline has no established customer-information,
customer-production, or remote-support incident-notification boundary. That
state must be reevaluated before such a boundary is introduced.

## Related controls

Incident response may trigger without replacing:

- `ISS-IAM-001` account lifecycle;
- `ISS-IAM-002` privileged access;
- `ISS-VUL-001` vulnerability management;
- `ISS-RSK-001` risk management;
- `ISS-ENG-001` / applicable ISRAS engineering assurance;
- `ISS-BCP-001` continuity/recovery;
- `ISS-SUP-001` supplier security; and
- `ISS-EXC-001` exceptions when applicable.

Closing an incident does not automatically close a related risk, vulnerability,
finding, exception, or engineering action.

## Closure

An incident may be `CLOSED` only when there is a supported basis that active
hostile activity is no longer known to be occurring in the affected boundary,
required containment/eradication is complete or transferred to governed action,
recovery is verified as applicable, findings are recorded, notification
applicability is resolved, and closure rationale is retained.

`SEV-1` and `SEV-2` incidents require post-incident review.

## Annual exercise

Exercise the response process at least annually and after material
response-boundary change.

A tabletop or technical exercise shall identify scenario, assumptions, severity,
triage, containment, eradication, recovery, notification decision,
related-control interaction, limitations, findings, and result.

A tabletop shall not be represented as proof that destructive containment,
credential revocation, provider response, disaster recovery, or external
notification was technically executed.

## Independence

Current exercises and reviews may be self-performed where independence is not
required and shall be labeled accordingly.

AI, automation, alternate accounts, keys, or sessions do not create independent
human review.

## Failure conditions

ISS-IR-001 fails when a known material incident is intentionally omitted,
uncertainty is silently converted to `NON_INCIDENT`, urgent containment is
delayed only for paperwork, secrets are published, recovery is claimed without
verification, material response actions are silently abandoned, notification
obligations are guessed or knowingly ignored, a tabletop is represented as
executed technical containment, or self-review is represented as independent.

## Implementation state

The incident-response policy is active, the incident register exists, and the
initial tabletop exercise `ISS-IR-EX-001` has been completed and retained.

ISS-IR-001 is `Implemented`.

Implementation does not mean a real incident occurred, destructive containment
was tested, every future incident will have the same facts, or independent
review has occurred.
