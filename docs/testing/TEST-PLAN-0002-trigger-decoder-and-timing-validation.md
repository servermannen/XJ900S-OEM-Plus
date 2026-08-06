# TEST-PLAN-0002: Trigger decoder and timing validation

## Purpose

Define a future, staged plan to validate whether a characterized crank signal
can be safely and repeatably decoded by an exactly identified Level 1 ECU
configuration and whether commanded ignition timing matches measured timing.

**Document status: Draft**

**Execution status: Not started**

**Test result: Not available**

Review: Technical Review Required

No rusEFI board, other ECU board, input circuit, firmware version, trigger
decoder, crank sensor, cam sensor, trigger pattern, or final strategy is
accepted by this plan. No test has been executed.

## Test identification

| Field | Planned record |
| --- | --- |
| Test ID | TEST-PLAN-0002 |
| Test type | Bench, passive motorcycle cranking, stationary fixed-timing validation, and fault injection |
| Related requirements | SYS-007 through SYS-009, SYS-013; SAF-001, SAF-003, SAF-004, SAF-007, SAF-008; ARC-001, ARC-003, ARC-006 through ARC-008; DEV-002 through DEV-008 |
| Architecture reference | [Level 1 engine-management system](../architecture/system-architecture.md#level-1-engine-management-system) |
| Related research | [RESEARCH-0002](../research/RESEARCH-0002-level-1-io-and-trigger-requirements.md) and [RESEARCH-0003](../research/RESEARCH-0003-trigger-and-synchronization-strategy.md) |
| Predecessor evidence | [TEST-PLAN-0001](TEST-PLAN-0001-original-pickup-characterization.md) |
| Roadmap stages | Stage 3 concept validation, Stage 4 bench system, and only the reviewed stationary portion of Stage 5 |

## Scope

### Included

- Exact selected ECU-board identification and hardware revision.
- Exact firmware build or commit and configuration identification.
- Trigger-input type, VR or Hall interface, input protection, and grounding.
- Recorded-waveform replay or signal-generator testing where supported.
- Passive installed motorcycle cranking with all fuel, injector, and ignition
  control disabled.
- Raw oscilloscope evidence, ECU trigger logs, synchronization state, and
  decoder error records.
- Fixed-commanded-timing validation after passive decoding is stable and a
  separate live-ignition method is technically reviewed.
- Crank-loss, intermittent-connection, missing-event, false-event, noise,
  voltage, temperature, stop/start, and resynchronization fault injection.

### Excluded

- Road testing.
- Fuel tuning or final fuel mapping.
- Final ignition mapping.
- Full-power or high-load operation.
- Final ECU, sensor, trigger, decoder, input-circuit, or synchronization
  acceptance without completed evidence and technical review.
- Parallel connection to the original TCI before input loading and grounding
  are analysed and technically reviewed.
- Ignition-primary or ignition-secondary oscilloscope probing.
- Definition of limp-home behavior without a dedicated safety analysis.

## Tested-configuration record

All fields are initially unrecorded. A test configuration is not traceable or
eligible for execution until every applicable field is completed.

| Configuration field | Recorded value | Initial state |
| --- | --- | --- |
| ECU manufacturer and board name | Not recorded | Unverified |
| ECU board serial number or identifier | Not recorded | Unverified |
| Hardware revision | Not recorded | Unverified |
| Firmware build, release, or commit | Not recorded | Unverified |
| Configuration/calibration file and checksum | Not recorded | Unverified |
| Trigger decoder name and configuration | Not recorded | Unverified |
| Trigger-input type | Not recorded | Unverified |
| Exact crank input pin or pins | Not recorded | Unverified |
| Exact cam input pin or pins, if used | Not recorded | Unverified |
| VR/Hall interface and revision | Not recorded | Unverified |
| Input protection | Not recorded | Unverified |
| Signal-conditioning settings | Not recorded | Unverified |
| Pull-up configuration where relevant | Not recorded | Unverified |
| VR polarity where relevant | Not recorded | Unverified |
| Sensor and ECU ground references | Not recorded | Unverified |
| Input voltage limits | Not recorded | Unverified |
| Unipolar or bipolar input behavior | Not recorded | Unverified |
| Logging tool and version | Not recorded | Unverified |
| Oscilloscope, probes, and configuration | Not recorded | Unverified |
| Signal generator or replay hardware and version | Not recorded | Unverified |
| Safe bench loads | Not recorded | Unverified |
| Output-disable method | Not recorded | Unverified |
| Fuel-pump disable method | Not recorded | Unverified |
| Injector disable method | Not recorded | Unverified |
| Ignition disable method | Not recorded | Unverified |
| Original TCI connection state | Not recorded | Unverified |
| Motorcycle identifier | Not recorded | Unverified |
| Engine identifier | Not recorded | Unverified |
| Test date, time, location, and operator | Not recorded | Unverified |

## Preconditions

### Evidence and configuration preconditions

1. TEST-PLAN-0001 evidence applicable to the proposed signal shall be complete,
   retained, and reviewed for the intended phase.
2. The exact ECU board and hardware revision shall be identified.
3. The exact crank and applicable cam input pins shall be verified against
   authoritative documentation for that board revision.
4. Input voltage limits and unipolar or bipolar input behavior shall be
   verified.
5. Pull-up configuration shall be documented where relevant.
6. VR polarity shall be documented where a VR signal is used.
7. Shared grounds, shield handling, and reference points shall be documented
   and technically reviewed.
8. The complete signal-conditioning path and settings shall be documented.
9. The firmware build, release, or commit and trigger-decoder configuration
   shall be recorded.
10. Logging tools, time correlation, export formats, and storage paths shall be
    verified.
11. Safe bench loads shall be identified for any enabled output test.
12. Output-disable, fuel-pump-disable, injector-disable, and ignition-disable
    methods shall be documented, checked, and fail-safe for the planned phase.
13. Input protection and any external interface circuit shall be documented and
    reviewed.
14. Supply-current limits, power sequencing, grounding, and emergency power-off
    shall be defined for bench work.
15. The waveform replay or signal-generator source shall be verified not to
    exceed ECU input limits or create an unintended ground path.

Review: Technical Review Required

### Original-TCI parallel-connection prohibition

**Execution status: Blocked**

Do not connect the candidate ECU input in parallel with the original TCI until
the input impedance, biasing, clamps, loading, ground references, failure
effects, and interaction with the original pickup and TCI have been analysed
and technically reviewed. Connector availability or a similar voltage range is
not compatibility evidence.

## Hazards, protective measures, and safe states

| Hazard | Required protective measure | Required safe state |
| --- | --- | --- |
| Unintended fuel-pump operation | Physically or electrically verified disable for replay and passive cranking | Fuel-pump command and pump energy off |
| Unintended injector command | Verified output disable and disconnected or safe-load state | Injector commands and fuel delivery off |
| Unintended ignition command | Verified output disable and controlled coil state | Ignition commands and ignition energy off |
| False high-RPM decoding | Output disable, RPM plausibility monitoring, stop condition | No fuel, ignition, or pump output |
| Ground loop or input overvoltage | Reviewed grounding diagram, verified probes, input protection, current-limited bench source where applicable | De-energize ECU and signal source |
| Unexpected engine start or motion | Secured motorcycle, approved start controls, fuel/ignition disable during passive cranking | Starter and engine stopped |
| Uncontrolled fixed-timing operation | Separate reviewed stationary-operation method, emergency shutdown, limited approved operating points | Fuel, ignition, and pump commands off |
| Rotating, hot, fuel, or electrical exposure | Barriers, routing, ventilation, inspection, and immediate stop access | Engine stopped and energy sources isolated |

No exact timeout, filter, voltage threshold, temperature limit, or fault
recovery is established by this plan.

## Phase A - Bench waveform replay or signal simulation

**Execution status: Not started**

Review: Technical Review Required

Where the selected hardware and tools support it, replay a recorded original
pickup waveform before connecting the ECU to the motorcycle. If replay is not
technically possible, document why and use a separately reviewed signal-
generator method that represents the characterized geometry and signal
limitations without inventing missing waveform data.

### Initial state

- Fuel-pump output disabled.
- Injector outputs disabled.
- Ignition outputs disabled.
- No motorcycle fuel, ignition, or starter energy connected.
- Safe bench power, current limitation where applicable, and emergency
  power-off verified.
- Input amplitude and offset within verified limits.

### Procedure

1. Record the exact configuration, firmware, decoder, input circuit, and replay
   file or generated-signal definition.
2. Verify outputs remain disabled before applying any trigger signal.
3. Apply a stopped state, then a low-speed start transition.
4. Replay representative recorded cranking segments where evidence exists.
5. Repeat the replay and retain separate logs.
6. Where safe and supported, vary amplitude within the characterized recorded
   range without creating an unverified extrapolation.
7. Where safe and supported, introduce separately identified noise, missing
   events, and false events.
8. Test stop/start transitions and recovery after signal loss.
9. Remove the signal and verify the reported stopped state and output-disabled
   state.

### Required records

- Reported RPM.
- Synchronization state.
- Time or event count to synchronization.
- Trigger errors.
- Missing and extra events.
- Error recovery and resynchronization.
- Behavior at low recorded amplitude.
- Behavior with identified noise injection.
- Behavior during stop/start transitions.
- Raw applied waveform, ECU trigger log, configuration, timestamps, and
  evidence references.

## Phase B - Passive motorcycle cranking

**Execution status: Not started**

Review: Technical Review Required

This phase is permitted only after applicable bench replay evidence is stable
and reviewed. During the first installed decoder test, the candidate ECU shall
not control injectors, ignition coils, or the fuel pump.

### Preconditions

1. Motorcycle identity, engine identity, battery state, test wiring, probes,
   grounds, and emergency stop are recorded.
2. The motorcycle is mechanically secured.
3. Fuel-pump, injector, and ignition outputs are physically or electrically
   verified disabled.
4. The original TCI is not connected in parallel unless the specific parallel
   interface has completed analysis and technical review.
5. Raw oscilloscope capture and ECU logging can be recorded simultaneously.
6. Cold, warm, and low-voltage conditions are defined only within safe and
   permitted motorcycle and equipment limits.
7. Unintended engine start is prevented using an approved method.

### Procedure and required observations

1. Record a cold-condition passive cranking capture where safe.
2. Record raw pickup waveform, battery voltage, approximate cranking speed,
   ECU trigger log, reported RPM, synchronization state, synchronization time,
   and trigger errors simultaneously.
3. Repeat the test to assess synchronization repeatability.
4. Record a warm-condition passive cranking capture only where separately safe
   and justified.
5. Record a low but permitted cranking-voltage capture only after the permitted
   range and method are established.
6. Verify no false high-RPM spikes appear in the retained logs.
7. Verify output-disable states before and after every capture.
8. Stop and investigate any false synchronization, unstable RPM, unexplained
   error, output activity, wiring heat, ground disturbance, or unsafe condition.

## Phase C - Fixed-timing validation

**Execution status: Blocked**

Review: Technical Review Required

This phase remains blocked until passive decoding is stable, its evidence has
been reviewed, and a separate stationary live-ignition method and safe engine-
operation configuration have been approved. This plan does not itself enable
fuel, ignition, injector, or pump outputs.

### Planned method

1. Record the exact ECU, firmware, decoder, configuration, ignition output
   interface, coil arrangement, timing-light equipment, and approved operating
   configuration.
2. Use one fixed commanded ignition angle.
3. Disable all advance compensation that could alter the fixed command.
4. Use an inductive timing light; do not add ignition-primary or ignition-
   secondary oscilloscope probing.
5. Compare commanded and measured timing at cranking, idle, and selected
   stationary engine speeds only within the separately approved operating
   scope.
6. Repeat each point and retain commanded angle, measured angle, engine speed,
   battery voltage, temperature, logs, and evidence.
7. Adjust only a documented global trigger offset.
8. Do not hide drift or an incorrect offset in an ignition table.

A maximum deviation of plus or minus 1 crank degree may be evaluated as a
proposed project validation target. It is not a Yamaha, ECU-manufacturer, or
rusEFI specification and is not accepted until reviewed.

Any timing drift with speed requires investigation of VR polarity, selected
edge, input conditioning, air-gap variation, runout, noise, and trigger
geometry before progression.

## Phase D - Fault injection

**Execution status: Not started**

Review: Technical Review Required

Fault injection begins on the bench with outputs disabled. Any installed or
running-engine fault test requires a separately reviewed method, controlled
operating state, emergency shutdown, and explicit authorization for the exact
fault.

| Fault ID | Planned fault | Initial test domain | Proposed expected safe behavior |
| --- | --- | --- | --- |
| DEC-FLT-001 | Crank sensor disconnected before start | Bench, then passive cranking | No synchronization; no fuel, ignition, or pump command. |
| DEC-FLT-002 | Crank signal interrupted during controlled operation | Bench first | Injection and ignition commands stop; fuel pump switches off after a defined and validated timeout. |
| DEC-FLT-003 | Intermittent connection | Bench first | Invalid sequence is rejected; outputs remain or enter the reviewed safe state. |
| DEC-FLT-004 | Missing event | Bench first | Error is detected and no invalid fuel or ignition command is produced. |
| DEC-FLT-005 | False event | Bench first | Implausible sequence or frequency is rejected without a false high-RPM output. |
| DEC-FLT-006 | Noise burst | Bench first | No unsafe synchronization or output; detection and recovery are logged. |
| DEC-FLT-007 | Low supply voltage | Bench first, passive cranking later | Defined reset or continued operation without unintended output. |
| DEC-FLT-008 | Sensor heating | Bench or controlled environmental setup | No unsafe output; temperature, signal change, diagnostics, and recovery are recorded. |
| DEC-FLT-009 | Start/stop transition | Bench replay, then passive cranking | Repeatable synchronization and stop detection without stale output. |
| DEC-FLT-010 | Loss and recovery of synchronization | Bench first | Outputs remain safe; resynchronization behavior is logged and requires review. |

All expected safe behaviors in this table are proposals until the exact
configuration, method, timing, diagnostics, and recovery have been technically
reviewed and experimentally validated. No cam-loss fallback is assumed.

## Measurement and evidence identifiers

| Measurement ID | Planned evidence | Phase | Initial execution status | Result |
| --- | --- | --- | --- | --- |
| DEC-CFG-001 | Complete ECU, firmware, decoder, input, output-disable, and grounding configuration | Preconditions | Not started | Not run |
| DEC-BENCH-001 | Baseline recorded-waveform replay | Phase A | Not started | Not run |
| DEC-BENCH-002 | Low-amplitude replay within recorded evidence | Phase A | Not started | Not run |
| DEC-BENCH-003 | Noise and event-error replay | Phase A | Not started | Not run |
| DEC-CRK-001 | Cold passive cranking synchronization | Phase B | Not started | Not run |
| DEC-CRK-002 | Warm passive cranking synchronization where safe | Phase B | Not started | Not run |
| DEC-CRK-003 | Low but permitted cranking-voltage synchronization | Phase B | Not started | Not run |
| DEC-TIM-001 | Fixed timing at cranking | Phase C | Blocked | Not run |
| DEC-TIM-002 | Fixed timing at idle | Phase C | Blocked | Not run |
| DEC-TIM-003 | Fixed timing at selected stationary speeds | Phase C | Blocked | Not run |
| DEC-FAULT-001 | Complete fault-injection record for DEC-FLT-001 through DEC-FLT-010 | Phase D | Not started | Not run |

Retain original scope waveforms, applied replay files, generator definitions,
ECU logs, configuration files, firmware identifiers, screenshots, CSV exports
where supported, timing-light observations, photographs, connection diagrams,
operator notes, equipment records, deviations, failures, and repeated results.
Use measurement IDs in filenames. Do not store copyrighted manual pages.

## Stop conditions and recovery

Stop immediately for any uncommanded fuel-pump, injector, or ignition output;
false high-RPM spike; unexpected synchronization; unexplained timing shift;
grounding uncertainty; input overrange; unstable or hot wiring or equipment;
fuel leak; smoke; unexpected engine start or motion; loss of emergency shutdown;
unsafe rotating or thermal exposure; corrupted configuration identity; lost
logging; or invalid precondition.

After stopping, establish fuel-pump, injector, ignition, starter, and engine
safe states; isolate power and signal sources; retain the configuration and raw
evidence; document the event; inspect the motorcycle and equipment; and resume
only after the cause and revised method have been technically reviewed.

## Decision gates

No gate is passed. A successful engine start cannot by itself accept a trigger,
sensor, decoder, ECU, input circuit, or synchronization strategy.

| Gate | Required evidence | Initial state |
| --- | --- | --- |
| Gate 1 - Bench decoder stability | Repeatable replay, correct RPM interpretation, synchronization evidence, error logs, stop/start behavior, and safe output-disable state. | Not evaluated |
| Gate 2 - Passive cranking synchronization | Simultaneous raw waveform and ECU log, no false high-RPM spikes, repeated synchronization across reviewed conditions, and no control output. | Not evaluated |
| Gate 3 - Fixed-timing accuracy and stability | Reviewed fixed-angle method, commanded-versus-measured evidence, repeatability, global offset record, and no unexplained speed-related drift. | Blocked pending Gates 1 and 2 |
| Gate 4 - Fault handling and safe shutdown | Reviewed disconnection, interruption, intermittent, missing/false event, noise, voltage, heat, transition, loss, recovery, and shutdown evidence. | Not evaluated |
| Gate 5 - Technical review | Review of requirements, configuration, hazards, methods, evidence, deviations, safe states, limitations, and next-stage authorization. | Not completed |

## Result and acceptance boundary

**Test result: Not available**

The result remains unavailable until execution records and gate evidence are
reviewed. Passing this plan would establish only the tested configuration and
scope. It would not establish road suitability, tuning, full-power operation,
mechanical compatibility, final electrical compatibility, final safety
suitability, or component acceptance.

## Quality checks

1. [ ] Document status remains Draft.
2. [ ] Execution status remains Not started.
3. [ ] Test result remains Not available.
4. [ ] Review remains Technical Review Required.
5. [ ] Exact ECU board, hardware revision, firmware, pins, and input circuit are required before execution.
6. [ ] Initial replay and passive cranking keep fuel-pump, injector, and ignition outputs disabled.
7. [ ] Parallel original-TCI connection remains blocked pending loading and grounding review.
8. [ ] Fixed-timing work remains blocked pending stable passive decoding and separate review.
9. [ ] The plus-or-minus-1-degree value is only a proposed project target.
10. [ ] No road, tuning, full-power, ignition-primary, or ignition-secondary work is included.
11. [ ] No fallback behavior, timeout, filter, threshold, board, sensor, pattern, or decoder is accepted.
12. [ ] Relative links resolve and UTF-8 is valid.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-06 | Created future trigger-decoder and fixed-timing validation plan. | Define staged evidence and safety gates after original pickup characterization. |

## Navigation

[TEST-PLAN-0001](TEST-PLAN-0001-original-pickup-characterization.md) | [RESEARCH-0002](../research/RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [RESEARCH-0003](../research/RESEARCH-0003-trigger-and-synchronization-strategy.md) | [Test strategy](test-strategy.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [Documentation index](../INDEX.md)
