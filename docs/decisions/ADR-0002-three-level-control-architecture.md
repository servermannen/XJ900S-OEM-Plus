# ADR-0002: Three-Level Control Architecture

**Purpose:** Record the accepted functional separation between engine control,
body control, and future-ready systems.

**Status: Accepted**

## Context

Modernization introduces engine management, rider controls, lighting,
instrumentation, power management, safety functions, and optional future
systems. A single controller could create unnecessary coupling, while
uncontrolled modules could create unclear authority and hidden dependencies.

## Decision

The motorcycle uses three functional levels: Level 1 engine management, Level
2 separate body control or supervision, and Level 3 future-ready systems. This
defines functional ownership and authority, not final hardware implementation.
ECU, body controller, power hardware, protocol, and donor components remain
future decisions.

## Level 1: Engine-management system

Level 1 owns combustion, engine operation, and immediate engine-safe behavior:
engine position and speed, synchronization, fuel injection, ignition, load and
temperature sensing, throttle inputs, starting and idle functions where used,
fuel-pump safety, fault handling, and shutdown for a valid fall or tip-over.
Drive-by-wire authority applies only to a later accepted design.

- Level 1 retains fuel, ignition, and direct engine authority.
- Level 1 shall not depend on Level 2 or Level 3 for basic engine operation
  unless a later accepted safety architecture requires it.
- Level 1 is safety-critical.

Review: Technical Review Required

## Level 2: Separate body-control or supervisory unit

Level 2 may own lighting, signaling, horn, accessories, heated grips,
non-engine rider inputs, warnings, instrumentation aggregation, body
diagnostics, selected power management, legacy-circuit adaptation, and
fall-sensor distribution while Level 1 retains shutdown authority.

- Level 2 shall not own direct fuel or ignition control or be required for
  basic combustion control.
- Level 2 may exchange documented state, requests, warnings, and diagnostics.
- A Level 2 failure shall not unintentionally command fuel, ignition, or
  throttle actuation. Level 2 may be introduced in stages.
- Only safety-influencing Level 2 functions require review.

Review: Technical Review Required

This review applies only to safety-supporting Level 2 functions.

## Level 3: Future-ready systems

Level 3 provides provisions for wheel-speed sensing, traction-control support,
ABS coordination, IMU integration, rider modes, suspension interfaces, future
power distribution, advanced instrumentation, logging, telemetry, and network
expansion.

**Function status: Proposal**

- Level 3 is an accepted category, but its functions are not initial
  implementation requirements.
- Level 3 shall not be required for basic engine operation; its absence or
  failure shall not compromise Level 1.
- Each future function requires requirements, research, a decision, and
  validation before implementation.

## Control-authority boundaries

- Every safety-critical command shall have one clearly defined authority.
- Fuel, ignition, and direct engine authority remain in Level 1.
- Level 2 and Level 3 may provide information or requests but shall not gain
  hidden engine-control authority.
- Interfaces shall define direction, ownership, validity, timeouts, startup,
  shutdown, and fault handling where applicable. No protocol is selected.

## Consequences

### Positive consequences

The partition improves modularity, fault containment, staged implementation,
independent testing, diagnosis, serviceability, and controlled expansion.

### Trade-offs and constraints

Interfaces require design and documentation. Multiple control units can increase
wiring, integration, testing, and coordination. This ADR selects neither
hardware nor compatibility.

## Safety implications

Level 1 requires review before road use. Safety-supporting Level 2 functions
require review where their failure affects safety. Level 3 shall not cause
uncontrolled engine behavior. A valid fall or tip-over shall shut down engine
and fuel and require deliberate restart or reset. Detailed safe states,
degraded behavior, and fault recovery remain future work.

Review: Technical Review Required

## Requirement traceability

This ADR records ARC-001 through ARC-008 and supports SYS-010 through SYS-012,
SAF-001 through SAF-007, and applicable reliability, serviceability,
development, and documentation requirements. It does not claim complete
implementation traceability.

## Related documents

- [System architecture](../architecture/system-architecture.md)
- [System requirements](../requirements/system-requirements.md)
- [ADR-0001: Project Principles](ADR-0001-project-principles.md)
- [Decision register](README.md)
- [Documentation index](../INDEX.md)

## Supersession

This ADR is not superseded.

A future change to the partition, control authority, or safety boundaries shall
require a new ADR that explicitly supersedes this record.
