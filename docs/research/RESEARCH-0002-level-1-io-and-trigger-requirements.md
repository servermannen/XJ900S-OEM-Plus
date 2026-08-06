# RESEARCH-0002: Level 1 I/O and trigger requirements

**Purpose:** Define Level 1 engine-management I/O and trigger requirements before ECU hardware, including rusEFI hardware, can be evaluated.

**Document status: Draft**

Status: Unverified

Review: Technical Review Required

## Research question

What engine-management inputs, outputs, trigger functions, safety signals, and diagnostic interfaces are required for the XJ900S OEM+ Level 1 system before an ECU hardware platform can be evaluated?

## Scope

### Included

- Cylinder/ignition topology; fuel, ignition, crank/cam, analog, digital, safety, pump, idle, auxiliary, wideband, throttle, diagnostic, logging, power, grounding, wake-up, spare-capacity, bench-test, and fault-injection I/O.
- Measurements and decisions required before hardware selection.

### Excluded

- Final ECU, trigger wheel, sensor, throttle body, injector, ignition coil, idle hardware, DBW, pinout, connector, Level 2 controller, Level 3 function, calibration value, or numerical electrical limit.

## Current system assumptions

Status: Unverified

These research inputs are not all confirmed implementation facts.

- The engine is an air-cooled inline four-cylinder four-stroke engine; the
  project intends electronically controlled fuel injection and ignition.
- Four cylinders require individual or grouped fuel and ignition control.
- Level 1 retains direct authority over fuel, ignition, engine state, and engine shutdown.
- Cable throttle remains valid initially; DBW is a separately evaluated future option.
- A crankshaft-position input is an accepted mandatory Level 1 function. Its
  sensor, technology, trigger pattern, location, mounting, signal conditioning,
  offset, decoder, and final implementation remain open.
- A fall or tip-over sensor is an accepted project requirement. Level 1 retains
  engine and fuel-pump shutdown authority, while sensor model, orientation,
  signal type, thresholds, plausibility, reset behavior, missing-signal
  behavior, wiring, and implementation remain open.
- Level 1 remains independent of optional Level 2 and Level 3 systems for basic operation.
- Bench testing precedes installed critical-output testing where practical.

Exact timing references, trigger geometry, sensor signal types, and actuator electrical characteristics require verification.

## Requirement classes

- **Mandatory initial function or planning path:** needed for initial Level 1
  operation, development, or calibration without selecting its implementation.
- **Final-target or strongly preferred function:** evaluated for the intended
  final architecture without making it an initial dependency or accepted
  component decision.
- **Strategy-dependent I/O:** needed only by an accepted control strategy.
- **Safety-critical I/O:** affects fuel, ignition, state, or shutdown.
- **Optional initial I/O:** useful but not required for basic operation.
- **Future-reserved I/O:** provision without initial dependency.
- **Diagnostic and test interfaces:** configuration, observation, testing, and service.

Hardware comparison shall distinguish these classes rather than treating every possible function as mandatory.

## Sensor architecture planning baseline

The classifications below describe functional planning paths. They do not
select a sensor, mounting location, signal range, calibration, connector,
pinout, ECU board, or fallback behavior.

