# ISS-TRN-001 — Security Awareness

## Control identity

**Control ID:** ISS-TRN-001
**Control:** Security Awareness
**Status:** Implemented
**Control owner:** Security Authority
**Control operator:** Security Authority
**Frequency:** Before or at material access + annual + material change

## Objective

Ensure every person with material Iron Signal Systems access understands the
security responsibilities necessary to protect ISS systems, repositories,
information, authorities, and recovery boundaries.

## Current organizational boundary

Iron Signal Systems is currently operated as a solo-developed project.

The sole project operator is the only current person within the material
development and administrative access boundary.

This control does not invent employees, contractors, an HR onboarding process,
an LMS, a training department, or a workforce that does not exist.

If another person later receives material ISS access, the awareness boundary
shall be reevaluated before or at access activation.

## Required awareness topics

The applicable awareness review shall cover, proportionate to the person's
access and responsibilities:

- authentication, multifactor authentication, and account-recovery protection;
- phishing, impersonation, social engineering, and suspicious requests;
- password, token, key, recovery-code, and other secret handling;
- SSH authentication and Git signing authority where applicable;
- least privilege and appropriate administrative use;
- patching, vulnerability identification, and remediation expectations;
- security-event and incident recognition, containment, and reporting;
- repository, source, release, and signed-history integrity;
- supplier and hosted-service dependency risks;
- information classification and handling;
- backup, snapshot, reconstruction, and recovery limitations;
- security exception governance and the difference between an exception, risk,
  action, limitation, and future boundary; and
- the rule that AI, automation, alternate accounts, keys, or sessions do not
  create independent human review.

## Completion triggers

Awareness shall be completed:

- before or at activation of material access where practical;
- at least annually while material access continues;
- after a material change to security responsibilities, controls, or operating
  boundary when the change makes prior awareness materially incomplete; and
- after an incident, finding, or recurring mistake when targeted awareness is a
  supported corrective action.

## Completion standard

Completion requires an affirmative acknowledgment by the person receiving the
awareness review.

Merely possessing a policy, opening a file, receiving an automated message, or
having prior unrelated training does not by itself establish completion.

## External training

External training may supplement this control when relevant.

ISS-TRN-001 does not depend on or publish unrelated external training history
merely to claim completion.

## Sensitive information

Awareness material shall not require publication of passwords, private keys,
tokens, recovery codes, private support communications, customer secrets, or
sensitive exploit detail.

## Related controls

Awareness reinforces but does not replace `ISS-IAM-001`, `ISS-IAM-002`,
`ISS-ENG-001`, applicable ISRAS, `ISS-VUL-001`, `ISS-IR-001`, `ISS-BCP-001`,
`ISS-SUP-001`, `ISS-RSK-001`, or `ISS-EXC-001`.

## Independence

Current awareness review may be self-administered because the current boundary
contains one person and independent awareness delivery is not required.

The record shall identify self-review as not independent.

AI assistance may help prepare material but does not create independent human
review.

## Failure conditions

ISS-TRN-001 is not operating as required when completion is recorded without an
affirmative acknowledgment, material access is introduced without the applicable
awareness boundary being addressed, secrets are published as awareness records,
or self-review is represented as independent review.

## Implementation state

The security-awareness policy is active.

The current material human boundary completed the initial required awareness
review and affirmative acknowledgment under record `ISS-TRN-REV-001`.

The awareness register is operating.

ISS-TRN-001 is `Implemented`.

Implementation does not create independent review, certify outside training, or
establish a future employee/contractor training program that does not yet exist.
