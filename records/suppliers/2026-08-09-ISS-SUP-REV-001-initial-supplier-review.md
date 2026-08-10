# ISS-SUP-REV-001 — Initial Supplier Security Review

## Review identity

**Control:** ISS-SUP-001
**Review ID:** ISS-SUP-REV-001
**Review date:** 2026-08-09
**Review authority:** Sole project operator acting as Governance Authority / applicable System Owner
**Independence status:** Self-review; not independent
**AI assistance:** Public provider documentation was researched and summarized with AI assistance; this is not independent human review or independent provider assurance
**Definition commit:** `8ae134aae5e82dd196fe0adef0c24acb131e4b94`
**Reviewed asset-register SHA-256:** `8d5104b5987c6afce481ac7b3572805bd37f193175c8cd0e6467a1156633099b`
**Reviewed risk-register SHA-256:** `44552e69b7402c6a66b5d3a657f297423e54783589a62e1fdcff981ac00d2b4e`
**Reviewed continuity-register SHA-256:** `a6b4074514b690656980122a9832e131438225e96401b7c348695af3c7c28347`
**Review result:** `PASS_WITH_OPEN_DEPENDENCY_ACTIONS`
**Next required review:** 2027-08-09 or earlier upon material supplier/boundary change or relevant incident

## Scope

The initial review covers the material hosted-service providers already present
in the current asset boundary:

1. GitHub;
2. Squarespace for domain/DNS; and
3. Google/Gmail for administrative email.

The review does not create a claim that no other software or network dependency
exists.

Software/package engineering dependencies remain governed primarily through
`ISS-ENG-001`, applicable ISRAS requirements, and `ISS-VUL-001` unless they
become a material hosted-service supplier boundary.

## Source handling

The provider materials below were reviewed as public provider documentation.

They are provider assertions or provider documentation unless explicitly stated
otherwise.

This review does not independently audit the providers.

The source URLs are retained so the basis can be reconstructed, but provider
content may change after the review date.

## GitHub

### Current dependency

GitHub hosts the ISS organization and the canonical remote Git history for
current repositories.

The asset register classifies the GitHub organization as CRITICAL.

### Provider documentation reviewed

- GitHub Docs — Keeping your organization secure:
  https://docs.github.com/en/organizations/keeping-your-organization-secure
- GitHub Docs — Requiring two-factor authentication in your organization:
  https://docs.github.com/en/organizations/keeping-your-organization-secure/managing-two-factor-authentication-for-your-organization/requiring-two-factor-authentication-in-your-organization
- GitHub Docs — Reviewing the audit log for your organization:
  https://docs.github.com/en/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/reviewing-the-audit-log-for-your-organization
- GitHub Docs — Accessing compliance reports for your organization:
  https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/accessing-compliance-reports-for-your-organization

### Supported observations

GitHub documents organization security settings, organization-level 2FA
requirements, organization audit logging, and access to provider compliance
reports.

Those capabilities support continued use of GitHub for the present boundary.

This review does not establish which optional GitHub organization security
settings are currently enabled for ISS, and it does not independently validate
GitHub's compliance reports.

### Decision

`CONTINUE_CURRENT_USE`

Current open risks and recovery limitations remain governed separately.

## Squarespace

### Current dependency

Squarespace is the current service boundary for `ironsignalsystems.com` domain
and DNS administration.

The asset register classifies this boundary as HIGH.

### Provider documentation reviewed

- Squarespace Help Center — Protect your account with two-factor authentication:
  https://support.squarespace.com/hc/en-us/articles/360000044827-Protect-your-account-with-two-factor-authentication
- Squarespace Help Center — DNSSEC for Squarespace domains:
  https://support.squarespace.com/hc/en-us/articles/31094668921229-DNSSEC-for-Squarespace-domains
- Squarespace — Security Measures and Safeguards:
  https://www.squarespace.com/measures

### Supported observations

Squarespace documents account 2FA methods including passkeys and recovery codes,
documents DNSSEC behavior for Squarespace-managed domains whose TLD supports
DNSSEC, and publishes security-measures information.

Those capabilities support continued use for the present domain/DNS boundary.

This review does not establish the exact ISS account 2FA/recovery configuration,
does not establish plan-specific assurance, and does not independently validate
Squarespace security controls.

### Decision

`CONTINUE_CURRENT_USE`

Current account-security and recovery-path questions remain governed separately.

## Google / Gmail

### Current dependency

Google/Gmail provides the current ISS administrative/contact email service.

The asset register classifies that boundary as HIGH.

### Provider documentation reviewed

- Google Account Help — Protecting your personal info with 2-Step Verification:
  https://support.google.com/accounts/answer/10956730

### Supported observations

Google documents 2-Step Verification and passkey-based account authentication.

That capability supports continued current use of the Gmail service.

The current account edition, enabled security configuration, recovery
configuration, and any plan-specific compliance capabilities are not established
by this supplier review.

No Workspace-edition or regulated-use claim is made.

### Decision

`CONTINUE_CURRENT_USE`

Current account-security and recovery-path questions remain governed separately.

## Continuity and concentration

The current environment depends materially on external providers for repository
hosting, domain/DNS, and administrative email.

`ISS-BCP-ACT-005` already tracks provider recovery dependencies and practical
alternate/recovery paths for GitHub, Squarespace, and Gmail.

The action remains OPEN.

This review does not duplicate or close it.

## Risk disposition

The review considered current supplier-related risks including
`ISS-RISK-003`, `ISS-RISK-010`, `ISS-RISK-011`, `ISS-RISK-012`, and
`ISS-RISK-014`.

The supplier decisions do not lower, close, or accept those risks.

Risk treatment remains authoritative under `ISS-RSK-001`.

## Future boundary

No current review establishes that GitHub, Squarespace, or Google/Gmail is
approved for future customer information, production, public-safety, CJIS,
payment-card, remote-support, or another regulated/contractual boundary.

Such use requires a new or materially updated review against the actual
requirements, provider service/edition, contracts, data handling, recovery, and
assurance available at that time.

## Result

`PASS_WITH_OPEN_DEPENDENCY_ACTIONS`

All material hosted-service suppliers presently identified in the asset boundary
were reviewed.

Current use may continue.

The review preserved provider/recovery limitations, did not convert provider
features into claims about ISS configuration, did not create independent
assurance, and did not close existing supplier-related risks or continuity
actions.
