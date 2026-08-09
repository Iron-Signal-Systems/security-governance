# ISS-VUL-001 — Vulnerability Identification and Remediation

## Control identity

**Control ID:** ISS-VUL-001
**Control:** Vulnerability Identification and Remediation
**Status:** Implemented
**Control owner:** Security Authority / Engineering Authority
**Control operator:** Security Authority / Engineering Authority
**Frequency:** Continuous identification with risk-based remediation and review

## Objective

Identify applicable vulnerabilities affecting Iron Signal Systems-controlled
systems or governed software, assign accountable disposition, remediate or
mitigate material findings, and verify resolution without duplicating
authoritative engineering-assurance records.

## Authority boundary

ISS-VUL-001 governs organizational vulnerability handling.

Where accepted ISRAS authority governs software-component or vulnerability
history for a repository or release, ISS-VUL-001 shall inherit those
authoritative results rather than create a competing scanner history.

Organizational vulnerability governance may:

- receive an authoritative engineering finding;
- evaluate organizational risk and operational impact;
- assign treatment ownership;
- require remediation, mitigation, or exception handling;
- track organizational target dates; and
- verify that the authoritative engineering disposition is reflected in the
  organizational risk boundary.

ISS-VUL-001 shall not silently override an authoritative ISRAS engineering
decision.

## Current organizational vulnerability boundary

The current ISS-VUL-001 boundary includes, as applicable:

- the primary ISS development and administrative workstation;
- operating-system and installed-package vulnerabilities affecting that system;
- the active local Atlas development PostgreSQL package/software boundary;
- vulnerabilities affecting authentication, signing, recovery, or administrative
  tooling used to operate ISS assets;
- authoritative software vulnerability findings produced by applicable
  engineering controls; and
- newly identified vulnerabilities that materially affect current ISS assets,
  repositories, or trusted dependencies.

Vendor-managed services such as GitHub, Squarespace-managed domain/DNS, and
Gmail are not represented as ISS-scanned infrastructure. Vulnerabilities or
security conditions affecting those services are governed when identified
through provider advisories, incidents, authoritative notifications, or supplier
review.

## Identification sources

Applicable findings may originate from:

- operating-system security advisories;
- package-manager or platform vulnerability data;
- authoritative software-component or dependency scanning;
- ISRAS-controlled vulnerability history;
- source-code security analysis;
- vendor or supplier advisories;
- security incident investigation;
- manual review;
- penetration or security assessment;
- responsible vulnerability reports; or
- other technically credible sources.

A scanner or feed is a source of findings, not the control itself.

## Applicability triage

Scanner, package-manager, feed, or advisory output identifies a candidate
condition. It does not automatically prove that the governed asset is currently
vulnerable.

Before assigning or retaining an applicability-dependent disposition, the
operator shall evaluate the actual technical boundary using information such as:

- authoritative affected-version or fixed-version information;
- installed and running component versions;
- enabled features, drivers, protocols, or services;
- actual exposure and operating state; and
- authoritative supplier or engineering disposition where applicable.

A candidate may be `NOT_APPLICABLE` when a documented technical basis
demonstrates that the governed boundary is outside the affected condition.

Where vulnerable capability exists but is intentionally prevented from operating,
`MITIGATE` / `MITIGATED` may be used when the compensating control is verified.

Continued scanner output after a supported technical disposition does not by
itself invalidate that disposition. The finding shall be reevaluated when the
source data or governed technical state materially changes.

Scanner failure, stale coverage, unavailable data, or unsupported assets shall
be recorded as a coverage limitation and shall not be represented as zero
findings.

## Finding identity

Each material organizational vulnerability finding shall include:

- stable finding identifier;
- affected asset, software, repository, or authority boundary;
- vulnerability or condition description;
- source and source date;
- applicable external identifier when available;
- severity;
- organizational risk context;
- accountable owner;
- disposition;
- target date;
- current status;
- resolution or mitigation description;
- verification status; and
- related risk, control, exception, or authoritative engineering record where
  applicable.

Sensitive exploit or currently exposed package/CVE detail shall not be placed in
the public register when doing so would materially increase risk.

Protected supporting detail may be retained outside Git history and bound to the
public review by cryptographic digest.

## Severity

ISS-VUL-001 uses:

- `CRITICAL`;
- `HIGH`;
- `MEDIUM`;
- `LOW`; or
- `INFORMATIONAL`.

