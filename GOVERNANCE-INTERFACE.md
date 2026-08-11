# Security Governance Consumption Interface

## Purpose

This document defines how other Iron Signal Systems repositories, including the
Iron Signal Repository Assurance Standard (ISRAS), may consume released
organizational security-governance authority.

It does not make this repository ISRAS-adopted and does not merge organizational
governance authority with ISRAS engineering-assurance authority.

## Authority boundary

`security-governance` is authoritative for organizational security governance,
including organizational control identities, risk state, access governance,
continuity, supplier governance, incident-response governance, vulnerability
governance, awareness, exceptions, and related organizational records.

`engineering-standards` remains authoritative for ISRAS engineering-assurance
requirements, release assurance, project adoption, project-command execution,
repository validation, and software-lifecycle engineering controls.

Neither authority silently rewrites the other.

Where an organizational requirement needs engineering implementation, ISRAS may
map or satisfy that requirement within its own engineering authority. The
organizational control remains defined here; the engineering mechanism remains
defined by ISRAS.

## Release identity

The release version is:

`26.08.11`

The corresponding signed annotated tag is:

`security-governance-v26.08.11`

A consuming repository shall not treat `dev`, another branch name, or an
unverified repository tip as immutable release authority.

A consuming repository that depends on an exact governance release shall record:

- the governance version;
- the signed annotated tag;
- the exact commit selected by that tag; and
- the consuming purpose or mapping.

## Allowed consumption

A consuming repository may use a released governance identity to reference
stable organizational control IDs, map engineering requirements to
organizational controls, identify applicable organizational requirements, or
retain a traceable organizational-governance dependency.

Current operational state remains authoritative in this repository's current
registers when current state matters.

## ISRAS relationship

ISRAS may consume this released governance baseline as an organizational
authority input.

That relationship does not make `security-governance` an ISRAS-adopted project,
allow security governance to bypass or weaken an accepted ISRAS requirement,
allow ISRAS to change organizational risk or control status, make a development
branch an accepted governance release, or create independent/external assurance.

## Change and compatibility rule

Released tags are immutable historical authority.

A consuming repository remains bound to the exact governance release it records
until a separately reviewed change updates that dependency.

Material organizational, legal, customer, production, support, or authority
changes may require a new governance release or an earlier targeted review.
