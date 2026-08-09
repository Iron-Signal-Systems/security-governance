# Privileged Access Review Records

This directory retains non-sensitive records produced by
ISS-IAM-002 — Privileged Access Review.

## Naming

Use:

`YYYY-MM-DD-ISS-IAM-002-<description>.md`

## Required content

Each review record shall identify:

- control ID;
- review date;
- review authority;
- exact repository or governed state reviewed;
- systems and services reviewed;
- privileged identities or authorities observed;
- access decisions;
- findings and required actions;
- related risk-treatment impact;
- next required review date; and
- independence status.

## Sensitive information

Do not commit passwords, private keys, tokens, recovery codes, secret values,
internal administrative addresses, or other restricted authentication details.

Record enough information to identify the governed authority without publishing
the credential.

## Independence

The current solo-project review may be self-review.

Self-review shall not be represented as independent review.

## Authenticity

Review records shall use the normal signed Git workflow.

Signed Git history establishes attribution and repository history. It does not
convert self-review into independent review.
