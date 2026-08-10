# ISS-SUP-001 — Supplier Security Review

## Control identity

**Control ID:** ISS-SUP-001
**Control:** Supplier Security Review
**Status:** Implemented
**Control owner:** Governance Authority
**Control operator:** Governance Authority / applicable System Owner or Security Authority
**Frequency:** Before material use + periodic review + material change

## Objective

Ensure material external services and suppliers used by Iron Signal Systems are
identified, reviewed in proportion to their security and continuity impact, and
retained only with a supported understanding of dependency, security capability,
recovery limitation, and current risk.

## Current organizational boundary

Iron Signal Systems is currently operated as a solo-developed project.

This control does not invent a procurement department, legal department, vendor
management office, purchasing committee, employee approval chain, or contractual
authority that does not exist.

The current supplier boundary is limited to material providers actually used by
the present development and administrative environment.

Software packages and engineering dependencies remain governed primarily through
`ISS-ENG-001`, applicable ISRAS requirements, and `ISS-VUL-001` unless a package,
registry, hosted build service, or other dependency becomes a material external
service requiring supplier review.

## Material supplier

A supplier or external service is material when loss, compromise, misuse, or
unacceptable change could materially affect confidentiality, integrity,
availability, authenticity, recoverability, administrative authority, source
history, public identity, or another governed ISS boundary.

Materiality is based on the actual dependency, not on whether money is paid to
the provider.

A free service can be material.

## Review triggers

A material supplier shall be reviewed:

- before first material use where practical;
- when an existing service first becomes material;
- at least annually while classified HIGH or CRITICAL;
- after material service, ownership, security, recovery, contractual, or
  processing-boundary change;
- after a material supplier security incident or credible advisory affecting ISS;
- before introducing materially more sensitive information or authority; and
- before a future customer, production, regulated, or remote-support boundary
  relies on the supplier in a way not covered by the current review.

The current initial review may occur after adoption because the suppliers already
exist in the pre-control operating boundary.

## Review dimensions

The review shall consider, as applicable:

- provider/service identity;
- ISS assets and functions dependent on the provider;
- information or authority exposed to the provider boundary;
- criticality and concentration risk;
- authentication and administrative security capabilities;
- logging, monitoring, or administrative-review capabilities;
- public security, privacy, assurance, or compliance information relevant to the
  actual use;
- incident/security reporting paths;
- recovery, export, portability, replacement, or alternate-path limitations;
- material subcontractor or platform dependency when known and relevant;
- current ISS risk-register entries;
- related continuity and access-control records;
- known gaps and uncertainty; and
- current use decision.

The control does not require collection of every possible provider certification,
marketing statement, contract term, or audit report when those items are not
material to the present boundary.

## Source quality

Supplier review may use provider documentation, provider trust/security
materials, contractual materials, public advisories, independent assurance
reports where available, authoritative government or standards information, and
ISS operating observations.

A provider's own security statement is a provider assertion.

It shall not be represented as independent assurance performed by ISS.

Missing, inaccessible, stale, contradictory, or plan-specific information shall
remain a limitation rather than being silently assumed favorable.

## Use decisions

Use one current supplier decision:

- `CONTINUE_CURRENT_USE` — current use remains supported within the reviewed
  boundary;
- `CONTINUE_WITH_CONDITIONS` — current use may continue subject to explicit
  controls or actions;
- `REPLACE` — transition away from the provider is required;
- `DO_NOT_USE` — material use is not authorized;
- `PENDING_REVIEW` — the information required for a supported decision is not
  yet sufficient; or
- `FUTURE_BOUNDARY` — a foreseeable use exists but is not current.

A decision applies only to the reviewed boundary.

`CONTINUE_CURRENT_USE` is not a claim that the supplier is risk-free, certified
for every future requirement, or appropriate for customer/regulated data that
has not yet been introduced.

## Provider security versus ISS configuration

A provider capability is not the same as an enabled ISS configuration.

For example, provider support for multifactor authentication, passkeys, audit
logs, recovery methods, DNSSEC, encryption, or compliance reports does not prove
that the applicable ISS account, plan, domain, or organization has enabled or
validated that capability.

ISS account configuration and privileged access remain governed by
`ISS-IAM-001` and `ISS-IAM-002`.

Recovery and alternate-path validation remain governed by `ISS-BCP-001`.

## Continuity and concentration

Supplier review shall identify material dependence on hosted providers.

Provider-managed resilience shall not be represented as an ISS-controlled
recovery capability.

Where supplier outage, account loss, or provider unavailability could materially
interrupt ISS work, the relevant recovery or alternate-path decision shall be
tracked under `ISS-BCP-001` or another applicable control.

## Security incidents

A supplier incident that may materially affect an ISS asset, identity,
information boundary, or trusted authority shall be evaluated under
`ISS-IR-001`.

A public provider incident does not automatically establish that ISS was
affected.

Likewise, absence of a public provider incident does not prove that a specific
ISS account or authority was not compromised.

## Future customer and regulated boundaries

The current supplier review does not establish suitability for future
customer-information, customer-production, public-safety, CJIS, payment-card,
remote-support, or other regulated/contractual use.

Before such a boundary relies materially on an external provider, applicable
security, contractual, data-location, support, recovery, notification,
subprocessor, retention, and assurance requirements shall be reviewed for the
actual service edition and use.

No future compliance status shall be inferred from a provider's general
marketing or certification statements.

## Records

The supplier register shall retain:

- stable supplier ID;
- provider/service;
- affected ISS assets or functions;
- criticality;
- review date;
- reviewed source categories;
- supported security observations;
- dependency/recovery limitations;
- related risks or controls;
- use decision;
- open action or referenced action where applicable; and
- next review trigger/date.

Secrets, private account details, recovery codes, billing data, private support
communications, or other sensitive information shall not be published merely to
populate the register.

## Independence

Current supplier reviews may be self-performed where independent review is not
required.

They shall be labeled as self-review.

AI-assisted research or summarization does not create independent human review.

Alternate accounts, keys, sessions, or automation do not create independent
review.

## Failure conditions

ISS-SUP-001 is not operating as required when:

- a known material supplier is intentionally omitted;
- provider marketing is represented as independent ISS assurance;
- provider capability is represented as enabled ISS configuration without
  verification;
- a supplier decision is silently extended to a materially different future
  boundary;
- material provider outage/recovery dependence is concealed;
- a known material supplier incident affecting ISS is ignored;
- supplier use continues after a `REPLACE` or `DO_NOT_USE` decision without an
  applicable governed exception;
- secrets are published as supplier-review records; or
- self-review is represented as independent review.

## Related controls

Supplier review interacts with:

- `ISS-AST-001` for current material assets;
- `ISS-RSK-001` for supplier and concentration risks;
- `ISS-IAM-001` and `ISS-IAM-002` for account/access configuration;
- `ISS-ENG-001` / applicable ISRAS for engineering dependencies;
- `ISS-VUL-001` for vulnerability management;
- `ISS-IR-001` for supplier-related incidents;
- `ISS-BCP-001` for recovery and alternate paths; and
- `ISS-EXC-001` where an applicable mandatory requirement cannot be met.

## Implementation state

The supplier-security policy is active.

The current material hosted-service boundary has been reviewed and recorded in
the supplier register.

Initial review `ISS-SUP-REV-001` is retained with result
`PASS_WITH_OPEN_DEPENDENCY_ACTIONS`.

ISS-SUP-001 is `Implemented`.

Implementation does not establish that every provider capability is enabled in
the applicable ISS account, that provider recovery has been technically
validated, or that the current suppliers are suitable for future customer or
regulated boundaries.
