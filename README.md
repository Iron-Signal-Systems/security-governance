# Iron Signal Systems Security Governance

<p align="center">
  <img src="docs/assets/security-governance-emblem.png"
       alt="Iron Signal Systems Security Governance emblem"
       width="720">
</p>

This repository defines the organizational security governance system for Iron Signal Systems.

It governs organizational security responsibilities including risk management, identity and access management, incident response, business continuity, supplier security, information classification, security awareness, organizational exceptions, and governance review.

It does not replace the Iron Signal Repository Assurance Standard (ISRAS). ISRAS remains the engineering assurance authority for Iron Signal Systems repositories and software lifecycle controls.

## Current organizational state

Iron Signal Systems is currently operated as a solo-developed project and has
not been formed as a separate legal business entity.

This governance system applies to software, repositories, infrastructure,
information, services, and other work conducted under the Iron Signal Systems
name.

Governance roles describe responsibilities and authority. They do not imply the
existence of employees, officers, departments, a corporation, an LLC, or another
separate legal entity.

The governance model shall be reviewed when the organizational or legal
structure materially changes.

## Authority boundaries

- `security-governance`: organizational security governance and ISMS/GRC controls.
- `engineering-standards`: ISRAS engineering assurance authority.
- product repositories: product architecture, runtime behavior, domain requirements, and product-specific controls.

## Current status

**Current-boundary organizational security-governance baseline — operating.**

All twelve baseline controls are `Implemented`. The 2026-08-11
current-boundary hardening pass is complete with explicitly retained open risks.

This status does not mean the controls are `Verified`, independently assessed,
certified, or externally attested.

This repository is not ISRAS-adopted. Its organizational governance authority
and ISRAS's engineering-assurance authority remain separate, defined boundaries.

External certification and framework mapping remain intentionally out of scope
until sufficient operating history and an appropriate assessment boundary exist.

## Repository layout

- `GOVERNANCE.md` — organizational governance authority and principles.
- `SECURITY-POLICY.md` — top-level information security policy.
- `controls/` — ISS control catalog and machine-readable control registry.
- `policies/` — operational policy documents.
- `registers/` — risks, assets, suppliers, and exceptions.
- `records/` — guidance for retained control records; sensitive records should not be committed here unless explicitly safe.

## Governing rule

Define and operate real ISS controls first. External certification and framework mapping come later, after the controls have operating history.
