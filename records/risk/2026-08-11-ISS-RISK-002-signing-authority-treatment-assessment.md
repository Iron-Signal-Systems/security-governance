# ISS-RISK-002 — Signing Authority Treatment Assessment

## Assessment identity

**Risk:** ISS-RISK-002
**Assessment date:** 2026-08-11
**Assessment UTC:** `2026-08-11T09:31:13Z`
**Assessment authority:** Sole project operator acting as Engineering Authority
**Independence:** Self-review; not independent
**Reviewed base commit:** `603c9279df6d76d0e4a6616cc7586a914cb8b530`
**Protected supporting-state SHA-256:** `b86b7109441bdd292abda2a91249184d31d8e3fcc4abfbe75e62a0dc2a8fefea`
**Current HEAD signature verification:** `PASS`
**Result:** `ASSESSMENT_COMPLETE`

## Purpose

Perform a focused current-state review of controls reducing the likelihood that
the current Git commit-signing authority is compromised or misused.

Detailed yes/no/unknown responses are retained only in protected local supporting
state and are not committed to the public governance repository.

No private key, passphrase, key path, fingerprint, recovery secret, or other
secret authentication material is recorded in the public record.

## Reviewed categories

The assessment reviewed signing/authentication separation, signing-key
passphrase protection, intentional system custody, exclusion from repository and
ordinary cloud-sync storage, duplicate-key review, restricted local access,
deliberate operator involvement in signing, public-identity recognition,
verification of current signed Git history, and compromise/transition readiness.

## Treatment model

A focused likelihood reduction is supported only when every required
operator-confirmed category is `YES` and current HEAD signature verification
passes.

If any required category is `NO` or `UNKNOWN`, `ISS-RISK-002` remains High and
open. Detailed deficiency state remains protected locally.

If every required category is `YES`, the treatment review may reduce likelihood
from 2 to 1 while impact remains 3, producing a residual Medium rating of 3.

The risk is not closed. It remains under `REDUCE` treatment and moves to
monitoring.

`ISS-RISK-015` remains independent and is not lowered by this assessment.

## Revocation and transition procedure

A non-secret signing-authority revocation/replacement/transition procedure is
defined in:

`procedures/SIGNING-AUTHORITY-REVOCATION-AND-TRANSITION.md`

Creating the procedure does not claim that a real compromise, loss, rotation, or
replacement was exercised.

## Public/private boundary

The public record contains the assessment scope, method, digest, and resulting
governance decision.

Detailed categorical responses remain protected locally because publishing
negative security posture is unnecessary to operate the control.