| Function | Planning class | Function status | Implementation status | Boundary |
| --- | --- | --- | --- | --- |
| Crankshaft position | Mandatory initial | Accepted | Unverified | Sensor, pattern, conditioning, offset, and decoder remain Unverified. |
| Throttle position | Mandatory initial | Proposal | Unverified | Cable throttle is permitted initially; no throttle body, TPS, cable arrangement, or idle strategy is selected. |
| MAP or accepted equivalent load signal | Mandatory initial | Proposal | Unverified | The equivalent load method requires evidence and acceptance. |
| Intake-air temperature | Mandatory initial | Proposal | Unverified | Sensor, location, range, and calibration remain open. |
| Engine temperature appropriate for an air-cooled engine | Mandatory initial | Proposal | Unverified | Cylinder-head temperature, oil temperature, or another validated engine-temperature proxy may be evaluated; none is selected. |
| Battery or system voltage | Mandatory initial | Proposal | Unverified | The path may be internal or external; range, accuracy, and fault handling remain open. |
| Fall or tip-over input | Mandatory initial | Accepted | Unverified | Sensor model, orientation, interface, thresholds, plausibility, reset, missing-signal behavior, and wiring remain Unverified. |
| Practical wideband-oxygen interface | Mandatory initial development and calibration path | Proposal | Unverified | Analog, digital, or network interface and external controller remain open. |
| Level 1 fuel-pump command and shutdown authority | Mandatory initial | Accepted | Unverified | Output circuit, prime logic, timeout, filtering, and relay or driver implementation remain open. |
| Cam phase | Final target or strongly preferred | Proposal | Unverified | Needed to evaluate full 720-degree phase identification; initial crank-only development shall not depend on it. |
| Fuel-pressure monitoring | Final target or strongly preferred | Proposal | Unverified | Sensor, range, mounting, and protective response remain open. |
| Oil-pressure warning or monitoring | Final target or strongly preferred | Proposal | Unverified | Switched or analog path and response remain open. |
| Knock sensing | Optional or later evaluation | Proposal | Unverified | It shall not become an initial Level 1 dependency. |
| Wheel-speed inputs | Optional or later evaluation | Proposal | Unverified | They remain Level 3-facing unless a later accepted architecture requires them. |
| DBW-related redundant sensing | Future-reserved | Proposal | Unverified | It is required only if a dedicated future decision accepts DBW. |
| Additional thermal measurements | Optional or later evaluation | Proposal | Unverified | These supplement, but do not replace without validation, the mandatory engine-temperature path. |

Availability, published specification, physical compatibility, electrical
compatibility, functional compatibility, safety suitability, and final
acceptance shall be evaluated separately for every later component candidate.

## Fuel-injection outputs

The platform shall support four-cylinder fuel delivery. Four independent outputs are preferred for sequential capability and calibration flexibility; fewer require a separately accepted grouped or batch strategy.

Preliminary requirement: Four independently controllable injector outputs

Status: Proposal

Review: Technical Review Required

Safe non-fuel bench loads are required. Protection, current, flyback, and failure behavior require verification against selected injectors. Final acceptance depends on synchronization strategy and injector selection.

## Ignition outputs

The platform shall support all four cylinders. Four independent commands preserve coil-on-plug or cylinder-specific control; two may suffice only with separately accepted wasted spark and compatible hardware.

Preliminary requirement: Four independently controllable ignition commands

Status: Proposal

Review: Technical Review Required

Commands may be logic-level or power-driving depending on later coil/module selection. Safe-load testing is required. This does not require four built-in high-current coil drivers.

## Crankshaft trigger requirements

Crankshaft position is mandatory for engine-speed determination and angular synchronization through cranking, starting, idle, and the operating range.

**Status: Accepted**

Review: Technical Review Required

The need for crankshaft-position sensing is accepted, while trigger pattern,
tooth count, sensor type, placement, and conditioning remain unverified.
Cranking quality, loss, implausible timing, and stale input need defined
handling. Direction detection is not accepted. Final pattern selection precedes
ECU acceptance.

## Camshaft trigger requirements

Cam position is required where the strategy needs full phase identification and is preferred for sequential fuel, cylinder-specific ignition, faster synchronization, and diagnostics. Crank-only operation requires documented justification.

Preliminary requirement: At least one camshaft-position input

Status: Proposal

Review: Technical Review Required

Sensor, target, edges, phase, and conditioning remain open. Hardware evaluation shall verify cam-input capability even if initial operation is crank-only.
Cam input is safety-relevant where used for phase control.

## Synchronization strategy

### Controlled first-start development stage

Status: Proposal

The first controlled EFI start may use crankshaft synchronization only,
wasted-spark ignition, and grouped, batch, or semi-sequential injection. It may
have no dependency on a cam sensor and shall use a limited operating range,
conservative ignition, and defined fuel-pump shutdown following loss of valid
crankshaft rotation. This is a development and validation stage, not an
accepted final road configuration.

### Final synchronization target

Status: Proposal

Evaluate a sufficiently high-resolution crank trigger plus a separate
cam-phase signal for full 720-degree phase identification, sequential-injection
capability, individually controlled ignition capability, and diagnosable
crank/cam correlation. Sequential operation, a trigger pattern, a sensor, and a
decoder are not accepted by this proposal.

Both stages require evaluation of synchronization time, noise robustness,
recovery, phase accuracy, firmware support, bench testing, diagnostics, and
safe uncertainty behavior. The strategy shall be accepted before final ECU
selection.

## Analog input requirements

