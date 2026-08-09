# Governance Review Records

This directory retains non-sensitive records produced by
ISS-GOV-001 — Security Governance Review.

## Naming

Use:

`YYYY-MM-DD-ISS-GOV-001-<description>.md`

## Required content

Each review record shall identify:

- control ID;
- review date;
- review trigger;
- authority performing the review;
- repository or governance state reviewed;
- scope reviewed;
- material changes considered;
- findings;
- required actions;
- active exceptions requiring attention;
- result;
- next review date; and
- independence status.

## Independence

A review performed by the same person responsible for the reviewed governance
state is self-review.

It shall not be described as independent review.

## Sensitive information

Credentials, customer-sensitive information, protected operational details, and
other restricted information shall not be committed to this public repository.

A public governance record may reference a protected supporting record without
publishing the sensitive material.

## Authenticity

Governance review records shall use the normal signed Git workflow.

A signed commit establishes repository attribution and history. It does not
convert self-review into independent review.
