# ISS-RSK-001 — Security Risk Assessment and Register

## Control identity

**Control ID:** ISS-RSK-001  
**Control:** Security Risk Assessment and Register  
**Status:** Defined  
**Control owner:** Security Authority  
**Control operator:** Security Authority  
**Frequency:** At least quarterly and after material change

## Objective

Identify, evaluate, assign, treat, and review material security and operational
risks affecting work conducted under the Iron Signal Systems name.

## Requirement

The Security Authority shall maintain a risk process that:

- identifies material risks from the actual operating boundary;
- records each risk using a stable identifier;
- identifies the affected asset, service, authority, or operating boundary;
- assigns an accountable risk owner;
- assesses likelihood and impact using the approved risk model;
- derives the current overall risk rating deterministically;
- records a treatment decision;
- identifies related controls or treatment actions;
- records a target date when treatment is required;
- records a next-review date;
- tracks current risk status; and
- retains review records sufficient to reconstruct material risk decisions.

## Sources of risk

Risk identification shall consider, as applicable:

- the ISS asset inventory;
- governance-review findings;
- engineering-assurance results;
- material vulnerabilities;
- incidents and near misses;
- supplier and hosted-service dependencies;
- authentication and signing authority;
- recovery and continuity limitations;
- architecture and deployment changes;
- customer or contractual obligations; and
- newly understood threats or failure modes.

Absence from the current register does not make a newly discovered material risk
non-governed.

## Risk model

ISS-RSK-001 uses a three-level likelihood scale and a three-level impact scale.

### Likelihood

`1 — UNLIKELY`

The event is not expected under current conditions and would normally require
unusual circumstances, multiple failures, or a low-probability path.

`2 — POSSIBLE`

A credible path exists under current conditions and occurrence is reasonably
plausible.

`3 — LIKELY`

The event is expected, recurring, has occurred materially before, or the current
exposure makes occurrence substantially more probable.

### Impact

`1 — LIMITED`

Impact is localized and recoverable with limited disruption and no material loss
of engineering trust, governance authority, protected information, or important
service capability.

`2 — MATERIAL`

Impact could cause meaningful compromise, disruption, loss, or remediation work
but remains recoverable without severe or sustained organizational harm.

`3 — SEVERE`

Impact could materially undermine release or engineering trust, compromise
critical authority or sensitive information, cause sustained inability to
operate or recover, or create severe customer, contractual, legal, or security
consequences.

### Score

Risk score is:

`likelihood × impact`

The derived rating is:

| Score | Rating |
|---:|---|
| 1–2 | LOW |
| 3–4 | MEDIUM |
| 6 | HIGH |
| 9 | CRITICAL |

No other numeric score is possible under this model.

If the available facts reasonably support two adjacent levels and the ambiguity
cannot yet be resolved, the higher level shall be used until the uncertainty is
resolved.

## Treatment

Permitted treatment decisions are:

- `AVOID`;
- `REDUCE`;
- `TRANSFER`;
- `ACCEPT`; or
- `DISCONTINUE`.

A treatment decision shall describe what is actually being done or why no
additional treatment is required.

High and Critical risks shall not remain without either:

- an active treatment plan and accountable target date; or
- explicit Governance Authority acceptance.

Risk acceptance does not waive an otherwise mandatory control. Any required
control deviation must be governed separately through the applicable exception
process.

## Risk ownership

The risk owner is accountable for ensuring the risk is reviewed and that the
recorded treatment remains appropriate.

The risk owner may be a governance role such as:

- Governance Authority;
- Security Authority;
- Engineering Authority; or
- System Owner.

The same person may currently occupy multiple roles. Role concentration does not
create independent review.

## Risk status

Risk status shall use one of:

- `IDENTIFIED` — risk is recorded but the initial assessment is not yet complete;
- `OPEN` — risk is assessed and requires continued governance;
- `TREATMENT_IN_PROGRESS` — active treatment work is underway;
- `ACCEPTED` — residual risk has been explicitly accepted by the authorized
  Governance Authority;
- `MONITORING` — no immediate treatment work is required, but the risk remains
  subject to periodic review; or
- `CLOSED` — the risk-producing condition no longer materially exists.

A risk shall not be marked `CLOSED` merely because treatment work was completed.
The remaining condition must no longer constitute a material governed risk.

## Review triggers

The risk register shall be reviewed:

- at least quarterly;
- after a material security incident;
- after a material architecture or deployment change;
- after a significant supplier or dependency change;
- after identification of a significant vulnerability or control deficiency;
- after a material organizational or authority change;
- when the asset inventory materially changes; and
- when new customer, contractual, or legal security obligations materially alter
  the risk boundary.

## Required review record

Each risk review shall identify:

- review date;
- review authority;
- exact governed state reviewed;
- risks added, removed, or materially changed;
- likelihood and impact decisions;
- treatment decisions;
- accepted risks;
- overdue actions;
- next required review date; and
- independence status.

## Records

The authoritative non-sensitive risk register is retained in:

`registers/RISK-REGISTER.md`

Risk-review records are retained under:

`records/risk/`

Sensitive supporting details may be retained in a protected location and
referenced without publishing them.

## Independence

Risk assessment under the current solo-project baseline may be self-review.

Self-review shall not be represented as independent review.

If a contract, assessment, future policy, or other obligation requires
independent risk review, a qualified independent person must perform that
function.

## Failure conditions

ISS-RSK-001 is not operating as required when:

- a known material risk is intentionally omitted;
- likelihood or impact is manipulated to reduce the derived rating;
- a risk is represented as assessed without an actual assessment;
- a High or Critical risk has neither active treatment nor explicit authorized
  acceptance;
- an acceptance is used to bypass a mandatory control without the required
  exception;
- a required quarterly or material-change review becomes overdue;
- an overdue treatment action is silently omitted; or
- self-review is represented as independent review.

## Implementation state

This document defines ISS-RSK-001 and its deterministic risk model.

The current register contains identified risks awaiting the first formal risk
assessment.

ISS-RSK-001 shall remain `Defined` until:

1. the initial risk review is performed;
2. material risks have accountable owners;
3. likelihood and impact are assessed;
4. derived ratings and treatment decisions are recorded;
5. required target and next-review dates are established; and
6. the review record and machine-readable control state are updated
   consistently.
