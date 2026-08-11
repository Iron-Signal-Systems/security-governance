# GitHub Administrative Authority Recovery and Revocation Procedure

## Purpose

Define a non-secret, reconstructable response path for compromise, suspected
compromise, or loss of the GitHub administrative and SSH authentication
authority used by the current Iron Signal Systems solo-project boundary.

This procedure supports `ISS-RISK-014`, `ISS-IAM-002`, `ISS-IR-001`, and
`ISS-BCP-001`.

It does not publish credentials, private keys, recovery codes, account
identifiers, or other authentication secrets.

## Current boundary

Iron Signal Systems is currently operated as a solo-developed project.

The current GitHub organization administrative authority and GitHub SSH
authentication authority are controlled by the sole project operator.

No alternate internal operator is invented by this procedure.

## Normal security posture

The current administrative boundary should maintain, as applicable:

- two-factor authentication on the controlling GitHub personal account;
- organization-level two-factor authentication enforcement;
- organization enforcement of secure two-factor methods where supported and
  appropriate;
- more than one practical authentication or recovery method;
- protected recovery material not stored only in the primary workstation
  failure domain;
- reviewed SSH keys;
- reviewed personal access tokens and application authorizations;
- reviewed organization owners, members, outside collaborators, and
  administrative access;
- reviewed organization audit activity; and
- a current, controlled security-notification/recovery email path.

The governance record shall not disclose the actual recovery codes, private keys,
token values, or other secret material used to satisfy these requirements.

## Suspected compromise

If GitHub administrative authority may be compromised:

1. Treat the condition as a security incident under `ISS-IR-001`.
2. From a separate trusted system or trusted recovery context where practical,
   secure the controlling personal account.
3. Review and revoke or replace unexpected or potentially exposed authentication
   methods, SSH keys, personal access tokens, and application authorizations.
4. Review organization owners, members, outside collaborators, repository
   administration, branch/security settings, and recent audit activity for
   unauthorized change.
5. Rotate or replace any other ISS authority whose secrecy or trust may have
   depended on the compromised context.
6. Verify canonical repository state and signed history before resuming
   trust-sensitive engineering or governance actions.
7. Retain a non-secret incident/recovery record and reference protected material
   by stable identifier or digest when necessary.

A valid Git signature is not automatically trusted when the signing authority or
the environment protecting it may have been compromised.

## Lost SSH authentication authority

Loss of an SSH private key is handled as replacement, not as an assumption that
the original private key can or should be recovered.

1. Confirm control of the GitHub personal account through an unaffected
   authentication/recovery path.
2. Remove the lost or suspect SSH public key from GitHub.
3. Create a replacement SSH authentication authority from a trusted system.
4. Protect the replacement private key with appropriate local controls.
5. Add only the replacement public key to GitHub.
6. Verify authenticated Git access.
7. Update governed access/recovery records without publishing the private key or
   other secret material.

Private-key backup is not asserted by this procedure.

## Lost account authentication or 2FA method

Use an already configured GitHub recovery method.

Recovery methods may include protected recovery codes or another configured
authentication/recovery factor.

Do not rely on an assumption that GitHub Support can restore an account when all
configured recovery methods are lost.

If the account cannot be recovered, treat the loss as a material continuity and
security event and establish a new governed administrative authority before
resuming trust-sensitive operations.

## Review after recovery

After any real recovery or revocation event:

- perform an `ISS-IAM-002` privileged-access review;
- update the applicable risk treatment under `ISS-RSK-001`;
- update `ISS-BCP-001` recovery state if the procedure was exercised;
- evaluate whether `ISS-IR-001` incident closure criteria are satisfied;
- verify repository and organization configuration as applicable; and
- keep self-review explicitly identified as self-review where no independent
  person participated.

## Provider documentation reviewed

The procedure was prepared against current GitHub documentation for organization
two-factor-authentication requirements, secure two-factor methods, account
recovery methods and recovery codes, SSH-key and personal-access-token recovery
relationships, and review/revocation of organization-accessing credentials.

Provider documentation describes GitHub capabilities. It is not independent
proof that a particular ISS setting is enabled.

## Validation state

This procedure is a documented recovery/revocation path.

It is not a destructive recovery exercise and does not claim that the GitHub
account, SSH authority, or organization was actually recovered during creation
of this procedure.
