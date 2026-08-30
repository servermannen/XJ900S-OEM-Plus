# COMP-0008: Owner-Reported Yamaha Tracer 900 GT Left Handlebar Switch

**Purpose:** Record the purchased left-hand handlebar-switch candidate while
preserving conflicting historic identification and without establishing Yamaha
application, compatibility, acceptance, or validation.

**Document status: Draft**

## Candidate identification

- Component: Left-hand handlebar-switch assembly - project-reported
  identification
- Manufacturer: Yamaha - project-reported identification; physical marking not
  recorded
- Source model: Tracer 900 GT - owner-reported; exact Yamaha application,
  market, model-year range, and variant Unverified
- Model year or range: Unknown
- Current project-supplied identification: `B1J-83954-11-00`
- Conflicting historic identification: `B5U-83954-01`
- Source or listing: Owner-provided purchase information; no retained listing or
  authoritative Yamaha parts-catalogue evidence is recorded
- Evaluation date: 2026-08-30

## Evaluation status

**Status: Unverified**

**Review: Technical Review Required**

## Evidence register

| Evidence | Recorded information | Boundary |
| --- | --- | --- |
| Current project-supplied identification | The physical/purchased component is currently identified in the project as `B1J-83954-11-00`. | Acquisition and project-identification provenance only; it does not independently confirm a physical marking, Yamaha application, compatibility, or acceptance. |
| Historic project information | Older project material identified the component as `B5U-83954-01`. | Conflicting historic information retained for traceability; it is not silently replaced or treated as a supersession record. |
| Prior catalogue context | B1J-family handle-switch part numbering has previously been associated with Yamaha catalogue evidence. | No retained authoritative evidence reviewed for this record establishes the exact application or any supersession relationship for `B1J-83954-11-00`. |

The exact relationship, if any, between `B1J-83954-11-00` and
`B5U-83954-01` remains Unverified.

## Intended function

The component is relevant to evaluation of non-engine rider-control and HMI
functions that may fall within Level 2. This record does not select the switch,
its electrical implementation, an interface architecture, or any control
assignment.

## Applicable requirements

