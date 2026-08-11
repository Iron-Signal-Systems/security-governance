# Domain Neutral Platform ISRAS Adoption-Topology Review

## Review identity

**Review date:** 2026-08-11
**Repository:** `Iron-Signal-Systems/domain-neutral-platform`
**Authority:** Sole project operator acting as Engineering Authority
**Independence:** Self-review; not independent
**Decision:** `RETAIN_EXPLICIT_NON_ADOPTED_STATE`

Canonical DNP contains an active nested Go module at `go/platform/go.mod` and no
committed `.isras/project.json`.

No ISRAS adoption claim is made. The repository remains explicitly non-adopted
rather than hand-authoring a project pin, moving/fabricating Go content, or
claiming a topology not accepted for this repository.

`ISS-ENG-ACT-001` is complete as a review action. Completion means the topology
decision was made; it does not mean DNP is adopted.

A future material topology change or an accepted ISRAS profile/topology that can
truthfully govern DNP as it exists triggers reevaluation.

This decision does not modify DNP source, create a project pin, alter Atlas or
File Intelligence pins, create independent review, or claim external assurance.
