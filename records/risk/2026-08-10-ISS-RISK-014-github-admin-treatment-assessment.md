# ISS-RISK-014 — GitHub Administrative Authority Treatment Assessment

## Assessment identity

**Risk:** ISS-RISK-014
**Assessment date:** 2026-08-10
**Assessment UTC:** `2026-08-11T08:27:03Z`
**Assessment authority:** Sole project operator acting as Security Authority
**Independence:** Self-review; not independent
**Reviewed base commit:** `2791862473dc1bc7878d2999ebf66650d985b76f`
**Protected supporting-state SHA-256:** `f6229cae7f03687e8dc0847236b2aa6f2ba9bdf987448817977a0e7414570754`
**Result:** `ASSESSMENT_COMPLETE`

## Purpose

Perform a focused current-state review of the controls that reduce the
likelihood of compromise of the Iron Signal Systems GitHub organization
administrative authority.

The detailed yes/no/unknown responses are retained only in protected local
supporting state and are not committed to the public repository.

No password, private key, token, recovery code, passkey secret, authenticator
secret, or similar authentication material is recorded.

## Reviewed categories

The assessment reviewed personal-account 2FA, organization 2FA enforcement,
secure-method enforcement, authentication/recovery diversity, protected recovery
material, recovery-path understanding, SSH-key inventory and local protection,
personal-access-token and application authorization inventory, organization
access inventory, organization audit activity, and the security/recovery email
path.

## Treatment model

A focused likelihood reduction is supported only when every required category is
affirmatively confirmed.

If any required category is `NO` or `UNKNOWN`, `ISS-RISK-014` remains High and
open. Detailed deficiency state remains protected locally.

If every required category is `YES`, the treatment review may reduce likelihood
from 2 to 1 while impact remains 3, producing a residual Medium rating of 3.
The risk remains under `REDUCE` treatment and moves to monitoring rather than
being closed.

## Recovery/revocation procedure

A non-secret GitHub administrative-authority recovery/revocation procedure is
defined in:

`procedures/GITHUB-ADMINISTRATIVE-AUTHORITY-RECOVERY.md`

Creating the procedure does not claim that destructive account or SSH recovery
was exercised.

## Relationship to other controls

This assessment informs `ISS-IAM-002`, `ISS-BCP-001`, `ISS-IR-001`, and
`ISS-SUP-001`.

It does not automatically close `ISS-BCP-ACT-005`, other GitHub-related risks,
or any unrelated open action.

## Public/private boundary

The public record contains scope, method, digest, and governance decision.
Detailed categorical responses remain protected locally because publishing
negative security posture is unnecessary to operate the control.