- [SYS-003](../requirements/system-requirements.md#sys-003)
- [SYS-006](../requirements/system-requirements.md#sys-006)
- [SYS-010](../requirements/system-requirements.md#sys-010)
- [SYS-011](../requirements/system-requirements.md#sys-011)
- [SAF-002](../requirements/system-requirements.md#saf-002)
- [SAF-004](../requirements/system-requirements.md#saf-004)
- [REL-002](../requirements/system-requirements.md#rel-002)
- [REL-004](../requirements/system-requirements.md#rel-004)
- [SRV-003](../requirements/system-requirements.md#srv-003)
- [ARC-002](../requirements/system-requirements.md#arc-002)
- [ARC-004](../requirements/system-requirements.md#arc-004)
- [ARC-008](../requirements/system-requirements.md#arc-008)
- [DEV-003](../requirements/system-requirements.md#dev-003)
- [DEV-008](../requirements/system-requirements.md#dev-008)
- [DOC-002](../requirements/system-requirements.md#doc-002)
- [DOC-003](../requirements/system-requirements.md#doc-003)
- [DOC-006](../requirements/system-requirements.md#doc-006)
- [DOC-008](../requirements/system-requirements.md#doc-008)

## Known information

| Attribute | Value | Source | Status |
| --- | --- | --- | --- |
| Acquisition state | Purchased / on hand | Owner/project report | Confirmed as project acquisition provenance |
| Current project-supplied identification | `B1J-83954-11-00` | Latest approved project correction | Confirmed as project-supplied identification; exact Yamaha application Unverified |
| Historic identification | `B5U-83954-01` | Older project material | Confirmed as conflicting historic information; relationship to current identification Unverified |
| Exact Yamaha application | Unknown | No retained authoritative evidence resolving the application | Unverified |
| Market and model-year coverage | Unknown | No retained authoritative evidence resolving coverage | Unverified |
| Supersession relationship | Unknown | No retained authoritative supersession evidence | Unverified |
| Physical markings and condition | Unknown | No documented inspection retained | Unverified |
| Switch functions and contact behavior | Unknown | No documented characterization retained | Unverified |
| Connector family, cavities, and pinout | Unknown | No retained authoritative or direct evidence | Unverified |
| Supply, signal levels, and architecture | Unknown | No retained authoritative or direct evidence | Unverified |

## Compatibility status

### Physical compatibility

Mounting geometry, locating features, handlebar fit, clearances, harness length,
routing, strain relief, and environmental condition are Unknown. Appearance,
source-family similarity, clamp fit, or matching dimensions alone would not
establish physical compatibility with the XJ900S.

### Electrical and functional compatibility

Connector identity, cavity mapping, pinout, contact matrix, supply requirements,
signal levels, electrical protection, and whether any function is discrete,
resistive, serial, or networked remain Unknown. No connector family, voltage,
switch matrix, CAN architecture, or discrete architecture is claimed.

Electrical characterization and connector/cavity mapping remain future evidence
work. The component shall not be energized merely to resolve its identity or by
assuming similarity to another Yamaha switch.

### Safety suitability

Rider-control functions may influence signaling, warning, horn, lighting, or
other safety-relevant behavior. No safety suitability, installed function, road
readiness, or technical-review result is established.

Review: Technical Review Required

## Accepted architecture boundary

[ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) permits
non-engine rider inputs and HMI functions to be evaluated for Level 2 while
Level 1 retains fuel, ignition, engine shutdown, and any later accepted direct
throttle authority. This record does not alter those boundaries and does not
accept a Level 2 electrical implementation.

## Integration assessment

### Benefits

- The acquired component is available for documented non-destructive
  identification and later characterization.

### Risks and constraints

- Conflicting project identifications remain unresolved.
- Incorrect application, interface, or energization assumptions could damage
  the component or produce unsafe rider-control behavior.
- Acquisition does not establish availability of documentation, connector
  counterparts, service parts, or a suitable interface.

### Required adaptations

Unknown; no mechanical or electrical adaptation is proposed or accepted.

### Missing evidence

- Photographs and direct recording of all labels and moulded markings.
- Authoritative Yamaha parts evidence for exact application and any
  supersession relationship.
- Physical dimensions, mounting, clearances, and condition inspection.
- Connector identification, cavity population, wire colours, and cavity map.
- Switch/contact or communication characterization using a reviewed method.
- Defined interface, protection, fault handling, acceptance criteria, and
  technical review.

## Decision recommendation

**Recommendation: Continue research**

**Rationale:** The component is purchased and available, but identification
conflict, exact application, physical and electrical compatibility, functional
behavior, safety suitability, and acceptance remain unresolved.

Acquisition and availability do not constitute component acceptance.

## Required validation

- Record direct photographs and physical markings without inferring application.
- Resolve exact Yamaha application and any supersession only through retained
  authoritative evidence.
- Inspect condition and measure mounting and clearance interfaces.
- Map connectors and cavities before any powered work.
- Characterize functions using a documented, current-limited, technically
  reviewed test method where powered work is necessary.
- Define acceptance criteria and complete applicable technical review before
  installation or road use.

## Traceability

- Related research: None recorded
- Related ADRs: [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md)
- Related tests: None recorded
- Roadmap stage: [Stage 2 - requirements and measurement capture](../implementation/roadmap.md#stage-2--requirements-and-measurement-capture)

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-30 | Created acquired-candidate record with current and conflicting historic identifications. | Add the missing purchased component without inferring Yamaha application, electrical architecture, compatibility, or acceptance. |

## Navigation

[Component index](README.md) | [Purchased / on-hand inventory](PURCHASED-ON-HAND-INVENTORY.md) | [Documentation index](../INDEX.md) | [Component evaluation template](../templates/component-evaluation-template.md)
