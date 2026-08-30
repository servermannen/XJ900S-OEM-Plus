# ADR-0004: Project Priority Order

**Purpose:** Record the accepted precedence for project priorities when
requirements or design objectives conflict.

**Document status: Draft**

**Status: Accepted**

## Context

[ADR-0001](ADR-0001-project-principles.md) established otherwise valid project
principles but stated reliability, safety, and serviceability without defining
the accepted precedence now required between them. Current project documents
also used wording that could imply that reliability preceded safety.

A single explicit order is required so that requirements, proposals, and design
objectives can be resolved consistently without hiding the earlier decision
history.

## Decision

The accepted project priority order is:

1. Safety
2. Reliability
3. Serviceability
4. OEM-like integration
5. Functional improvement
6. Future expandability

This order establishes the precedence used when requirements or design
objectives conflict. Safety takes precedence over reliability, and reliability
takes precedence over serviceability. OEM-like integration, functional
improvement, and future expandability shall not override safety, reliability,
or serviceability.

This decision does not select a component, control architecture, interface, or
technical implementation.

## Consequences

- Project-wide requirements and current architecture documentation shall state
  or apply this priority order consistently.
- A lower-ranked objective may be pursued only within the constraints imposed
  by higher-ranked priorities.
- Proven production components and OEM-like integration remain important
  principles, but neither establishes compatibility, suitability, acceptance,
  or validation for a candidate component.
- No requirement, component, or implementation is marked validated or
  technically reviewed by this documentation decision.

## Requirement traceability

This decision directly governs
[SYS-006](../requirements/system-requirements.md#sys-006) and supports SYS-003,
SYS-012, SAF-001 through SAF-008, REL-001 through REL-006, SRV-001 through
SRV-007, DOC-002 through DOC-005, and DOC-008. It establishes decision
precedence; it does not claim implementation or validation of those
requirements.

## Supersession

This ADR supersedes ADR-0001 only with respect to priority ordering. It does not
supersede the remainder of ADR-0001, whose project vision, OEM+ approach,
staged implementation, component preference, custom-development principle, and
decision-history requirements remain valid.

This ADR is not superseded.

## Related documents

- [ADR-0001: Project Principles](ADR-0001-project-principles.md)
- [System requirements](../requirements/system-requirements.md)
- [System architecture](../architecture/system-architecture.md)
- [Decision register](README.md)
- [Documentation index](../INDEX.md)

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-30 | Created accepted project-priority-order decision. | Establish explicit precedence with safety before reliability while preserving the remaining ADR-0001 principles. |

## Navigation

[Decision register](README.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Documentation index](../INDEX.md)
