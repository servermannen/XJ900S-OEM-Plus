# RESEARCH-0001: Engine-management platform

**Purpose:** Define the research scope, evidence needs, and evaluation criteria
for selecting the Level 1 engine-management platform for the XJ900S OEM+
project.

**Document status: Draft**

Status: Unverified

Review: Technical Review Required

The final engine-management platform has not been accepted. This record does
not confirm the capability, suitability, or safety of any candidate platform.

## Research question

Which engine-management platform can satisfy the accepted Level 1 requirements
for the XJ900S OEM+ project while providing sufficient reliability,
serviceability, safety, documentation, diagnostic capability, and future
development flexibility?

## Scope

### Included

- Engine-position sensing support.
- Engine synchronization strategy.
- Sequential or batch fuel-injection capability.
- Ignition control.
- Required sensor inputs and actuator outputs.
- Fuel-pump safety control and fall or tip-over shutdown handling.
- Idle-control support and cable-throttle support.
- Drive-by-wire capability as a separately evaluated future option.
- Fault handling, safe-state behavior, diagnostics, data logging, and
  calibration tools.
- Hardware availability, documentation quality, firmware maturity,
  serviceability, community and developer support, licensing, and long-term
  maintainability.
- Integration with the accepted three-level architecture and the ability to
  bench-test Level 1 independently.

### Excluded

- Final throttle-body selection.
- Final injector selection.
- Final crank or cam sensor hardware.
- Detailed wiring and pin assignment.
- Final calibration.
- Level 2 controller, display, or PDM selection.
- ABS, traction control, IMU, or other Level 3 implementation.
- Final platform acceptance.

## Current primary candidate

- Candidate: rusEFI
- Candidate status: Proposal
- Intended role: Level 1 engine-management platform
- Final acceptance: Not decided
- Hardware variant: Not selected
- Firmware version: Not selected

rusEFI is the current primary candidate because it is being evaluated as a
flexible engine-management platform, but the repository does not yet contain
sufficient evidence to accept a specific rusEFI hardware variant or rusEFI
itself as the final platform.

No rusEFI capability is treated as confirmed by this record. External evidence
for the candidate has not yet been gathered in the repository.

## Accepted Level 1 needs

The following functional needs are derived from the accepted system
requirements, system architecture, and ADR-0002:

- Crankshaft position and engine-speed acquisition.
- Camshaft position input where required by the selected synchronization
  strategy.
- Engine synchronization and phase handling.
- Four-cylinder fuel-injection control.
- Ignition control.
- Engine-load, air-temperature, engine-temperature, and throttle-position
  sensing.
- Wideband oxygen-sensor integration for calibration, monitoring, or
  closed-loop use.
- Fuel-pump command and safety shutdown.
- Starting and cranking logic.
- Idle-control support where selected.
- Engine fault detection, diagnostic visibility, and data logging.
- Shutdown following a valid fall or tip-over condition, with deliberate
  restart or reset after the event.
- Defined handling of missing, invalid, implausible, or stale critical inputs.
- Independent Level 1 bench-test capability.
- Independence from optional Level 2 and Level 3 functions for basic engine
  operation.

This list describes functional requirements and does not select specific
sensors, actuators, wiring, or a platform implementation.

## Sources and current evidence

| Source | Type | Date accessed | Relevance | Reliability notes |
| --- | --- | --- | --- | --- |
| [System requirements](../requirements/system-requirements.md) | Existing project requirement record | 2026-08-04 | Defines accepted EFI, engine-management, safety, reliability, serviceability, architecture, development, and traceability requirements. | Establishes project needs, not a platform capability. |
| [System architecture](../architecture/system-architecture.md) | Existing project architecture record | 2026-08-04 | Defines the Level 1 functional boundary and its independence from optional functions. | Does not select hardware, interfaces, or protocol. |
| [ADR-0002: Three-Level Control Architecture](../decisions/ADR-0002-three-level-control-architecture.md) | Accepted project decision | 2026-08-04 | Defines Level 1 authority for fuel, ignition, and direct engine behavior. | Does not establish platform compatibility. |
| [Implementation roadmap](../implementation/roadmap.md) | Existing project planning record | 2026-08-04 | Places engine-management concept validation in Stage 3 and bench validation in Stage 4. | Planning framework; no platform evidence. |
| [Test strategy](../testing/test-strategy.md) | Existing project verification record | 2026-08-04 | Defines bench-first and safety-focused validation expectations. | Does not provide platform test results. |

