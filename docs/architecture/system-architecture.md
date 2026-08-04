# System Architecture

**Purpose:** Define the accepted functional partition of the XJ900S OEM+
architecture without selecting component implementations or interfaces.

**Document status: Draft**

The functional partition is accepted; interfaces and component implementations
remain incomplete.

## Architectural principles

**Status: Accepted**

- Engine-critical control remains in the engine-management system.
- Non-engine body-control functions may be separated where this improves
  modularity, reliability, serviceability, or testability.
- Optional and future systems shall not compromise basic engine operation.
- Interfaces between control domains shall be explicit and documented.
- The architecture supports staged implementation and independent subsystem
  testing, prefers proven production components where practical, and avoids
  unnecessary coupling and unnecessary single points of failure.
- Safety-critical behavior uses defined safe states where technically
  applicable.
- Future expansion is prepared for without requiring every future function in
  the initial implementation.

## Requirement traceability

This architecture primarily implements the accepted requirements ARC-001
through ARC-008 and supports SYS-010 through SYS-012, SAF-001 through SAF-007,
and applicable development and documentation requirements.

## System context

The motorcycle contains these high-level domains: engine and fuel; ignition;
electrical power distribution; rider controls; lighting and signaling;
instrumentation and diagnostics; safety functions; and optional future chassis
and rider-assistance systems. Not all domains are implemented in the first
stage.

## Three-level functional architecture

| Level | Control domain | Primary responsibility | Initial implementation status | Safety significance |
| --- | --- | --- | --- | --- |
| 1 | Engine-management system | Direct control of engine operation and engine-critical safety behavior | Required for EFI conversion | Safety-critical |
| 2 | Separate body-control or supervisory unit | Non-engine functions, coordination, and selected safety-supporting functions without direct real-time engine control | May be implemented in stages | Mixed; shall not replace engine-critical control |
| 3 | Future-ready systems | Optional later expansion not required for initial reliable operation | Interfaces and provisions only unless separately accepted | Must not compromise Level 1 operation |

## Level 1: Engine-management system

Level 1 contains functions that must remain in the engine-management system
because they directly affect combustion, engine operation, or immediate
engine-safe behavior.

- Crankshaft position and engine-speed acquisition; camshaft position where
  required by the selected strategy; engine phase and synchronization.
- Fuel-injection timing and quantity control; ignition timing and coil control;
  throttle-position sensing required for engine control.
- Air-temperature, engine-temperature, and manifold-pressure or equivalent
  engine-load sensing; wideband oxygen-sensor input for calibration,
  monitoring, or closed-loop control.
- Engine-state management; starting and cranking logic; idle control where
  used; fuel-pump command or fuel-pump safety control.
- Engine shutdown following a valid detected fall or tip-over condition;
  engine-related fault detection; and defined engine-safe responses where
  technically applicable.
- Direct drive-by-wire throttle control only if a later accepted design uses it.

The architecture does not select a specific ECU, throttle-body assembly,
injector, ignition coil, sensor part number, or idle-control implementation.

Review: Technical Review Required

Level 1 functions require technical review and validation before road use.

## Level 2: Separate body-control or supervisory unit

Level 2 may contain functions that benefit from separation from engine
management and do not require direct combustion-cycle control.

- Rider-control input handling not required directly by Level 1; lighting,
  turn-signal, brake-light, horn, auxiliary-relay, accessory-power, and
  heated-grip control.
- Instrumentation data aggregation; warning and tell-tale coordination;
  non-engine diagnostic coordination; system-state monitoring; selected
  power-management functions; controlled shutdown or wake-up coordination.
- Interface handling between legacy circuits and modern controls; fall-sensor
  signal distribution while Level 1 retains engine-shutdown authority; and
  service and test interfaces for body-control functions.

- Level 2 shall not be required for basic combustion control.
- A Level 2 failure shall not unintentionally command fuel or ignition.
- Level 2 may request or report state changes through an approved interface,
  but engine-critical authority remains in Level 1.
