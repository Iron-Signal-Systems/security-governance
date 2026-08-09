# ISS-GOV-001 — Security Governance Review

## Control identity

**Control ID:** ISS-GOV-001  
**Control:** Security Governance Review  
**Status:** Implemented  
**Control owner:** Governance Authority  
**Control operator:** Governance Authority  
**Frequency:** At least annually and after material change

## Objective

Determine whether the Iron Signal Systems organizational security governance
system remains accurate, suitable, effective, and proportional to the actual
operating environment and identified risks.

## Requirement

The Governance Authority shall review the organizational security governance
system:

- at least annually; and
- after a material change affecting the governance boundary.

The review shall determine whether:

- the documented organizational state remains truthful;
- authority assignments remain accurate;
- security policies remain applicable;
- organizational controls remain appropriate;
- required controls are operating or have explicitly recorded deficiencies;
- material security risks are being governed;
- active exceptions remain authorized and bounded;
- organizational governance and ISRAS authority boundaries remain correct;
- material changes require new or modified controls; and
- identified deficiencies have accountable follow-up actions.

## Material-change triggers

Material-change triggers include, as applicable:

- formation of a separate legal entity;
- addition or removal of personnel with material authority;
- material changes to governance or engineering authority;
- introduction of a materially different product or service;
- significant hosting, infrastructure, administrative, or support changes;
- a significant security incident;
- introduction of a materially significant supplier or dependency;
- a material contractual or customer security obligation;
- significant internal or independent review findings; or
- a material change to the Iron Signal Systems engineering-assurance model.

Editorial and formatting changes alone do not require a governance review.

## Review scope

A governance review shall consider, as applicable:

- `GOVERNANCE.md`;
- `SECURITY-POLICY.md`;
- `authorities/AUTHORITY-REGISTER.md`;
- the organizational control catalog;
- applicable policies;
- risk, asset, supplier, and exception registers;
- retained control records;
- known control deficiencies;
- the organizational-governance and ISRAS authority boundary; and
- material changes since the previous review.

ISS-GOV-001 does not replace the risk assessment governed by ISS-RSK-001 or
engineering assurance governed by ISRAS.

## Required review record

Each completed review shall identify:

- control ID;
- review date;
- review trigger;
- Governance Authority performing the review;
- exact repository commit or governed state reviewed;
- scope reviewed;
- material changes considered;
- deficiencies identified;
- required actions;
- active exceptions requiring attention;
- review result;
- next required review date; and
- independence status.

## Review result

A completed review shall record one of:

- `PASS` — the governance system remains suitable and no unresolved governance
  deficiency prevents acceptance of the reviewed state; or
- `ACTION_REQUIRED` — the review completed, but one or more deficiencies require
  tracked corrective action.

A missing required review or missing required record shall not be represented as
`PASS`.

## Independence

Under the current solo operating model, Governance Authority review is
self-review.

It shall not be represented as independent review.

Where independent review becomes required, the reviewer must be a qualified
person independent of the work being assessed.

## Records

Non-sensitive governance review records may be retained under:

`records/governance/`

Sensitive supporting material shall be retained in an appropriately protected
location and referenced without publishing the sensitive content.

Signed Git history establishes attribution and repository history. It does not
establish independent review.

## Failure conditions

ISS-GOV-001 is not operating as required when:

- a required annual review becomes overdue;
- a material-change trigger occurs without the required review;
- the required record is missing;
- self-review is represented as independent review;
- material deficiencies are intentionally omitted; or
- an `ACTION_REQUIRED` result is silently represented as `PASS`.

## Implementation state

The Governance Authority assignment is established and the first governance
review has been completed and retained.

ISS-GOV-001 is `Implemented`.

Implementation does not mean every organizational control is complete, that the
governance system has been independently assessed, or that the initial review
result was `PASS`.
