# ISS-RISK-005 — Dependency and Build-System Treatment Review

## Review identity

**Risk:** ISS-RISK-005
**Review date:** 2026-08-11
**Authority:** Sole project operator acting as Engineering Authority
**Independence:** Self-review; not independent
**Result:** `TREATMENT_PROGRESS_CONFIRMED`

## Prior risk state

**Likelihood:** 2
**Impact:** 3
**Rating:** `HIGH (6)`
**Treatment:** `REDUCE`
**Status:** `OPEN`

ISS-RISK-005 addresses compromise of the current engineering dependency and
build-system boundary.

## Reviewed engineering boundaries

### Atlas

Atlas remains an ISRAS-adopted repository under its exact accepted project pin.

Its committed project declaration includes governed build, formatting, static
analysis, testing, module consistency, module integrity, and known-vulnerability
operations.

A newer accepted ISRAS release does not silently replace the repository's
existing accepted pin.

### File Intelligence

File Intelligence remains an ISRAS-adopted repository under its exact accepted
project pin.

Its committed project declaration includes governed build, formatting, static
analysis, testing, module consistency, module integrity, and known-vulnerability
operations.

A newer accepted ISRAS release does not silently replace the repository's
existing accepted pin.

### Domain Neutral Platform

Domain Neutral Platform remains explicitly not ISRAS-adopted.

`ISS-ENG-ACT-001` remains open and continues to require a separate adoption
topology decision before any ISRAS-adoption claim is made.

The current DNP Go implementation nevertheless contains repository-owned
dependency and build controls including:

- exact Go toolchain enforcement;
- read-only module operation during normal validation;
- gofmt validation;
- go vet;
- complete Go package tests;
- go mod verify;
- an explicit accepted module graph;
- go.mod and go.sum consistency checks;
- reproducible production binary checks; and
- constrained production dependency use.

## Focused dependency review

The focused 2026-08-11 review executed the existing DNP Go validation boundary.

The result was:

**DNP validation:** `29 PASS, 0 FAIL`

The same review executed the exact `govulncheck v1.6.0` scanner version governed
by the currently accepted ISRAS engineering authority.

The initial scan identified one reachable vulnerability:

**Advisory:** `GO-2026-5970`
**Affected selected module:** `golang.org/x/text v0.29.0`
**Reachability:** reachable through the accepted PostgreSQL dependency path

This finding was not treated as a passing or acceptable vulnerability state.

## Technical remediation

The DNP dependency graph was updated to remove the affected selected
`golang.org/x/text v0.29.0` version.

The remediated selected version is:

`golang.org/x/text v0.39.0`

The resulting selected graph also changed:

- `golang.org/x/mod` from v0.27.0 to v0.37.0;
- `golang.org/x/sync` from v0.17.0 to v0.21.0;
- `golang.org/x/tools` from v0.36.0 to v0.47.0.

The direct production dependency `github.com/jackc/pgx/v5 v5.10.0` remains
unchanged.

The remediation was committed and merged to canonical DNP `dev`.

**DNP remediation commit:** `de0134e634dd61a8c794c75ab1dd76c415c655b8`
**DNP merge commit:** `acdfc64e630591a1eef9169c8d1e7a2d2d9ecba8`

Local Git verification reported Good ED25519 signatures for both commits.

GitHub remote verification confirmed the merge commit and intended dependency,
checksum, dependency-record, and exact-module-graph changes on DNP `dev`.

## Post-remediation validation

Following the dependency update:

**DNP validation:** `29 PASS, 0 FAIL`
**govulncheck version:** `v1.6.0`
**govulncheck result:** `No vulnerabilities found`
**govulncheck exit status:** `0`

These results apply to the reviewed DNP Go dependency boundary at the reviewed
repository state.

They do not claim that all future dependencies or all future repository states
are vulnerability-free.

## Treatment conclusion

The review demonstrated that the current dependency/build treatment can detect
a reachable dependency vulnerability, require remediation, preserve exact
dependency history, and revalidate the resulting build and dependency state.

The DNP remediation materially strengthens the current treatment basis for
ISS-RISK-005.

This record does not yet change the risk register rating.

A separate reassessment shall determine the residual likelihood, rating, and
status after this treatment record is committed and accepted.

## Boundaries preserved

This review does not:

- claim zero vulnerabilities across Iron Signal Systems;
- claim DNP is ISRAS-adopted;
- close ISS-ENG-ACT-001;
- force Atlas or File Intelligence to a newer ISRAS release;
- duplicate authoritative ISRAS engineering controls into organizational
  governance;
- claim independent review;
- certify the dependency supply chain;
- eliminate future dependency or build-system compromise risk; or
- close ISS-RISK-005.

## External assurance

This is internal organizational risk treatment and self-review.

It does not claim independent assessment, certification, attestation, or other
external assurance.