| Input ID | Function | Classification | Signal category | Safety relevance | Status |
| --- | --- | --- | --- | --- | --- |
| AIN-001 | Throttle position | Mandatory initial | Analog position | Safety-relevant | Unverified |
| AIN-002 | MAP or equivalent load | Mandatory initial | Analog load | Engine-critical | Unverified |
| AIN-003 | Intake-air temperature | Mandatory initial | Analog temperature | Engine-critical | Unverified |
| AIN-004 | Engine temperature appropriate for an air-cooled engine | Mandatory initial | Analog temperature or another validated path | Engine-critical | Unverified |
| AIN-005 | Wideband-controller output, if the selected interface uses analog signaling | Mandatory initial development/calibration path | Analog oxygen output | Safety-relevant | Unverified |
| AIN-006 | Battery/system voltage | Mandatory initial | Analog or internal | Safety-relevant | Unverified |
| AIN-007 | Fuel pressure | Final target or strongly preferred | Analog pressure | Safety-relevant | Unverified |
| AIN-008 | Oil-pressure sensing, if analog sensing is selected | Final target or strongly preferred | Analog pressure | Safety-relevant | Unverified |
| AIN-009 | Additional oil-temperature measurement, where oil temperature is not already the selected mandatory engine-temperature path | Optional or later evaluation | Analog temperature | Optional | Unverified |
| AIN-010 | Spare analog capacity | Future-reserved | Unspecified | Not applicable | Unverified |

Exact voltage ranges and calibration curves are Unverified. At least one spare analog channel is preferred; final reserve count is not accepted.

The XJ900S is air-cooled. No coolant-temperature sensor is assumed. Candidate
engine-temperature paths include cylinder-head temperature, oil temperature,
or another validated proxy, but no sensor or location is selected.
One physical sensor/input shall not be double-counted in the I/O budget as both
AIN-004 and AIN-009.

## Digital and switched input requirements

| Input ID | Function | Authority | Absence behavior | Required handling | Status |
| --- | --- | --- | --- | --- | --- |
| DIN-001 | Key-on state | Direct | Defined operation/shutdown | Debounce, plausibility | Unverified |
| DIN-002 | Starter request | Direct or approved derived | Diagnostics or inhibit as strategy requires | Debounce, plausibility | Unverified |
| DIN-003 | Fall or tip-over signal | Level 1 shutdown authority | Valid activation requires shutdown and deliberate reset; missing or invalid input behavior remains to be defined | Plausibility, timeout, fault detection, fail-safe behavior | Unverified |
| DIN-004 | Clutch switch where used | Direct or approved derived | Degraded operation/diagnostics unless required | Debounce, plausibility | Unverified |
| DIN-005 | Neutral switch where used | Direct or approved derived | Degraded operation/diagnostics unless required | Debounce, plausibility | Unverified |
| DIN-006 | Side stand where used | Direct or approved derived | Defined by accepted safety logic | Debounce, plausibility, timeout, fail-safe | Unverified |
| DIN-007 | Kill switch | Direct | Stop or block operation | Debounce, plausibility, fail-safe | Unverified |
| DIN-008 | Vehicle/wheel speed if later required | Approved interface | No initial Level 1 dependency | Plausibility, timeout | Proposal |
| DIN-009 | Calibration/service mode | Direct | Diagnostics unless accepted otherwise | Debounce, plausibility | Unverified |
| DIN-010 | Spare digital capacity | Future-reserved | Not applicable | To be defined | Unverified |
| DIN-011 | Oil-pressure switch, if switched sensing is selected | Direct or approved derived | Warning or defined protective response | Debounce and plausibility where applicable | Unverified |

Final logic states and wiring polarity are open. Safety-related inputs require Review: Technical Review Required.

The accepted fall-sensor requirement does not accept a component or signal
behavior. A valid fall event requires fuel-pump command off, injector commands
off, ignition commands off, and deliberate reset or restart behavior. Exact
detection, timing, and recovery details require technical review and validation.

## Fuel-pump, idle, and auxiliary outputs

Level 1 shall control and retain safety authority over fuel-pump operation.
Prime, cranking, running, stall, shutdown, fall-event, and engine-speed-loss
behavior need definition and independent bench testing. Level 2 shall not gain
hidden fuel-pump or engine authority.

Preliminary requirement: One fuel-pump command output

Status: Proposal

Review: Technical Review Required

