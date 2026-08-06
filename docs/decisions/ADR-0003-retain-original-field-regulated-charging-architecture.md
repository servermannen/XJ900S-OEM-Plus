# ADR-0003: Retain Original Field-Regulated Charging Architecture

**Purpose:** Evaluate and record the accepted charging-architecture decision.

**Document status: Draft**

**Status: Accepted**

## Context

The project considered replacing the original field-regulated generator
architecture with a permanent-magnet generator arrangement using a Shindengen
SH847 series regulator. The original architecture controls generator output
through rotor-field excitation. An SH847 is intended for a permanent-magnet
charging architecture and does not provide the required rotor-field control
function.

A connector, similar regulated-voltage range, physical resemblance, or
commercial availability does not establish electrical compatibility,
functional compatibility, safety suitability, or acceptance. Conversion would
also require evidence for the rotor, stator, regulator, rectification, mounting,
wiring, thermal behavior, balance, retention, and service consequences.

The field-regulated architecture reduces generator production when electrical
load is low. No sufficient measured capacity, thermal, or reliability evidence
has demonstrated a need for a permanent-magnet conversion.

The complete Yamaha manual currently referenced by project research states
applicability to the 1995 4KM1 variant. Its exact generator details are not
automatically confirmed for the project-recorded 1997 motorcycle. Direct
inspection, year-applicable sources, and measurement remain required.

Review: Technical Review Required

## Evidence basis

