# ISS-IR-EX-001 — Initial Security Incident Response Tabletop

## Exercise identity

**Control:** ISS-IR-001
**Exercise ID:** ISS-IR-EX-001
**Exercise date:** 2026-08-09
**Exercise authority:** Sole project operator acting as Security Authority / System Owner
**Exercise type:** Tabletop
**Independence status:** Self-review; not independent
**Definition commit:** `52dd6b27770fc90bcfc6679b518145eda65e4537`
**Reviewed risk-register SHA-256:** `44552e69b7402c6a66b5d3a657f297423e54783589a62e1fdcff981ac00d2b4e`
**Exercise result:** `PASS_WITH_DOCUMENTED_LIMITATIONS`
**Next required exercise:** 2027-08-09 or earlier after material response-boundary change

## Scenario

Assume the primary ISS development/admin workstation shows credible indicators
of hostile compromise.

Assume compromise time is unknown and GitHub SSH authentication authority and Git
signing authority may have been exposed.

It is unknown whether GitHub administration, repository refs/history, signing
authority, authentication authority, local development data, or persistence were
affected.

No real compromise is asserted.

## Related current risks

This scenario exercises:

- `ISS-RISK-002` — release-signing authority compromise;
- `ISS-RISK-014` — GitHub organization administrative compromise; and
- `ISS-RISK-015` — primary development/admin workstation compromise.

The tabletop does not close or reduce those risks.

## Severity

Initial severity: `SEV-1 — CRITICAL`.

Multiple critical trust and administrative authorities may be affected, so
severity remains critical until facts support reduction.

## Triage

Expected triage establishes UTC detection time, trigger observation, workstation
network state, active-threat indication, potentially exposed authorities,
known-good repository/reference boundaries, availability of a separate trusted
administrative context, provider-side activity, affected assets, unknowns, and
immediate containment decisions.

Lack of an obvious GitHub change does not prove the workstation or keys were not
compromised.

## Containment

Expected containment:

1. stop ordinary development/admin use of the suspected workstation;
2. isolate/disconnect it where safe;
3. stop treating authentication/signing authority available from it as trusted;
4. use a separate trusted context for high-trust recovery where practical;
5. revoke, replace, or suspend exposed authority when supported by facts;
6. stop releases or trusted-history promotion while signing/repository integrity
   is uncertain; and
7. retain enough system/provider state to reconstruct the response without
   delaying urgent containment.

If no separate trusted context is available, that limitation is recorded before
using the suspected system for emergency recovery.

## Repository integrity

From a trusted context where practical, review provider administrative changes,
unexpected access/key changes, branch/ref movement, releases/tags, unexpected
commits, known signed acceptance boundaries, local/remote history, and any trusted
decision depending on signatures after the earliest plausible compromise time.

A cryptographically valid signature is not automatically trustworthy if the
signing authority may itself have been compromised.

No real provider change or key revocation was performed in this tabletop.

## Eradication and recovery

A real response would determine whether trusted rebuild is required; remove
persistence or rebuild; fully update/harden; replace exposed authorities as
warranted; review privileged state; verify source/repository integrity; review
local development data; restore only required services/access; and retain
unresolved questions as governed findings.

Before trusted use resumes, verify workstation/admin state, GitHub authority,
repository refs/history, replacement and revoked authorities where applicable,
privileged-access state, corrected vulnerability/configuration state, and
follow-up monitoring.

Broader restoration remains governed by `ISS-BCP-001`.

## Notification

Tabletop disposition:
`NOT_APPLICABLE_TO_CURRENT_CUSTOMER_BOUNDARY`.

The current governance baseline has no customer-information, customer-production,
or remote-support incident boundary.

Provider support may be needed depending on real facts. A real incident must
identify applicable contractual, provider, legal, or regulatory requirements
before claiming notification complete or unnecessary.

No legal/regulatory conclusion is created by this tabletop.

## Related controls

A real scenario could trigger `ISS-IAM-001`, `ISS-IAM-002`, `ISS-VUL-001`,
`ISS-RSK-001`, `ISS-ENG-001` / ISRAS, `ISS-BCP-001`, and `ISS-SUP-001`.

Those authoritative records would be referenced rather than duplicated.

## Closure test

Reinstalling the workstation alone is insufficient.

Closure requires supported containment, exposed-authority handling,
repository/source integrity understanding, verified administrative recovery,
recorded unresolved findings, resolved notification applicability, and a
post-incident review.

## Limitations

This was a tabletop.

It did not actually isolate a workstation, revoke a credential/key, execute a
GitHub emergency workflow, perform destructive malware removal, validate an
alternate clean administrative device, restore backups, test customer
notification, or contact law enforcement, insurers, legal counsel, or
regulators.

These limitations are not hidden by the result.

## Findings and result

No contradiction was identified between the defined response process and the
current organizational/risk boundary.

The exercise provides no basis to claim alternate clean-device recovery, provider
emergency response, destructive containment, backup restoration, or external
notification has been technically validated.

Result: `PASS_WITH_DOCUMENTED_LIMITATIONS`.

The next exercise is required by 2027-08-09 or earlier after material
incident-response-boundary change.