- Safety-supporting Level 2 functions require separate technical review.
- No specific microcontroller, PDM, CAN controller, relay module, or production
  body-control unit has been selected.

Review: Technical Review Required

This review applies only to Level 2 functions that influence safety-related
behavior, such as brake-light logic, power management, warning coordination,
or fall-sensor signal distribution.

## Level 3: Future-ready functions

Level 3 contains optional functions for which the initial architecture should
preserve space, interfaces, data availability, or expansion paths without
making them mandatory for first-stage operation.

**Partition status: Accepted**

The listed future functions are candidates rather than initial implementation
requirements.

**Function status: Proposal**

- Front and rear wheel-speed sensing; advanced traction-control support; ABS
  integration or coordination; inertial measurement unit integration; and
  lean-angle-aware functions.
- Advanced rider modes; electronic-suspension interfaces; centralized
  power-distribution integration; advanced display or connected
  instrumentation; data logging beyond initial commissioning; vehicle-network
  expansion; navigation or communication integration; and additional
  diagnostic and telemetry functions.

- Level 3 functions are not accepted as initial implementation requirements.
- Level 3 shall not be required for basic engine operation.
- Failure or absence of a Level 3 subsystem shall not prevent normal Level 1
  operation unless a later accepted safety architecture explicitly requires it.
- No claim is made that the original motorcycle, selected donor components, or
  current engine-management candidate supports all Level 3 functions.

## Cross-level interfaces

- Every cross-level interface shall have a documented purpose, explicit signal
  direction, and control authority.
- Safety-critical commands shall have one clearly defined authority. Invalid,
  missing, implausible, or stale data shall have defined handling where
  technically applicable.
- Optional data consumers shall not become hidden dependencies for required
  engine operation. Interfaces shall support bench testing and fault simulation
  where practical.
- Electrical interfaces shall consider voltage levels, grounding, protection,
  electromagnetic disturbance, and failure behavior. Logical interfaces shall
  consider update rate, timeout, validity, startup, shutdown, and diagnostics.
- The architecture may use discrete, analog, serial, or vehicle-network
  signals; no protocol is selected here.

## Failure containment and safe-state principles

- Failure domains should be contained where practical. Lighting,
  instrumentation, accessory, or convenience failures shall not unintentionally
  stop a healthy engine unless required for safety.
- Failure of an optional future function shall not cause uncontrolled engine
  behavior. Fuel, ignition, and throttle authority remain under clearly defined
  engine-management control.
- Loss of a safety-critical input shall produce a documented response
  appropriate to the risk. A detected fall or tip-over shall cause engine and
  fuel shutdown and require deliberate restart or reset action.
- Recovery from faults shall not depend on undocumented behavior. Safe-state
  design remains subject to technical review and later validation.

Review: Technical Review Required

## Development and validation boundaries

- Each level shall be testable independently where practical. Level 1 shall be
  bench-tested before integrated road testing.
- Level 2 functions shall be tested without unintended Level 1 commands; Level
  3 interfaces shall be tested as optional dependencies.
- Interface tests shall include normal operation, startup, shutdown, loss of
  signal, implausible signal, and recovery where relevant.
- Road testing shall occur only after prerequisite safety validation.
- Architectural compliance shall be traceable to requirements and test evidence.

## Open architecture questions

Status: Unverified

- Final engine-management platform; final throttle-control strategy; and
  whether camshaft position is mandatory for the selected strategy.
- Final division of fall-sensor processing between Levels 1 and 2; final
  body-control implementation; and power-distribution architecture.
- Communication protocol; grounding and reference strategy; diagnostic and
  instrumentation architecture; and required wheel-speed interfaces.
- Future ABS and IMU integration boundaries; limp-home and degraded-operation
  architecture; startup, shutdown, and wake-up sequencing; and final safe-state
  definitions for each credible fault.

## Navigation

[Documentation index](../INDEX.md) | [System requirements](../requirements/system-requirements.md) | [Decisions](../decisions/README.md)