| Evidence category | Recorded basis | Status and boundary |
| --- | --- | --- |
| Manual-stated 1995 4KM1 source evidence | The Yamaha XJ900S(G) Service Manual, identifier 4KM-28197-20, is the local complete manual reference used by the project. Its identity and 1995 4KM1 applicability boundary are recorded in [RESEARCH-0003](../research/RESEARCH-0003-trigger-and-synchronization-strategy.md#sources). The referenced charging-system material documents a rotor-field-controlled generator architecture for that variant. | Confirmed for the manual-stated 1995 4KM1 source only; it is not direct evidence for the complete 1997 project motorcycle. |
| Official Shindengen regulator-architecture evidence | Shindengen's official [Regulators/Rectifiers technical page](https://www.shindengen.com/products/electro/motorcycle/reg/) (accessed 2026-08-06) states that a three-phase open regulator/rectifier controls charging by rectifying ACG output and opening that output when battery voltage is high. The published operating description does not include a rotor-field excitation or control function. | Confirmed for the documented open-regulator operating principle. The public page does not identify SH847 by model number, and no model-specific official SH847 datasheet is recorded in this repository. |
| Direct project measurements | The project has not yet inspected or measured the complete charging architecture on the project-recorded 1997 motorcycle. Generator identity, field wiring, regulator and rectifier identity, condition, output, voltage drop, temperature, and load capacity remain to be recorded. | Not executed; Status: Unverified. |
| Engineering conclusion | The retained generator architecture documented by the manual-stated source requires rotor-field control. The SH847 open/series architecture under consideration has no rotor-field control function in its documented operating principle. Direct SH847 substitution therefore cannot provide the required control function. This incompatibility is an engineering conclusion derived from those two documented architecture facts, not a direct project measurement. | Supports rejection of direct SH847 integration under this ADR; it does not validate the existing charging system. |
| Exact 1997 applicability | The manual source is for the manual-stated 1995 4KM1 variant, while the project motorcycle is recorded as a 1997 XJ900S. | Status: Unverified pending year-applicable evidence and direct inspection. |

Marketplace listings, connector resemblance, and seller descriptions are not
used here to establish electrical operating principle.

## Decision

The project shall:

- Retain the original field-regulated generator architecture.
- Reject SH847 integration.
- Reject conversion of the original generator to a permanent-magnet generator.
- Inspect, measure, repair, and load-test the original charging system as
  required.
- Spend no further project effort designing an SH847 mount, SH847 Furukawa
  harness, or SH847 integration unless measured evidence justifies reopening
  this decision.

This decision does not claim that the generator is currently serviceable, that
its output is sufficient for the final EFI load, or that exact 1997 component
details have been confirmed.

## Decision drivers

- Preserve OEM mechanical architecture and serviceability.
- Avoid an architecture that cannot perform the required rotor-field control
  function.
- Require measured capacity, voltage-drop, temperature, condition, and load
  evidence before redesign.
- Avoid unvalidated rotor, stator, regulator, rectifier, bracket, connector, and
  harness changes.
- Concentrate project effort on demonstrated maintenance and capacity needs.

## Considered alternatives

### Retain and service the field-regulated architecture

- Benefits: Preserves the original mechanical architecture, controls generator
  production through the field system, retains a repair and service path, and
  limits change until measurements identify a need.
- Drawbacks: Brushes, slip rings, regulator, rectifier, windings, connectors,
  and grounds remain inspection and service items; capacity still requires
  validation.
- Evidence boundary: Architecture decision accepted; exact 1997 condition,
  output, temperature, voltage drop, and part details remain Unverified.
- Decision outcome: Accepted.

### Integrate a Shindengen SH847

- Benefits considered: A production series-regulator component and a possible
  charging-system modernization path.
- Drawbacks: It does not provide rotor-field control, and connector fit or a
  similar regulated-voltage range would not establish functional
  compatibility.
- Evidence boundary: No measured need or complete compatible architecture has
  been demonstrated.
- Decision outcome: Rejected by this accepted ADR.

### Convert to a permanent-magnet generator architecture

- Benefits considered: Would create an architecture compatible in principle
  with a series regulator designed for permanent-magnet generation.
- Drawbacks: Requires unvalidated generator, retention, balance, thermal,
  electrical, mounting, wiring, and service changes; it removes the accepted
  field-regulated architecture without demonstrated need.
- Evidence boundary: No sufficient measured capacity, temperature, or
  reliability justification exists.
- Decision outcome: Rejected by this accepted ADR.

## Consequences

### Positive consequences

- Preserves the OEM mechanical architecture.
- Preserves serviceability and reversibility where practical.
- Avoids unnecessary generator redesign.
- Avoids unvalidated rotor, stator, regulator, bracket, connector, and wiring
  changes.
- Concentrates work on measured maintenance and electrical-capacity needs.
- Removes SH847 mount, Furukawa harness, and integration design from the active
  project scope.

### Trade-offs and retained risks

- Brushes and slip rings remain service items.
- The original regulator, rectifier, windings, connectors, grounds, and wiring
  still require inspection.
- Electrical capacity must be checked against the final EFI and motorcycle load
  budget.
- Temperature, regulated-voltage behavior, and voltage-drop testing remain
  necessary under defined conditions.
- Service-part availability remains to be verified.
- Retention of the architecture is not evidence that the existing components
  have passed inspection or load testing.

## Safety implications

Charging, wiring, electrical protection, battery behavior, temperature, and
voltage drop can affect engine management and motorcycle safety. Inspection,
repair, measurement, and load testing require defined methods, safe states,
limits from applicable evidence, and technical review before an implementation
is accepted.

**Review: Technical Review Required**

## Requirement traceability

- Related requirements: SYS-004 through SYS-006, SYS-010 through SYS-012,
  SYS-014, SAF-003, SAF-004, SAF-006, REL-001 through REL-006, SRV-001 through SRV-007,
  ARC-005, ARC-007, ARC-008, DEV-001 through DEV-008, and DOC-001 through
  DOC-008.
- Related architecture: [System architecture](../architecture/system-architecture.md).
- Related research: Charging-condition, load-budget, temperature, voltage-drop,
  and exact 1997 evidence remain to be recorded in later research and test
  records.

## Implementation impact

- Stage 1 shall inspect and record the baseline charging-system condition.
- Stage 2 shall define and measure the electrical load budget, generator output,
  voltage drop, and temperature behavior using reviewed methods.
- EFI planning shall account for measured available charging capacity.
- Repair and service work shall preserve the retained field-regulated
  architecture unless this ADR is superseded.
- No SH847 mount, SH847 Furukawa harness, or SH847 integration work is planned
  under the current decision.

## Reopening criteria

Reopening requires measured evidence of one or more of the following:

- Insufficient electrical output or capacity for accepted motorcycle loads.
- Unacceptable thermal behavior under defined and repeatable conditions.
- Repeated reliability failure after appropriate inspection and repair.
- Unavailable service parts that prevent a practical repair path.
- A fully evidenced alternative architecture that satisfies mechanical,
  electrical, functional, safety, reliability, serviceability, and validation
  requirements.

Reopening shall require a new superseding ADR. New availability information,
connector resemblance, or an untested proposed conversion is not sufficient by
itself.

## Supersession

- Supersedes: None.
- Superseded by: None.

This ADR is not superseded. Any future change to the retained architecture
shall explicitly supersede this record and preserve its rationale.

## Related documents

- [ADR-0001: Project Principles](ADR-0001-project-principles.md)
- [ADR-0002: Three-Level Control Architecture](ADR-0002-three-level-control-architecture.md)
- [System requirements](../requirements/system-requirements.md)
- [System architecture](../architecture/system-architecture.md)
- [Implementation roadmap](../implementation/roadmap.md)
- [Test strategy](../testing/test-strategy.md)

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-06 | Recorded the accepted decision and its bounded manual, regulator-architecture, measurement, and engineering evidence basis. | Close SH847 and permanent-magnet conversion work unless measured evidence supports a superseding ADR without presenting 1995 source evidence as direct 1997 verification. |

## Navigation

[Decision register](README.md) | [Documentation index](../INDEX.md)
