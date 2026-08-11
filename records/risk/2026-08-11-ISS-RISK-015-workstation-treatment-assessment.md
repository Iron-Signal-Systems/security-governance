# ISS-RISK-015 — Primary Workstation Treatment Assessment

## Assessment identity

**Risk:** ISS-RISK-015
**Assessment date:** 2026-08-11
**Assessment UTC:** `2026-08-11T09:48:07Z`
**Assessment authority:** Sole project operator acting as Security Authority
**Independence:** Self-review; not independent
**Reviewed base commit:** `3b7f46236bc07bda307fe110696f273b9cee884f`
**Protected supporting-state SHA-256:** `50a95651fcceda3fda4dbeaa0eb7fcfc6738046bfa9b642a3f79e1b598525871`
**Current HEAD signature verification:** `PASS`
**Result:** `ASSESSMENT_COMPLETE`

## Purpose

Perform a focused current-state review of controls reducing the likelihood that
the primary ISS development and administrative workstation is compromised or
misused.

Detailed yes/no/unknown responses are retained only in protected local
supporting state and are not committed to the public governance repository.

No passwords, private keys, passphrases, tokens, key paths, fingerprints,
internal addresses, or other secret authentication material are recorded in the
public record.

## Reviewed categories

The assessment reviewed:

- current operating-system and security-relevant package maintenance;
- current vulnerability treatment state;
- non-root routine operation and bounded administrative privilege;
- root-login posture;
- remote-administration authentication;
- network-facing service minimization;
- filtering of inbound exposure;
- disabled or absent unused network/wireless/Bluetooth surfaces;
- protection and separation of GitHub SSH and Git signing authorities;
- protection of local secret material from repository/cloud-sync/unintended
  local-user exposure;
- trusted software/package acquisition;
- unattended physical access; and
- compromise containment/rebuild readiness.

## Treatment model

A focused likelihood reduction is supported only when every required
operator-confirmed category is `YES` and current HEAD signature verification
passes.

If any required category is `NO` or `UNKNOWN`, `ISS-RISK-015` remains High and
open. Detailed deficiency state remains protected locally.

If every required category is `YES`, the treatment review may reduce likelihood
from 2 to 1 while impact remains 3, producing a residual Medium rating of 3.

The risk is not closed. It remains under `REDUCE` treatment and moves to
monitoring.

A Medium result does not mean the workstation cannot be compromised.

## Related governance

The assessment relies on but does not replace:

- `ISS-IAM-002` for privileged access;
- `ISS-VUL-001` for vulnerability handling;
- `ISS-IR-001` for incident response;
- `ISS-BCP-001` for recovery; and
- applicable `ISS-ENG-001` / ISRAS engineering requirements.

## Public/private boundary

The public record contains the assessment scope, method, digest, and resulting
governance decision.

Detailed host-security responses remain protected locally because publishing
negative or host-specific defensive state is unnecessary to operate the control.