No official hardware documentation, official firmware documentation, source
code evidence, schematics, pinouts, issue-tracker records, release history,
bench-test evidence, independent technical reports, or community reports for
rusEFI or another platform are recorded here. Those external evidence sources
remain to be gathered.

## Evaluation criteria

| Criterion ID | Criterion | Priority | Evidence required | Current status |
| --- | --- | --- | --- | --- |
| EMP-001 | Four-cylinder fuel-injection support | Critical | Official documentation and, before acceptance, bench-test evidence for the selected hardware and firmware. | Unverified |
| EMP-002 | Four-cylinder ignition-control support | Critical | Official documentation and, before acceptance, bench-test evidence for the selected hardware and firmware. | Unverified |
| EMP-003 | Crank-position decoding flexibility | Critical | Official documentation, maintained technical documentation, and trigger-decoder evidence for the selected sensing design. | Unverified |
| EMP-004 | Cam-position input and phase support | High | Official documentation and evidence against the selected synchronization strategy. | Unverified |
| EMP-005 | Configurable synchronization strategies | High | Official firmware documentation and source-code or maintained technical documentation. | Unverified |
| EMP-006 | Required analog sensor inputs | Critical | Hardware documentation, schematics or pinouts, and a verified I/O count. | Unverified |
| EMP-007 | Required digital inputs | Critical | Hardware documentation, schematics or pinouts, and a verified I/O count. | Unverified |
| EMP-008 | Required injector and ignition outputs | Critical | Hardware documentation, schematics or pinouts, and safe-load bench-test evidence. | Unverified |
| EMP-009 | Fuel-pump safety control | Critical | Official documentation and bench-test evidence for normal, fault, and shutdown behavior. | Unverified |
| EMP-010 | Fall-event shutdown integration | Critical | Documented authority and interface design, plus bench-test evidence for shutdown and deliberate recovery. | Unverified |
| EMP-011 | Idle-control capability | Medium | Official documentation and evidence for the selected idle-control approach. | Unverified |
| EMP-012 | Cable-throttle compatibility | Critical | Documented control strategy and evidence that the selected platform supports the required inputs without selecting throttle hardware. | Unverified |
| EMP-013 | Drive-by-wire capability or clearly defined external handling | High | Official documentation or an accepted external-handling architecture; any direct implementation also requires a safety architecture and review. | Unverified |
| EMP-014 | Fault detection and safe-state configuration | Critical | Official documentation, maintained technical documentation, and fault-injection bench-test evidence. | Unverified |
| EMP-015 | Data logging and diagnostic visibility | High | Official documentation and a practical bench demonstration using the selected hardware and firmware. | Unverified |
| EMP-016 | Calibration-tool usability | High | Official documentation and an evaluated calibration workflow. | Unverified |
| EMP-017 | Hardware and firmware documentation | High | Official hardware and firmware documentation, schematics or pinouts, and maintained technical documentation. | Unverified |
| EMP-018 | Hardware availability and replacement path | High | Current supplier and replacement evidence for the shortlisted hardware variant. | Unverified |
| EMP-019 | Firmware maturity and maintenance activity | High | Official release history, maintained issue-tracker evidence, and documented maintenance assessment. | Unverified |
| EMP-020 | Suitability for independent bench testing and staged integration | Critical | Bench-test plan, documented interfaces, safe-load test evidence, and staged-integration assessment. | Unverified |

No scores are assigned at this stage.

## Evidence hierarchy

