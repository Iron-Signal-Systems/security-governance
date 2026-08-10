# Supplier Security Policy

## Purpose

Material external suppliers and hosted services shall be reviewed in proportion
to their actual security, administrative, information, and continuity impact on
Iron Signal Systems.

## Current organizational state

Iron Signal Systems is currently operated as a solo-developed project.

Supplier governance describes a security responsibility and does not imply a
procurement department, legal department, purchasing committee, or formal vendor
management organization.

## Requirements

A material supplier shall be identified and reviewed before material use where
practical, when an existing service becomes material, periodically while in use,
and after material boundary or security change.

The review shall consider the actual ISS dependency, exposed information or
authority, provider security capabilities relevant to current use, recovery and
portability limitations, current risks, and whether use should continue.

Provider-published security statements are provider assertions unless supported
by separately identified independent assurance.

A provider capability shall not be represented as enabled ISS configuration
without verification.

Provider-managed resilience shall not be represented as ISS-controlled recovery.

Current supplier approval shall not be silently extended to future customer,
production, regulated, public-safety, or remote-support use.

## Decisions

Supplier decisions are:

- `CONTINUE_CURRENT_USE`;
- `CONTINUE_WITH_CONDITIONS`;
- `REPLACE`;
- `DO_NOT_USE`;
- `PENDING_REVIEW`; or
- `FUTURE_BOUNDARY`.

A decision applies only to the reviewed service and boundary.

## Records

The supplier register and review records shall retain enough non-sensitive
information to reconstruct the decision and known limitations.

Secrets, recovery codes, private account data, private support communications,
and other sensitive material shall not be published merely as supplier-review
records.
