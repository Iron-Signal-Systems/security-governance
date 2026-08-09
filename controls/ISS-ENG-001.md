# ISS-ENG-001 — Govern Software Engineering Through ISRAS

## Control identity

**Control ID:** ISS-ENG-001
**Control:** Govern Software Engineering Through ISRAS
**Status:** Implemented
**Control owner:** Engineering Authority
**Control operator:** Engineering Authority
**Frequency:** Continuous and upon repository, accepted-release, adoption, upgrade, or engineering-boundary change

## Objective

Ensure Iron Signal Systems software repositories are governed through the
authoritative Iron Signal Repository Assurance Standard (ISRAS) where an
accepted ISRAS profile applies, while preserving truthful boundaries for
repositories that are not yet adopted or are not supported by the currently
accepted adoption profile.

## Organizational and engineering authority

Organizational security governance establishes that ISRAS is the authoritative
engineering standard for Iron Signal Systems repositories.

ISS-ENG-001 does not copy ISRAS requirements into organizational governance.

Where ISRAS authoritatively governs repository, source, testing, validation,
component, vulnerability, change, acceptance, release, deployment-verification,
recovery, historical-verification, or other engineering-assurance behavior,
organizational governance shall inherit the applicable ISRAS result instead of
creating a competing authoritative control.

## Accepted-release authority

A branch, repository tip, source version, draft, development build, or published
release does not by itself establish ISRAS adoption authority.

For organizational engineering governance, an ISRAS release may be treated as
accepted authority only when its governing lifecycle establishes the exact
accepted release identity, including the applicable signed source, signed release
tag, published release artifacts, and post-publication acceptance record.

A project remains governed by its exact accepted project pin until a separately
reviewed and accepted upgrade changes that pin.

Publication of a newer ISRAS release does not silently upgrade an existing
project.

## Project adoption

Where an accepted ISRAS profile supports a repository, adoption shall occur only
through the adoption mechanism authorized by that exact accepted release.

A repository shall not be represented as ISRAS-adopted merely because it:

- follows similar engineering practices;
- copies ISRAS documentation;
- runs some ISRAS-like checks;
- references Engineering Standards;
- has signed Git history; or
- is owned by Iron Signal Systems.

A valid adoption claim requires the exact project-owned artifacts and
verification state required by the accepted release.

## Unsupported or non-adopted repositories

A repository that is not currently supported by an accepted ISRAS adoption
profile shall remain explicitly non-adopted.

The Engineering Authority shall not create dummy source, a fake language module,
hand-authored adoption artifacts, or other artificial content merely to force a
repository into an unsupported profile.

A non-adopted repository may still be governed by organizational controls and
repository-specific engineering rules.

Its non-adopted state shall be recorded until:

- an accepted ISRAS profile supports the repository;
- the repository legitimately changes into a supported engineering boundary; or
- a separate governed decision establishes that ISRAS adoption is not applicable
  to that repository.

## Development-source boundary

Development branches of Engineering Standards may propose future profiles,
schemas, tools, or adoption methods.

Development source is not accepted project-adoption authority merely because it
contains a capability that would be useful to a consuming repository.

A consuming repository shall not use unaccepted development source to claim
accepted ISRAS adoption.

## Repository classifications

Each material Iron Signal Systems repository shall receive one current
engineering-governance classification:

- `AUTHORITY_SOURCE` — the repository is the authoritative Engineering Standards
  source rather than a consuming project;
- `ADOPTED` — the repository has a current project pin to an accepted ISRAS
  release;
- `ADOPTION_REVIEW_REQUIRED` — the repository has an engineering boundary that
  may be eligible for an accepted profile but its adoption topology or migration
  requires deliberate review;
- `PROFILE_NOT_CURRENTLY_SUPPORTED` — the repository does not fit an accepted
  adoption profile and shall not fake adoption;
- `NOT_APPLICABLE` — a governed decision establishes that consuming-project
  adoption does not apply;
- `HISTORICAL` — the repository is retained as historical or archived material;
  or
- `PENDING_REVIEW` — insufficient information exists to classify the repository.

`PENDING_REVIEW` shall not be used to conceal a known adoption gap.

## Inheritance of ISRAS results

Where a project is validly ISRAS-adopted, ISS-ENG-001 may consume authoritative
ISRAS results including:

- repository validation state;
- project-pin identity;
- test and static-analysis results;
- known-vulnerability results;
- release and acceptance state;
- exception state;
- provenance and artifact verification;
- deployment-verification results; and
- other results the accepted ISRAS release makes authoritative.

Organizational governance may create organizational risk, access, supplier,
incident, continuity, or other records in response to an ISRAS result without
replacing the engineering result itself.

## Engineering findings and actions

A material engineering-governance gap shall identify:

- stable finding or action identifier;
- affected repository;
- observed condition;
- required decision or treatment;
- accountable authority;
- trigger or target condition; and
- current status.

An open engineering action does not invalidate the operation of ISS-ENG-001 when
the gap is truthfully recorded and controlled.

## Change triggers

ISS-ENG-001 shall be reevaluated when:

- a new material repository is created;
- a repository materially changes technology or layout;
- a repository is adopted into ISRAS;
- an ISRAS project pin is upgraded or replaced;
- a new ISRAS release becomes accepted authority;
- a previously unsupported profile becomes accepted;
- a repository is archived or retired;
- a project claims a new engineering-assurance status; or
- another material engineering-governance boundary changes.

## Required control records

The non-sensitive current repository engineering-governance state is retained in:

`registers/ENGINEERING-GOVERNANCE-REGISTER.md`

Operating review records are retained under:

`records/engineering/`

A record shall identify the accepted Engineering Standards authority used for the
review, the observed project-pin state, open adoption actions, and the
independence status of the review.

## Independence

ISS-ENG-001 is an organizational engineering-governance control.

Under the current solo-project baseline, the Engineering Authority may review
their own repositories and project pins.

That review is self-review and shall not be represented as independent review.

AI systems, automation, alternate accounts, separate keys, or separate sessions
do not create independent human review.

ISRAS itself may also be self-authored and self-validated. ISS-ENG-001 shall not
upgrade that assurance status into independent assurance.

## Failure conditions

ISS-ENG-001 is not operating as required when:

- a repository is represented as ISRAS-adopted without the required accepted
  project pin and adoption state;
- an unaccepted Engineering Standards development branch is treated as adoption
  authority;
- a newer release is silently treated as having upgraded a consuming project;
- dummy language content or hand-authored adoption artifacts are created merely
  to force an unsupported repository into a profile;
- a material repository is knowingly omitted from engineering-governance review;
- an open adoption or engineering-governance gap is concealed;
- organizational governance replaces an authoritative ISRAS engineering result
  with a competing record; or
- self-review is represented as independent review.

## Implementation state

The initial repository engineering-governance review has been completed for the
current material repository boundary.

The current accepted ISRAS authority, consuming-project pin state, unsupported
profile boundaries, and open adoption review action are retained in the
engineering-governance register and initial review record.

ISS-ENG-001 is `Implemented`.

Implementation does not mean every repository is ISRAS-adopted, that every
repository must immediately upgrade to the newest accepted release, that open
engineering actions are closed, or that independent review has occurred.
