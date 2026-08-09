# ISS-ENG-001 — Initial Engineering Governance Review

## Review identity

**Control ID:** ISS-ENG-001
**Review date:** 2026-08-09
**Review authority:** Sole project operator acting as Engineering Authority
**Independence status:** Self-review; not independent
**Definition commit:** `2672e4964977ad73a80b7a51627a130daa63d2a7`
**Review result:** `PASS_WITH_OPEN_ENGINEERING_ACTION`

## Purpose

This record establishes the initial operating baseline for ISS-ENG-001.

It identifies the current accepted ISRAS authority, classifies the material
repository boundary, records actual consuming-project pins where present, and
retains unsupported or unresolved adoption states without fabricating compliance.

## Accepted Engineering Standards authority

The reviewed post-publication acceptance record identifies:

- accepted release: `isras-v26.08.05`;
- accepted source commit:
  `f375b397a3039d82e96d76f269b444bef16adeb1`; and
- lifecycle status: `ACCEPTED — ACTIVE CALENDAR RELEASE`.

Accepted-source observation SHA-256:

`253900ac0c08dab623f4dd542e564e7faddbb1427fb6667546e9b43bbda0c34a`

The accepted release states that consuming projects already pinned to an earlier
accepted release remain governed by that exact release until a separately
reviewed upgrade changes the pin.

## Accepted adoption-profile boundary

The accepted 26.08.05 project-initialization contract supports first adoption of
the Go profile and explicitly does not implement non-Go initialization.

The accepted initializer requires the exact release mechanism and explicit
`--go-defaults`.

Development source is not adoption authority.

This review therefore does not create dummy Go content or hand-authored `.isras`
artifacts for repositories that do not fit the accepted profile.

## Atlas observation

The canonical Atlas `dev` project pin identifies:

- profile: `ISRAS-SD`;
- version: `26.07.26`;
- release tag: `isras-v26.07.26`;
- source commit:
  `a714436be59c64833c1a6da0dfb3cb32b5d6204b`; and
- project profile: `go`.

Observed project-pin SHA-256:

`a57f6d645610ff57ab8c8c42a62b648f8d3b1f3ba4d57342396b4a932d0be469`

Disposition:

`ADOPTED`

No automatic upgrade to 26.08.05 is claimed.

## File Intelligence observation

The canonical File Intelligence `dev` project pin identifies:

- profile: `ISRAS-SD`;
- version: `26.07.26`;
- release tag: `isras-v26.07.26`;
- source commit:
  `a714436be59c64833c1a6da0dfb3cb32b5d6204b`; and
- project profile: `go`.

Observed project-pin SHA-256:

`f512f43d2a77bfcbf5e6fdc3f4bafc94428f97a5730460f442b09e662a41fa7c`

Disposition:

`ADOPTED`

No automatic upgrade to 26.08.05 is claimed.

## Domain-Neutral Platform observation

Canonical DNP `dev` returned no `.isras/project.json` during the initial review.

Observed project-pin HTTP status:

`404`

A nested Go module exists at:

`go/platform/go.mod`

Observed nested Go-module SHA-256:

`8749f93aaeed8ce98749923ba781a1b3b4d3a79deea3b04b4bc218ab59e7ac77`

Disposition:

`ADOPTION_REVIEW_REQUIRED`

The accepted Go adoption mechanism shall not be applied blindly to a repository
layout that may not satisfy its project-command and root-boundary assumptions.

`ISS-ENG-ACT-001` requires a separate adoption-topology review before DNP is
represented as ISRAS-adopted.

## Module Families observation

Canonical Module Families `dev` returned no `.isras/project.json` and no root
`go.mod` during the initial review.

Observed project-pin HTTP status:

`404`

Observed root Go-module HTTP status:

`404`

Disposition:

`PROFILE_NOT_CURRENTLY_SUPPORTED`

No dummy Go module or hand-authored adoption artifacts are authorized.

## Security Governance observation

The security-governance repository contains no local `.isras/project.json`.

Its repository purpose is organizational governance and documentation.

The accepted 26.08.05 first-adoption boundary does not implement non-Go
initialization.

Disposition:

`PROFILE_NOT_CURRENTLY_SUPPORTED`

`ISRAS-ADOPTION.md` has been corrected to record that truthful state.

## Engineering Standards legacy observation

The legacy Engineering Standards repository is retained as historical source.

Disposition:

`HISTORICAL`

Retired or archived historical source is not treated as current adoption
authority.

## Open action

`ISS-ENG-ACT-001` remains open for DNP.

This does not mean ISS-ENG-001 failed to operate.

The control is operating because the repository state is explicitly classified,
the unresolved adoption topology is visible, and no false adoption claim is made.

## Inheritance boundary

Where Atlas, File Intelligence, or a future repository has a valid accepted ISRAS
project pin, organizational governance may consume the authoritative engineering
result rather than duplicate it.

ISS-ENG-001 does not make an engineering result independent merely because the
result is referenced by organizational governance.

## Independence statement

This review was performed by the same person who authors and administers the
current ISS repositories.

It is self-review and is not represented as independent review.

AI assistance was used to structure the control and inspect public repository
state, but no AI system is represented as an independent reviewer.

## Conclusion

The current material repository engineering-governance boundary has been
classified without inventing adoption.

Atlas and File Intelligence have accepted project pins.

DNP requires a separate adoption-topology review.

Module Families and security-governance remain explicitly non-adopted under the
current accepted profile boundary.

ISS-ENG-001 has completed its initial operating review and is `Implemented` with
one open engineering action.
