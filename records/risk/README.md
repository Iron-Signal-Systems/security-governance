# Risk Review Records

This directory retains non-sensitive records produced by
ISS-RSK-001 — Security Risk Assessment and Register.

## Naming

Use:

`YYYY-MM-DD-ISS-RSK-001-<description>.md`

## Required content

Each review record shall identify:

- control ID;
- review date;
- review authority;
- exact repository or governed state reviewed;
- risks added, removed, or materially changed;
- likelihood and impact decisions;
- derived risk ratings;
- treatment decisions;
- explicit risk acceptances;
- treatment target dates;
- overdue actions;
- next required review date; and
- independence status.

## Sensitive information

Do not commit credentials, private keys, customer-sensitive information,
protected operational details, or other restricted information merely to
support a risk assessment.

A public risk-review record may reference protected supporting material without
publishing the protected content.

## Independence

Risk review may currently be self-review.

Self-review shall not be described as independent review.

## Authenticity

Risk-review records shall use the normal signed Git workflow.

Signed Git history establishes repository attribution and history. It does not
convert self-review into independent review.
