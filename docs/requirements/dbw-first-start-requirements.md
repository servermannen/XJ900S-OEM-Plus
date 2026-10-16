# XJ900S OEM+ — First-start DBW requirements

Document status: Draft
Status: Proposal
Review: Technical Review Required
Test execution: Not started
Test result: Not evaluated

## Source and acceptance boundary

Source draft: owner-supplied `DBW-FIRST-START-REQUIREMENTS-DRAFT.md`, received
2026-10-16. All twelve proposed requirement IDs are retained. DBW-011 was clarified during technical review preparation to explicitly include firmware, fault-handling and safe-state validation.
The review and test-status labels above apply to every requirement and release
gate below; this document records no executed tests or technical approval.

Under [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) and
[System architecture](../architecture/system-architecture.md):

The accepted three-level architecture reserves engine-critical control authority to Level 1. The proposed DBW implementation, component interfaces and safety mechanisms require separate technical validation and acceptance. Level 2 and Level 3 shall not acquire throttle authority or become dependencies for safe Level 1 operation. The first-start configuration described here
is a proposal, not an accepted ECU or throttle-control selection or permission
to energize hardware. Level 1 retains engine-critical authority; Level 2 and
Level 3 must not become dependencies for basic engine operation. These gates
supplement, rather than replace, existing requirements and acceptance gates.
The priority order in [ADR-0004](../decisions/ADR-0004-project-priority-order.md)
and retained charging architecture in
[ADR-0003](../decisions/ADR-0003-retain-original-field-regulated-charging-architecture.md)
continue to apply.

Related [system requirements](system-requirements.md): SYS-004 through SYS-006
for staged validation and priorities; SAF-001, SAF-003, SAF-004, SAF-006 through
SAF-008 for shutdown, safe states, review, protection and diagnosis; ARC-001,
ARC-003 and ARC-006 through ARC-008 for authority, independence and modular
testing; DEV-001 through DEV-008 for validation evidence; and DOC-001 through
DOC-009 for documentation and traceability. This is scope traceability, not a
claim that those requirements have been implemented or verified.

## Scope and architecture

This document defines *proposed* acceptance gates for the first engine start using the on-hand 2022 Yamaha MT-10 electronic throttle-body assembly and Tracer 9 electronic accelerator grip, controlled directly by the Level 1 super-uaEFI Rev. B engine-management ECU. Neither donor assembly is accepted as electrically or functionally compatible yet. Level 2 must not have direct or implicit control over throttle, fuel, ignition, or shutdown.

## Evidence and outstanding uncertainties

- Confirmed: the project ECU reports the super-uaEFI firmware target; PCB marking identifies Rev. B (owner observations). Exact deployed firmware version and calibration baseline must be recorded again before further tests.
- Reported on hand, not validated for integration: MT-10 2022 throttle body; Tracer 9 accelerator grip.
- Open: OEM electrical diagrams and donor variants, connector cavity numbering, supply/ground arrangement, APS1/APS2 and TPS1/TPS2 electrical characteristics, polarity, absolute limits, ECU input scaling, throttle motor operating current and driver suitability, spring-rest position, wiring fault behavior, ECU software faults and watchdog response.
- No pinout, voltages, motor polarity or ECU calibration figures shall be inferred from appearances or other model years.

### Repository evidence boundaries

- Status: Confirmed only for the recorded owner observations: the delivered
  board marking and read-only firmware target are documented in
  [RESEARCH-0007](../research/RESEARCH-0007-super-uaefi-stage1-hardware-feasibility.md).
  Exact schematic, BOM, build-option and Rev B/Rev C applicability remain
  Unverified; the target name does not establish driver suitability.
- Status: Unverified for donor application and integration compatibility:
  [COMP-0004](../components/COMP-0004-2023-2024-tracer9-right-switch-dbw-grip.md)
  records the current project-supplied grip identification `BAP-8291R-10` and
  conflicting historic `B5U-8291R-10` identification;
  [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md)
  bounds the seller-reported 2022 MT-10 provenance. Neither record establishes
  compatibility with this proposed configuration.
- Status: Unverified for the exact connector implementation in this proposed
  configuration. Before wiring, record evidence for connector family, exact
  housing and mate/header, terminal family/type/size, cavity numbering and
  viewing orientation, primary lock, secondary lock/TPA/retainer, seals/cavity
  plugs, removal/depinning tool and method, and crimp tool/terminal replacement
  data using the [connector identification template](../templates/connector-identification-template.md).
  Preserve Unknown/Unverified where evidence is missing. Visual similarity,
  cavity count, wire colour and physical mating establish neither identity,
  pinout nor electrical or functional compatibility.