Idle approaches may be no actuator, on/off or PWM valve, stepper controller, or DBW idle if later accepted. Output count/type remain strategy-dependent; record supported methods and retain one practical path unless testing supports no-actuator operation.

Status: Unverified

| Function | Classification | Status |
| --- | --- | --- |
| Main/ECU relay; cooling fan if required | Strategy-dependent | Unverified |
| Tachometer; malfunction/diagnostic indicator | Optional initial | Unverified |
| Wideband enable/heater coordination | Strategy-dependent | Unverified |
| Boost/variable control | Not currently required | Unverified |
| Spare low-side/logic outputs | Future-reserved | Unverified |
| Level 2 status/request interface | Strategy-dependent | Unverified |

Cooling-fan control is not assumed mandatory. Level 2 interfaces shall not transfer direct engine authority.

## Wideband oxygen interface

Wideband sensing is required for calibration and monitoring; closed-loop use is strategy-dependent. The interface may be analog, digital, or network-based, with an external controller where needed. Verify a practical interface; heater/power may remain external and fault behavior is open.

Preliminary requirement: One practical wideband oxygen input path

Status: Proposal

The practical development and calibration path is mandatory for planning; the
interface technology and hardware remain proposed and unverified.

## Throttle strategy

### Cable throttle

Cable throttle is accepted as a permitted initial strategy. This does not
constitute a final throttle-strategy selection. Level 1 requires
throttle-position sensing; redundant sensing is not accepted as mandatory for
cable throttle. DBW shall not be required solely for future features.

**Status: Accepted**

### Drive-by-wire

DBW is optional and future-facing. Direct DBW needs redundant sensing, actuator outputs, plausibility, independent safety analysis, safe states, faults, and extensive validation. No initial DBW I/O count is mandatory until a dedicated ADR accepts DBW; capability may be recorded comparatively.

Function status: Proposal

Review: Technical Review Required

Knock sensing, wheel-speed input, DBW-related redundant sensing, and additional
thermal measurements shall not become hidden dependencies for initial Level 1
operation.

## Safe states and fault behavior

Review: Technical Review Required

### Crank-signal loss or invalidity

Status: Proposal

Review: Technical Review Required

- Fuel-injection commands shall stop.
- Ignition commands shall stop.
- The fuel pump shall be switched off after a defined and validated timeout.
- Implausible frequency or an invalid trigger sequence shall not cause fuel or
  ignition output.
- Exact timeout, filtering, thresholds, diagnostics, recovery, and restart
  behavior remain Unverified.

### Cam-signal loss

Status: Proposal

Behavior before start and during running shall be defined separately. No
fallback mode is assumed. Any fallback to grouped injection or wasted spark
requires experimental validation and technical review before acceptance.

### Fall-event activation

Status: Accepted

- Fuel-pump command off.
- Injector commands off.
- Ignition commands off.
- Deliberate reset or restart behavior required.

Fault testing shall include disconnected sensors, intermittent connections,
false edges or noise, low cranking voltage, hot sensors, start/stop
transitions, resynchronization, and loss during controlled operation. No
"limp-home" behavior is defined without a dedicated safety analysis.

## Diagnostic, power, and ECU-state interfaces

Require calibration connection, live sensor/state and output visibility, fault codes, trigger diagnostics, logs, version identification, export, rollback, and accessible service. Protocol remains open.

Preliminary requirement: At least one practical calibration and diagnostic interface

Status: Proposal

Consider battery, switched wake, relay control where used, grounds, sensor supply, brownout/reset, cranking voltage, reverse-polarity/transient protection, key-off shutdown, and power-interruption recovery. Exact limits are unverified.

Review: Technical Review Required

## Preliminary I/O count

| Function class | Preliminary minimum | Preferred planning count | Status | Notes |
| --- | --- | --- | --- | --- |
| Injector commands | Strategy-dependent | 4 | Proposal | Depends on fuel strategy. |
| Ignition commands | Strategy-dependent | 4 | Proposal | Commands, not driver implementation. |
| Crank inputs | 1 | 1 dedicated | Proposal | Pattern unverified. |
| Cam inputs | Strategy-dependent | 1 | Proposal | Strategy open. |
| Mandatory analog inputs | 4 | 4 | Proposal | TPS, MAP or equivalent load, intake-air temperature, and engine temperature. |
| Wideband interface path | 1 practical interface | 1 practical interface | Proposal | May be analog, digital, or network-based. |
| Battery/system-voltage path | 1 practical path | 1 practical path | Proposal | May be internal or external; implementation unverified. |
| Preferred analog capacity | Not applicable | At least 7 including reserve | Proposal | Reserve not accepted. |
| Safety/engine digital inputs | Not finalized | Not finalized | Unverified | Depends on strategy. |
| Fuel-pump command | 1 | 1 | Proposal | Level 1 authority. |
| Idle/warning/tach outputs | Strategy-dependent | Strategy-dependent | Unverified | Interface open. |
| Diagnostic interface | At least 1 practical | At least 1 practical | Proposal | Protocol open. |
| Spare I/O | Preferred | Count unverified | Proposal | Does not override reliability. |