Preferred evidence shall be assessed in this order:

1. Official hardware documentation.
2. Official firmware documentation.
3. Source-code implementation and maintained technical documentation.
4. Hardware schematics and pinout documentation.
5. Official issue tracker and release history.
6. Bench-test evidence.
7. Independent technical reports.
8. Community reports.
9. Forum discussion or anecdotal claims.

Community claims may identify questions but shall not by themselves confirm a
safety-critical capability.

## Known evidence gaps

- A specific rusEFI hardware variant has not been selected.
- Available injector and ignition output count has not been verified for the
  final hardware candidate.
- Supported crank and cam trigger patterns have not been verified against the
  future XJ900S sensing design.
- Required analog and digital input count has not been finalized.
- Drive-by-wire support and safety architecture have not been accepted.
- Idle-control implementation has not been selected.
- Fuel-pump shutdown and fall-event behavior have not been bench-validated.
- Safe-state and degraded-operation behavior remain undefined.
- Electrical-environment suitability has not been verified.
- Enclosure, connector, vibration, moisture, and temperature suitability have
  not been verified.
- Calibration workflow and long-term service process have not been evaluated.
- Firmware release, update, and rollback strategy has not been defined.
- Replacement-hardware availability has not been evaluated.
- The integration boundary with Level 2 has not been defined in detail.
- No comparative evaluation against alternative engine-management platforms
  has yet been recorded.

## Candidate alternatives

Status: Unverified

The following categories may be investigated. Named alternatives require
separate evidence-based research before comparison.

- Open-source standalone engine-management platforms.
- Commercial motorsport ECUs.
- Motorcycle-specific aftermarket ECUs.
- Adapted production motorcycle ECUs.
- Custom engine-management hardware.

## Risks

- Selecting a platform before trigger and I/O requirements are verified.
- Depending on undocumented firmware behavior.
- Insufficient output protection.
- Inadequate motorcycle-environment robustness.
- Weak diagnostic or logging capability.
- Platform abandonment or limited replacement availability.
- Excessive dependence on one-off custom knowledge.
- Hidden coupling with Level 2 or Level 3.
- Drive-by-wire implementation without an accepted safety architecture.
- Treating successful engine start as full platform validation.

Review: Technical Review Required

The risks concerning fuel, ignition, shutdown, electrical protection, and any
future throttle function require technical review before road use.

## Required next research

1. Define the expected crank and cam sensing strategy.
2. Determine required injector, ignition, analog-input, digital-input, and
   auxiliary-output counts.
3. Identify viable rusEFI hardware variants.
4. Gather official documentation for each viable variant.
5. Verify trigger-decoder support.
6. Verify ignition and injection output capability.
7. Verify fuel-pump and shutdown logic.
8. Evaluate diagnostics and calibration workflow.
9. Evaluate electrical and environmental suitability.
10. Define a bench-test plan.
11. Compare rusEFI against at least two credible alternative platform
    categories.
12. Create a component-evaluation record for each shortlisted hardware
    platform.
13. Create an ADR only after evidence supports a platform decision.

## Preliminary conclusion

rusEFI remains the current primary candidate for further evaluation. No
engine-management platform is accepted by this research record. Platform
selection requires verified functional capability, suitable hardware,
documented safety behavior, bench-test evidence, and comparison against
credible alternatives.

## Decision impact

- Related requirements: SYS-007 through SYS-009, applicable SAF, REL, SRV,
  ARC, and DEV requirements.
- Related architecture: Level 1 engine-management system.
- Related roadmap stage: Stage 3.
- ADR required: Yes.
- Component evaluation required: Yes.
- Bench testing required: Yes.
- Recommended next action: Complete the engine-management I/O and trigger
  requirements before selecting hardware.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-04 | Created initial research record. | Establish a traceable, evidence-based platform-selection research scope. |

## Navigation

[Research index](README.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [Test strategy](../testing/test-strategy.md) | [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) | [Documentation index](../INDEX.md)