## Proposed requirements and verification

| ID | Requirement | Verification / evidence | Status |
| --- | --- | --- | --- |
| DBW-001 | All APS/TPS power, return and signal pins shall be independently identified before energizing. | Donor OEM schematics, continuity and controlled measurements. | Proposal |
| DBW-002 | Both independent accelerator channels shall be read, range-checked and mutually checked across travel. | Low-energy sweep and injected open/short/out-of-range faults. | Proposal |
| DBW-003 | Both throttle-position channels shall be read, range-checked and mutually checked across movement. | Passive sweep and injected faults. | Proposal |
| DBW-004 | ETB driver electrical ratings, motor polarity and current limiting shall be verified before commanding movement. | Manufacturer hardware evidence and current-limited bench test. | Proposal |
| DBW-005 | The unpowered spring-rest position, stops, mechanical return and friction shall be measured. | Unpowered mechanical inspection and documented photos/angles. | Proposal |
| DBW-006 | Missing, implausible or inconsistent APS/TPS signals shall not cause unintended opening. | Fault injection for each sensor channel and combinations. | Proposal |
| DBW-007 | Driver failure, lost power, MCU reset and watchdog events shall reach a defined, tested safe state. | Independent supply interruption and reset/fault tests. | Proposal |
| DBW-008 | Unexpected throttle motion, runaway demand and position tracking error shall be detected and safely handled. | Controlled actuator rig with travel/current constraints. | Proposal |
| DBW-009 | Initial power-on and configuration shall not automatically move the ETB without explicit controlled authorization. | Cold-start and reconnect test, no fuel/ignition outputs. | Proposal |
| DBW-010 | Fuel and ignition disabling shall remain Level 1 responsibilities and not rely on Level 2/CAN. | Isolation and fault injection, verify commanded and physical output state. | Proposal |
| DBW-011 | Throttle control shall not be enabled for engine start until electrical, mechanical, firmware and fault-handling tests have passed, the defined safe states have been verified, and the technical review has been completed. | Signed technical review and test records. | Proposal |
| DBW-012 | The exact firmware/INI/configuration shall be versioned with checksums, with no migrated donor settings silently accepted. | Reproducible baseline export and comparison. | Proposal |

## Defined safe state — open design question

A safe state cannot yet be specified solely as “closed throttle”: the mechanical spring rest may be partly open. Prior to any engine start, establish and test the motor de-energized resting position and Level 1 fuel/ignition cut behavior for each major DBW fault. Reject configurations that cannot guarantee prevention of uncontrolled engine torque. The target state and timing limits require technical review and measurement.

## First-start release gates

1. Verify exact donor part numbers, connector pinouts, supplies and return paths from documentation and measurements.
2. Validate redundant APS/TPS tracking and each disconnect, short-to-ground/supply and cross-channel discrepancy case.
3. Verify ETB electrical protection, motion limits, current limits, return spring and non-runaway behavior on a restrained bench fixture.
4. Confirm engine synchronization, physical ignition timing with timing light, fuel-pressure control and injector/coil actuation independently of the DBW rig.
5. Test emergency stop, fuel pump shutdown and engine shutdown at Level 1 with all relevant input/power failures.
6. Require recorded technical review before connecting actuators for engine-running tests; brief operation is not final acceptance.

## Calibration donor handling

External rusEFI tunes are research examples only. Never import pin assignments, trigger offsets, dwell, injector dead time, ETB/PPS/TPS settings, current limits, or ignition/fuel tables into the project ECU by copying a donor MSQ. Numerical comparison of donor VE, lambda and ignition tables must preserve sources, native axes, units, firmware signature and any caveats, and must be labeled analytical only.

## Sources to verify

- rusEFI online tune library: https://rusefi.com/online/
- rusEFI CBR600RR tune: https://rusefi.com/online/view.php?msq=1499
- rusEFI CBR600RR troubleshooting discussion: https://rusefi.com/forum/viewtopic.php?f=16&t=2572
- Yamaha MT-10 2022 service manual (project reference; exact donor variant applicability to be checked).
- Yamaha Tracer 9 service documentation (project reference; exact grip variant applicability to be checked).

## Navigation

[Documentation index](../INDEX.md) | [System requirements](system-requirements.md) | [Test strategy](../testing/test-strategy.md)
