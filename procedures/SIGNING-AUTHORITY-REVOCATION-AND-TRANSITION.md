# Signing Authority Revocation and Transition Procedure

## Purpose

Define a non-secret, reconstructable response path for suspected compromise,
confirmed compromise, loss, or intentional replacement of the current Iron
Signal Systems Git commit-signing authority.

This procedure supports `ISS-RISK-002`, `ISS-IAM-002`, `ISS-IR-001`,
`ISS-BCP-001`, and `ISS-ENG-001`.

It does not publish private keys, passphrases, recovery secrets, or other
authentication material.

## Current boundary

Iron Signal Systems is currently operated as a solo-developed project.

The current signing authority is controlled by the sole project operator.

No alternate signer or independent approver is invented by this procedure.

## Normal protection expectations

The signing authority should maintain, as applicable:

- a signing private key distinct from GitHub SSH authentication authority;
- passphrase protection for the signing private key;
- storage only on intentionally authorized ISS systems;
- no repository or ordinary cloud-sync storage of the signing private key;
- no unnecessary duplicate or obsolete private-key copies;
- local access controls appropriate to the intended user and system authority;
- deliberate operator action for signing rather than unattended unrestricted use;
- a recognizable public signing identity that can be verified without exposing
  secret material; and
- a current transition and compromise-response path.

The governance repository shall not contain the signing private key,
passphrase, or other secret material merely to prove these expectations.

## Suspected or confirmed compromise

If compromise of signing authority is reasonably suspected:

1. Treat the condition as a security incident under `ISS-IR-001`.
2. Stop trust-sensitive signing, release acceptance, and governance actions that
   depend on the suspect authority until the trust decision is resolved.
3. From a trusted system or context where practical, identify the last signing
   activity that can still be reconstructed from known repository history and
   other available records.
4. Treat signatures produced after the possible-compromise point as requiring
   review rather than automatically trusted merely because cryptographic
   verification succeeds.
5. Generate a replacement signing authority from a trusted context.
6. Publish or configure the replacement public verification identity where
   required by the applicable engineering and repository process.
7. Record the transition point and old/new public identities without publishing
   private material.
8. Do not rewrite historical Git history merely to create a new authority.
9. Reevaluate affected repositories, accepted releases, governance records, and
   engineering assurance where trust may have depended on the compromised
   authority.
10. Resume trust-sensitive signing only after the replacement authority and
    repository trust state are established.

## Lost signing authority

Loss without suspected compromise is handled as replacement and transition.

The procedure does not assume the private signing key is recoverable.

1. Confirm the loss condition.
2. Create a replacement signing authority from a trusted context.
3. Configure the replacement public verification identity.
4. Verify that new signed Git operations succeed.
5. Record the transition point and public identity change.
6. Update applicable access, continuity, and engineering records.

Private-key backup is not asserted by this procedure.

## Intentional rotation

Intentional rotation follows the same controlled transition pattern:

1. create the replacement authority;
2. verify the replacement public identity;
3. establish the transition point;
4. update applicable verification configuration;
5. verify a new signed Git operation; and
6. retire the old authority from future use.

The old private key shall not be retained indefinitely merely because it once
signed trusted history.

## Verification after transition

After a real replacement or rotation event:

- verify a new signed Git commit with the replacement authority;
- perform an `ISS-IAM-002` privileged-access review;
- update `ISS-RISK-002` under `ISS-RSK-001`;
- update the `ISS-BCP-001` signing-recovery state;
- evaluate `ISS-IR-001` closure criteria when compromise was suspected;
- evaluate applicable `ISS-ENG-001` / ISRAS trust implications; and
- keep self-review explicitly identified as self-review where no independent
  person participated.

## Relationship to repository history

A cryptographically valid signature establishes that the configured signing
authority produced the signature.

It does not prove that the authority was uncompromised at signing time.

If signing authority is suspected compromised, repository history and accepted
engineering state must be reviewed according to the applicable incident and
engineering controls.

## Validation state

This procedure defines the revocation/replacement/transition path.

Creation of the procedure is not a destructive key-loss or compromise exercise
and does not claim that a real signing-authority transition occurred.