When a credible authoritative source provides severity, that severity may be
used as the starting point.

Organizational risk context may increase urgency based on:

- active exploitation;
- network or administrative exposure;
- privilege required;
- availability of a practical exploit path;
- affected asset criticality;
- presence of authentication/signing authority;
- sensitive information exposure; or
- absence of effective compensating controls.

Organizational context shall not be used merely to suppress an inconvenient
finding.

## Target remediation windows

Unless a stricter engineering, contractual, legal, customer, or risk-treatment
requirement applies, material findings shall have a target resolution or
formally governed exception no later than:

| Severity | Maximum target window |
|---|---:|
| CRITICAL | 7 calendar days |
| HIGH | 30 calendar days |
| MEDIUM | 90 calendar days |
| LOW | 180 calendar days |
| INFORMATIONAL | Review; no mandatory remediation window |

A shorter target shall be assigned where active exploitation, asset criticality,
or current risk warrants it.

If remediation cannot be completed within the applicable window, the finding
shall have a documented mitigation and/or governed exception rather than silently
remaining overdue.

## Disposition

Each reviewed finding shall receive one disposition:

- `REMEDIATE` — remove or correct the vulnerable condition;
- `MITIGATE` — reduce practical exposure while remediation is pending or not
  immediately practical;
- `NOT_APPLICABLE` — technically confirmed not to affect the governed boundary;
- `ACCEPT_WITH_EXCEPTION` — defer remediation through the authorized exception
  process; or
- `PENDING_REVIEW` — insufficient information exists to determine disposition.

`NOT_APPLICABLE` requires a technical basis.

`ACCEPT_WITH_EXCEPTION` is not valid without the required exception record.

## Status

Finding status shall use:

- `IDENTIFIED`;
- `TRIAGE`;
- `REMEDIATION_IN_PROGRESS`;
- `MITIGATED`;
- `RESOLVED`;
- `NOT_APPLICABLE`;
- `EXCEPTED`; or
- `PENDING_REVIEW`.

A finding shall not be marked `RESOLVED` until resolution has been verified.

## Verification

Resolution verification shall confirm, as applicable:

- the affected vulnerable version or condition is no longer present;
- the fixed or mitigated state is actually active;
- relevant tests or authoritative engineering verification completed;
- no required exception remains active; and
- the organizational finding record reflects the final state.

Merely installing an update does not by itself prove that the vulnerable
condition is no longer present when additional activation, restart, migration,
or configuration is required.

## Relationship to risk

Vulnerability findings shall be linked to ISS-RSK-001 where they materially
change an existing risk or create a new material risk.

Resolving one vulnerability does not automatically close a broader risk unless
the risk-producing condition has actually changed enough to justify reassessment.

## Records

The non-sensitive organizational vulnerability register is retained in:

`registers/VULNERABILITY-REGISTER.md`

Review and operating records are retained under:

`records/vulnerability/`

Authoritative engineering records remain in the engineering system that owns
them and may be referenced rather than copied.

Protected local supporting detail may be retained outside Git history. When used,
the public review record shall identify the supporting record type and a
cryptographic digest sufficient to detect later substitution.

## Independence

Routine vulnerability identification, remediation, and verification may be
performed as self-review under the current solo-project baseline where
independent review is not required.

Self-review shall not be represented as independent review.

## Failure conditions

ISS-VUL-001 is not operating as required when:

- a known material finding is intentionally omitted;
- scanner or coverage failure is represented as zero vulnerabilities;
- a material finding has no accountable disposition;
- an overdue Critical, High, Medium, or Low finding has neither justified
  mitigation nor governed exception;
- `NOT_APPLICABLE` is assigned without technical basis;
- a finding is marked `RESOLVED` without verification;
- authoritative ISRAS vulnerability history is silently replaced by a competing
  organizational history; or
- self-review is represented as independent review.

## Implementation state

The initial organizational vulnerability review has been completed for the
current coverage boundary.

Current Arch operating-system/package coverage is operating, material findings
have been assigned stable organizational identifiers, severity, disposition, and
target dates, and known coverage limitations are explicit.

ISS-VUL-001 is `Implemented`.

Implementation does not mean the current vulnerability count is zero, that all
findings are remediated, that all repositories have identical engineering
coverage, or that any independent assessment has occurred.