Battery monitoring may be internal and must not automatically count as external analog input. This is not a final hardware acceptance checklist.

## Spare capacity and bench testing

Reserve analog, digital, and auxiliary-output capacity is preferred, but shall not override reliability, documentation, availability, or environmental suitability. Exact count is unverified; Level 3 normally remains outside Level 1.

- Simulate crank/cam signals and sensors; use safe injector/ignition-command loads; observe pump and fall activation.
- Simulate starter/key, input faults, power interruption, and brownout; verify logs, diagnostics, startup, sync, shutdown, and recovery.
- Use no installed fuel or ignition energy during early tests where practical.

Review: Technical Review Required

## Open measurements and decisions

Status: Unverified

- Exact 1997 ignition topology, crank/cam locations, resolution, packaging,
  sensor type/amplitude, and cranking waveform quality.
- Synchronization strategy; injector/ignition electrical characteristics; TPS, MAP, temperature, and idle strategy.
- Safety signal derivation; pump, tach/warning, spare capacity, power/ground/transient, protocol, calibration, and DBW decisions.

## Research outputs

- Accepted Level 1 I/O list and trigger/synchronization strategy.
- Preliminary signal/electrical specification, ECU screening checklist, bench-test matrix, component criteria, and new requirements or ADRs.

## Preliminary conclusion

The accepted functional baseline requires crank sensing, Level 1 engine and
fuel-pump shutdown authority, and a fall or tip-over sensor without accepting
their implementations. The planning baseline includes throttle position, MAP
or an accepted equivalent load signal, intake-air temperature, an appropriate
air-cooled-engine temperature path, battery/system voltage, and a practical
wideband interface. A crank-plus-cam final target, fuel-pressure monitoring,
oil-pressure warning or monitoring, four injector commands, and four ignition
commands remain proposals rather than accepted hardware requirements.

No ECU hardware shall be accepted solely because its published I/O count appears sufficient.

## Decision impact

- Related research: [RESEARCH-0001](RESEARCH-0001-engine-management-platform.md)
  and [RESEARCH-0003](RESEARCH-0003-trigger-and-synchronization-strategy.md).
- Related requirements: SYS-007 through SYS-009, SYS-013, SAF-001, SAF-003,
  SAF-004, SAF-007, SAF-008, and applicable REL, SRV, ARC, and DEV requirements.
- Related architecture: Level 1; related roadmap stage: Stage 2 and Stage 3.
- ADR required: Yes, for trigger/control-strategy decisions. Component evaluation required: Yes. Bench testing required: Yes.
- Recommended next action: Execute
  [TEST-PLAN-0001](../testing/TEST-PLAN-0001-original-pickup-characterization.md)
  only after its review gates are satisfied, then use its evidence in
  RESEARCH-0003 and the later decoder-validation plan before selecting trigger
  or ECU hardware.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-06 | Consolidated staged synchronization, air-cooled temperature sensing, fall-sensor, monitoring, and safe-state planning. | Separate accepted functions from proposed targets and unverified implementations before hardware evaluation. |
| 2026-08-04 | Created initial research record. | Define I/O and trigger research before ECU hardware comparison. |

## Navigation

[Research index](README.md) | [RESEARCH-0001](RESEARCH-0001-engine-management-platform.md) | [RESEARCH-0003](RESEARCH-0003-trigger-and-synchronization-strategy.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [Test strategy](../testing/test-strategy.md) | [TEST-PLAN-0001](../testing/TEST-PLAN-0001-original-pickup-characterization.md) | [TEST-PLAN-0002](../testing/TEST-PLAN-0002-trigger-decoder-and-timing-validation.md) | [Documentation index](../INDEX.md)
