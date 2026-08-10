# Business Continuity and Recovery Policy

## Purpose

Maintain truthful and proportionate recovery capabilities for material Iron
Signal Systems systems, repositories, authorities, services, and operational
dependencies.

## Current organizational state

Iron Signal Systems is currently operated as a solo-developed project.

There is no current customer-production or customer-critical operated-service
boundary in this governance baseline.

Continuity requirements shall therefore reflect the current development and
administrative boundary rather than invented production commitments.

## Recovery requirements

Material recovery boundaries shall identify, as applicable:

- affected asset or dependency;
- required recovery outcome;
- authoritative reconstruction or backup source;
- whether the source is local, off-host, independent, or provider-managed;
- restoration or replacement sequence;
- required authority;
- validation method;
- responsible governance role;
- known limitations; and
- open recovery action.

A recovery-time objective or recovery-point objective shall be defined only when
supported by an actual operating need.

## Backup and snapshot truth

A backup shall not be considered a proven recovery capability merely because it
exists.

A local snapshot in the same host/storage failure domain is not an independent
off-host backup against complete loss of that domain.

Remote Git history is a reconstruction source only for content actually pushed
and retained remotely.

## Authority recovery

Authentication and signing secrets shall not be published as continuity records.

Loss or compromise of protected authority may require revocation, provider
recovery, replacement keys, governed transition, and related incident or
engineering review rather than restoration of the original secret.

## Supplier dependencies

Provider-managed recovery shall be recorded as provider-managed.

It shall not be represented as independently validated ISS recovery unless
actually validated.

## Sole-operator continuity

There is currently no alternate internal operator.

Current ISS work may pause if the sole operator is unavailable.

Before future customer, production, support, contractual, legal, or
public-safety obligations require continuation during such unavailability, an
appropriate continuity path shall be established.

## Exercise

Material recovery procedures shall be exercised at least annually and after
material recovery-boundary change.

Exercises shall clearly distinguish technical actions actually executed from
tabletop or assumed actions.

A partial recovery test shall not be represented as complete disaster recovery.
