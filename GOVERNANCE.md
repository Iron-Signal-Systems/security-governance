# Iron Signal Systems Security Governance

## Purpose

Iron Signal Systems maintains a security governance system to protect the confidentiality, integrity, availability, authenticity, and recoverability of Iron Signal Systems information, software, infrastructure, customer systems, and services.

Security governance establishes organizational authority and accountability. It does not replace product engineering standards or product-specific security requirements.

## Current organizational state

Iron Signal Systems is currently operated as a solo-developed project and has
not been formed as a separate legal business entity.

This governance system governs activities performed under the Iron Signal
Systems name. Governance roles identify responsibilities and authority and do
not imply the existence of employees, officers, departments, a corporation, an
LLC, or another separate legal entity.

The current Governance Authority may hold multiple governance and engineering
roles because only one person presently exercises those responsibilities.

Role assignment does not create independence. A person shall not represent
review of their own work as independent review.

The governance structure shall be revised when material organizational, legal,
personnel, or authority changes make the current model inaccurate.

## Governance boundaries

### Organizational security governance

This repository governs organizational matters including:

- information-security risk management;
- personnel security;
- identity and access management;
- information classification and handling;
- security incident management;
- business continuity;
- vendor and supplier security;
- infrastructure and administrative security;
- security awareness;
- compliance obligations;
- organizational exceptions;
- governance review; and
- independent external assessment where required.

### Engineering assurance

The Iron Signal Repository Assurance Standard (ISRAS) is the authoritative engineering standard for Iron Signal Systems repositories.

ISRAS governs applicable repository, source, testing, validation, component, vulnerability, change, acceptance, release, deployment-verification, recovery, historical-verification, and related engineering-assurance requirements.

Organizational governance may inherit results produced by ISRAS and shall not duplicate an ISRAS control when the engineering requirement is already governed authoritatively by ISRAS.

## Governing principles

Iron Signal Systems security controls shall be:

- proportional to actual risk;
- technically and operationally enforceable where practical;
- attributable to an accountable authority;
- reviewable;
- testable where applicable;
- supported by retained control records;
- bounded in scope;
- explicit about exceptions;
- fail-closed where uncertainty could create unacceptable security or operational risk; and
- no more complex than required to control the identified risk.

A policy shall not claim that a control exists unless Iron Signal Systems actually performs the control.

Automation, separate accounts, separate cryptographic keys, or artificial-intelligence systems shall not be represented as independent human review.

## Authority

Security governance authority shall be assigned explicitly.

A person may perform more than one governance role while Iron Signal Systems is operated by one person or limited personnel. Where independence is required, the same person shall not claim independent review of their own work.

Required independent functions may be performed by qualified external parties when the available personnel cannot satisfy the required independence.

## Control model

Every governed organizational security control shall have a stable control identifier and identify, as applicable:

- control objective;
- scope;
- accountable owner;
- responsible operator;
- required activity;
- execution or review frequency;
- triggering conditions;
- required control records;
- inherited controls;
- exception authority; and
- review boundary.

## Risk management

Material risks shall be recorded, assigned an owner, evaluated, and addressed through one or more of:

- avoidance;
- reduction;
- transfer;
- acceptance; or
- removal of the activity creating the risk.

Risk acceptance shall be explicit and bounded and shall not silently disable an otherwise mandatory engineering or organizational control.

## Exceptions

An exception shall identify:

- the control being excepted;
- the reason;
- the affected boundary;
- the risk created or retained;
- compensating controls where applicable;
- approving authority;
- approval date;
- expiration or mandatory review date; and
- remediation plan where applicable.

Expired exceptions shall not remain valid through silence.

## Control records

Iron Signal Systems shall retain sufficient records to determine whether required controls were performed. Records shall describe what actually occurred.

Sensitive operational records shall be protected according to their information classification and shall not be placed in a public repository merely to demonstrate compliance.

## Governance review

Security governance shall be reviewed periodically and after material changes including significant incidents, substantial organizational changes, materially different technologies or services, significant requirement changes, and findings from internal or independent review.

## Continuous improvement

A control deficiency, security incident, failed test, unsuccessful recovery, audit finding, customer issue, or newly understood risk may require modification of the governance system.

Changes should correct the underlying control weakness where practical rather than merely producing additional documentation.
