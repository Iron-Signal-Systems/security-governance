# Engineering Governance Register

## Current state

**ISS-ENG-001 status:** `Implemented`
**Register state:** Operating
**Initial review:** 2026-08-09
**Review result:** `PASS_WITH_OPEN_ENGINEERING_ACTION`
**Current accepted ISRAS release:** `isras-v26.08.05`
**Accepted ISRAS source commit:** `f375b397a3039d82e96d76f269b444bef16adeb1`

A newer accepted ISRAS release does not silently change an existing consuming
project pin.

Repositories remain governed by their exact accepted project pin until a
separately reviewed upgrade changes that pin.

## Repository register

| Engineering ID | Repository | Asset | Classification | Current ISRAS / engineering state | Governance disposition |
|---|---|---|---|---|---|
| ISS-ENG-REP-001 | `Iron-Signal-Systems/engineering-standards` | ISS-ASSET-004 | AUTHORITY_SOURCE | Accepted active Engineering Standards release is `isras-v26.08.05` at source commit `f375b397a3039d82e96d76f269b444bef16adeb1`. | This repository is the authority source, not a consuming project pin. |
| ISS-ENG-REP-002 | `Iron-Signal-Systems/atlas` | ISS-ASSET-002 | ADOPTED | Canonical `dev` contains an ISRAS Go project pin to `isras-v26.07.26`, source commit `a714436be59c64833c1a6da0dfb3cb32b5d6204b`. | Retain exact accepted pin until a separately reviewed project upgrade occurs. A newer accepted release does not silently upgrade Atlas. |
| ISS-ENG-REP-003 | `Iron-Signal-Systems/file-intelligence` | ISS-ASSET-006 | ADOPTED | Canonical `dev` contains an ISRAS Go project pin to `isras-v26.07.26`, source commit `a714436be59c64833c1a6da0dfb3cb32b5d6204b`. | Retain exact accepted pin until a separately reviewed project upgrade occurs. |
| ISS-ENG-REP-004 | `Iron-Signal-Systems/domain-neutral-platform` | ISS-ASSET-003 | ADOPTION_REVIEW_REQUIRED | No `.isras/project.json` is present on canonical `dev`. The repository contains an active nested Go module at `go/platform/go.mod`. | Do not claim ISRAS adoption. Complete `ISS-ENG-ACT-001` before any new claim that DNP is ISRAS-adopted. |
| ISS-ENG-REP-005 | `Iron-Signal-Systems/module-families` | ISS-ASSET-007 | PROFILE_NOT_CURRENTLY_SUPPORTED | No `.isras/project.json` or root `go.mod` is present on canonical `dev` in the initial review. Current accepted first-adoption authority is Go-profile only. | Do not fake Go content or hand-author adoption. Reevaluate when an accepted suitable profile exists or the repository boundary legitimately changes. |
| ISS-ENG-REP-006 | `Iron-Signal-Systems/security-governance` | ISS-ASSET-008 | PROFILE_NOT_CURRENTLY_SUPPORTED | No project pin is present. The repository is an organizational governance/documentation boundary, while accepted 26.08.05 first adoption supports Go repositories only. | Remain explicitly non-adopted. `ISRAS-ADOPTION.md` records the boundary. |
| ISS-ENG-REP-007 | `Iron-Signal-Systems/engineering-standards-legacy` | ISS-ASSET-005 | HISTORICAL | Archived historical Engineering Standards source. | Retain for history; do not treat retired historical source as current adoption authority. |

## Open engineering actions

| Action ID | Repository | Condition | Required treatment | Owner | Trigger / target | Status |
|---|---|---|---|---|---|---|
| ISS-ENG-ACT-001 | `Iron-Signal-Systems/domain-neutral-platform` | Active Go implementation exists but no current ISRAS project pin is present on canonical `dev`. The Go module is nested rather than rooted at the repository top level. | Perform a separate adoption-topology review against an exact accepted ISRAS release. Adopt only if the supported profile can truthfully govern the repository as it exists; otherwise retain an explicit non-adopted state until an accepted suitable profile or governed migration exists. | Engineering Authority | Before any claim that DNP is ISRAS-adopted, and before any organizational release requirement that mandates an adopted ISRAS project boundary. | OPEN |

## No forced upgrade finding

Atlas and File Intelligence remain pinned to accepted `isras-v26.07.26`.

The existence of accepted `isras-v26.08.05` does not itself create an overdue
upgrade finding.

An upgrade becomes a governed project change only when separately proposed,
reviewed, validated, and accepted.

## Inherited engineering results

Where a repository is `ADOPTED`, ISS-ENG-001 may consume authoritative ISRAS
validation, vulnerability, release, provenance, exception, and related
engineering-assurance results.

Those results are not duplicated here.

Organizational controls may create separate organizational records when an
engineering result changes risk, access, supplier, incident, continuity, or
other organizational state.

## Maintenance rule

New material repository boundaries shall receive the next stable:

`ISS-ENG-REP-NNN`

identifier.

New engineering-governance actions shall receive the next stable:

`ISS-ENG-ACT-NNN`

identifier.

Identifiers shall not be reused.

A repository, project-pin, accepted-release, profile, archive, or material
engineering-boundary change triggers reevaluation.
