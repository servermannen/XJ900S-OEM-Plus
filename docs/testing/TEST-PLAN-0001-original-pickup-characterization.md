# TEST-PLAN-0001: Original pickup characterization

## Purpose

Define a safe, repeatable, and traceable procedure for identifying, inspecting,
measuring, and characterizing the original XJ900S pickup coil and timing-plate
arrangement before deciding whether it is suitable for Level 1 engine
management.

**Document status: Draft**

**Execution status: Not started**

Review: Technical Review Required

The plan shall not be executed until equipment inventory, probe ratings, scope grounding, connection diagram, and engine-start prevention are technically reviewed. No result classification is assigned before execution.

## Scope

Included: vehicle/engine and pickup identification, wiring/coil routing, static resistance and continuity, plate geometry/timing marks/air gap/space, cranking waveform and optional separately approved idle waveform, signal characteristics, repeatability, timing correlation, configuration, photos, raw evidence, and follow-up analysis.

Excluded: ignition primary/secondary/TCI measurement, high voltage, modification, machining, trigger/ECU selection, EFI suitability decision, strategy acceptance, and road testing. Initial work is low-voltage pickup characterization only.

## Known reference values

For manual-stated 1995 4KM1 only: pickup 446-545 ohms at 20 degrees C; White/Red and White/Green leads; 5 degrees BTDC at 1,000 rpm; 40 degrees BTDC at 5,000 rpm; timing check 950-1,050 rpm; timing-plate bolt 45 Nm. These are comparison references, not 1997 limits. Do not remove or tighten the timing-plate bolt for inspection.

## Available equipment

| Equipment ID | Equipment | Intended use | Verification required | Status |
| --- | --- | --- | --- | --- |
| EQ-001 | Fluke 87V digital multimeter | Resistance/continuity | Leads, fuse, battery, operation | Available; configuration Unverified |
| EQ-002 | Micsig TO1104 oscilloscope number 1 | Primary waveform | Probes, limits, grounding, calibration, storage | Available; configuration Unverified |
| EQ-003 | Micsig TO1104 oscilloscope number 2 | Backup/repeatability | Same as EQ-002 | Available; configuration Unverified |
| EQ-004 | Uni-T UT131D | Optional repeatability | Leads, battery, operation | Available; configuration Unverified |
| EQ-005 | Cleqee 16-piece test-lead kit | Non-invasive connection | Insulation, fit, retention, suitability | Available; configuration Unverified |

Probe models/attenuation/ratings/condition/compensation, batteries, external grounding paths, channel grounds, differential probe, breakout/fused leads, insulated back-probes, tach/timing light, and remote starter are Unverified. Missing optional equipment may block waveform capture, not static inspection.

## Safety assumptions

Status: Unverified

- Treat scope grounds as common until correct TO1104 documentation and a safe disconnected check prove otherwise; battery operation does not prove isolation.
- Do not ground a probe clip to pickup leads or connect clips to different potentials; do not attach charger, computer, USB, grounded display, or external equipment without grounding review.
- Never use resistance mode energized; positively identify and disconnect the pickup before static measurement.
- Do not probe ignition circuits, leave HT leads ungrounded, or rely on stop switch before its effects are known. Secure motorcycle, control fuel/ventilation, and stop for heat, damage, instability, or insecure leads.

Review: Technical Review Required

## Missing equipment information

| Item ID | Missing or unverified information | Status | Blocking effect |
| --- | --- | --- | --- |
| MEQ-001 | Exact Micsig probe models | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-002 | Probe attenuation settings | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-003 | Probe voltage ratings | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-004 | Probe physical condition | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-005 | Probe-compensation status | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-006 | Oscilloscope battery condition | Unverified | Blocks waveform capture until power state is reviewed; does not automatically block visual or static inspection. |
| MEQ-007 | Effect of charger connection on grounding | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-008 | Effect of USB connection on grounding | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-009 | Effect of computer connection on grounding | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-010 | Effect of other external connections on grounding | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-011 | Whether TO1104 channel grounds are common | Unverified | Blocks waveform capture; does not automatically block visual or static inspection. |
| MEQ-012 | Availability of a suitable differential probe | Unverified | Blocks Method D1; does not automatically block visual or static inspection. |
| MEQ-013 | Availability of an automotive low-voltage breakout or fused test lead | Unverified | Blocks waveform capture unless an approved equivalent connection method is available. |
| MEQ-014 | Availability of suitable insulated back-probes | Unverified | Blocks waveform capture unless an approved equivalent connection method is available. |
| MEQ-015 | Availability of a non-contact tachometer | Unverified | Blocks any tachometer-based correlation activity; does not automatically block visual or static inspection. |
| MEQ-016 | Availability of a timing light | Unverified | Blocks timing-light correlation activity; does not automatically block visual or static inspection. |
| MEQ-017 | Availability of a safe remote-starter method | Unverified | Blocks cranking waveform capture; does not automatically block visual or static inspection. |

Missing optional equipment does not automatically prevent visual or static
inspection, but unresolved grounding, probe, or connection requirements shall
block waveform capture.

## Required preconditions

| Precondition ID | Requirement | Initial state | Evidence required | Blocking relevance |
| --- | --- | --- | --- | --- |
| PRE-001 | Motorcycle identity recorded | Not satisfied | Photograph or record identifying motorcycle information. | Blocks all work until the test object is traceable. |
| PRE-002 | Engine number recorded | Not satisfied | Photograph or record the engine number. | Blocks all work until the test object is traceable. |
| PRE-003 | Battery condition acceptable | Not satisfied | Recorded battery condition and assessment. | Blocks electrical work where battery condition affects safety or data quality. |
| PRE-004 | Applicable wiring diagram reviewed | Not satisfied | Reviewed diagram reference and reviewer record. | Blocks electrical work and connection planning. |
| PRE-005 | Pickup connector positively identified | Not satisfied | Photograph and connector identification record. | Blocks pickup measurement and waveform capture. |
| PRE-006 | Pickup wires positively identified | Not satisfied | Photograph and wire-identification record. | Blocks pickup measurement and waveform capture. |
| PRE-007 | Ignition-coil routing recorded | Not satisfied | Photograph and routing record. | Blocks phase-related interpretation and protects against incorrect connections. |
| PRE-008 | Correct oscilloscope manual obtained | Not satisfied | Manual title, model applicability, and revision recorded. | Blocks waveform capture. |
| PRE-009 | Oscilloscope grounding architecture reviewed | Not satisfied | Technical review record of channel-grounding architecture. | Blocks waveform capture. |
| PRE-010 | Oscilloscope probes identified | Not satisfied | Probe manufacturer, model, and identifier recorded. | Blocks waveform capture. |
| PRE-011 | Oscilloscope probes inspected | Not satisfied | Inspection record for insulation, compensation, and condition. | Blocks waveform capture. |
| PRE-012 | Probe attenuation matched between probe and oscilloscope | Not satisfied | Recorded matching probe and oscilloscope attenuation settings. | Blocks waveform capture. |
| PRE-013 | Multimeter leads inspected | Not satisfied | Lead insulation and continuity inspection record. | Blocks static electrical measurement. |
| PRE-014 | Measurement connection diagram approved | Not satisfied | Technically reviewed connection diagram. | Blocks electrical measurement and waveform capture. |
| PRE-015 | Engine-start prevention method approved | Not satisfied | Technically reviewed prevention method and connection diagram. | Blocks cranking and idle work. |
| PRE-016 | Motorcycle mechanically secured | Not satisfied | Stability and restraint check recorded. | Blocks cranking and idle work. |
| PRE-017 | Fuel risks controlled | Not satisfied | Fuel-leak and fuel-control check recorded. | Blocks cranking and idle work. |
| PRE-018 | Ventilation risks controlled | Not satisfied | Ventilation check recorded. | Blocks cranking and idle work. |
| PRE-019 | Emergency stop method available | Not satisfied | Emergency-stop method recorded and checked. | Blocks cranking and idle work. |
| PRE-020 | File naming prepared | Not satisfied | Naming convention recorded. | Blocks execution that would create evidence. |
| PRE-021 | Evidence storage prepared | Not satisfied | Proposed storage location and access check recorded. | Blocks execution that would create evidence. |

## Test phases

### Phase A - Non-invasive visual identification

Record VIN/model/engine; photograph coils, HT routes, TCI, pickup connector/routing; record part numbers, connector pins, White/Red/White/Green where applicable, and 4KM1 discrepancies. No electrical measurement.

### Phase B - Static pickup measurement

Ignition off, key removed, and accidental starter operation prevented: identify/disconnect pickup, prove absence of voltage, measure lead-to-lead resistance with EQ-001, record temperature/stable value, reverse leads, and record open/unstable/intermittent behavior. Chassis observation only after topology review. EQ-004 is optional. Manual-range resistance is not proof of dynamic suitability.

### Phase C - Mechanical inspection

Photograph cover; remove only required service cover; do not loosen plate bolt. Photograph pickup, plate, features, pin, fasteners, marks, pointer, routing, and seals; count/measure features, clearances, and non-damaging air gap; record damage/contamination/runout/adjustment/modification. Prevent debris and restore sealing. Do not infer angles from photos.

### Phase D - Cranking waveform planning

**Execution status: Blocked**

Blocked pending approved connection diagram and start prevention. Required outputs if approved: loaded/unloaded and differential signal, approved-reference signal, cranking correlation, amplitude/count/spacing/polarity/noise/irregular events/repeatability.

#### Method D1 &mdash; True differential measurement

**Status:** Unverified

Use a suitable differential probe across the pickup leads only after its
identity, rating, range, and common-mode capability have been verified through
technical review. This remains the preferred method where verified suitable
differential-probe equipment is available.

#### Method D2 &mdash; Two-channel subtraction

**Status:** Proposal

Use two-channel subtraction only with both ordinary oscilloscope ground clips
at one approved reference point, matched probes and attenuation, and a
technically reviewed common-mode range. This method remains blocked pending
technical review of the TO1104 grounding architecture, pickup circuit,
common-mode range, probe matching, and connection diagram.

### Phase E - Idle waveform capture

**Execution status: Blocked**

Requires reviewed cranking work, retained probes, restored operation, ventilation, thermal/rotating protection, and approved shutdown. No ignition-primary or secondary measurement.

## Engine-start prevention method

Status: Unverified

No method is selected. It must preserve pickup/TCI state, prevent unintended start, control ignition/fuel risks, avoid open HT leads/fuel accumulation, be reversible, and be in the approved connection diagram.

## Oscilloscope configuration record

| Record field | Recorded value | Status or limitation |
| --- | --- | --- |
| Oscilloscope equipment ID | Not recorded | Required before waveform work. |
| Oscilloscope serial number | Not recorded | Required before waveform work. |
| Firmware version | Not recorded | Required before waveform work. |
| Battery state | Not recorded | Required before waveform work. |
| Charger disconnected | Not recorded | Must be disconnected or technically reviewed. |
| USB disconnected | Not recorded | Must be disconnected or technically reviewed. |
| Computer disconnected | Not recorded | Must be disconnected or technically reviewed. |
| Other external connections | Not recorded | Must be disconnected or technically reviewed. |
| Channel used | Not recorded | Required before waveform work. |
| Probe manufacturer and model | Not recorded | Required before waveform work. |
| Probe serial number or identifier | Not recorded | Required before waveform work. |
| Probe attenuation setting | Not recorded | Required before waveform work. |
| Oscilloscope attenuation setting | Not recorded | Required before waveform work. |
| Input coupling | Not recorded | Required before waveform work. |
| Volts per division | Not recorded | Required before waveform work. |
| Vertical offset | Not recorded | Required before waveform work. |
| Timebase | Not recorded | Required before waveform work. |
| Sample rate | Not recorded | Required before waveform work. |
| Acquisition mode | Not recorded | Required before waveform work. |
| Bandwidth limit | Not recorded | Required before waveform work. |
| Trigger source | Not recorded | Required before waveform work. |
| Trigger coupling | Not recorded | Required before waveform work. |
| Trigger mode | Not recorded | Required before waveform work. |
| Trigger slope | Not recorded | Required before waveform work. |
| Trigger level | Not recorded | Required before waveform work. |
| Channel reference point | Not recorded | Required before waveform work. |
| Mathematical function | Not recorded | Required where applicable. |
| Differential-probe settings where applicable | Not recorded | Required where applicable. |
| File format | Not recorded | Required before waveform work. |
| Raw waveform filename | Not recorded | Required before waveform work. |
| Screenshot filename | Not recorded | Required where applicable. |
| CSV filename where available | Not recorded | Required where supported. |
| Operator notes | Not recorded | Required before waveform work. |

## Measurement identifiers

| Measurement ID | Planned observation or measurement | Applicable phase or method | Initial execution status | Result |
| --- | --- | --- | --- | --- |
| PCK-VIS-001 | Motorcycle and engine identification | Phase A | Not started | Not run |
| PCK-VIS-002 | Ignition-coil and high-tension lead routing | Phase A | Not started | Not run |
| PCK-VIS-003 | TCI, pickup connector, and pickup-wire identification | Phase A | Not started | Not run |
| PCK-VIS-004 | Timing cover, pickup, and timing-plate visual inspection | Phase A | Not started | Not run |
| PCK-RES-001 | Pickup lead-to-lead resistance using EQ-001 | Phase B | Not started | Not run |
| PCK-RES-002 | Pickup resistance with meter leads reversed | Phase B | Not started | Not run |
| PCK-RES-003 | Optional independent repeatability measurement using EQ-004 | Phase B | Not started | Not run |
| PCK-RES-004 | Pickup-lead-to-chassis observation, only after topology review | Phase B | Not started | Not run |
| PCK-GEO-001 | Visible timing-feature count | Phase C | Not started | Not run |
| PCK-GEO-002 | Timing-feature widths and gaps | Phase C | Not started | Not run |
| PCK-GEO-003 | Pickup air gap | Phase C | Not started | Not run |
| PCK-GEO-004 | Available radial and axial clearance | Phase C | Not started | Not run |
| PCK-GEO-005 | Timing-cover clearance | Phase C | Not started | Not run |
| PCK-WAV-001 | Cranking differential waveform using Method D1 | Phase D, Method D1 | Blocked | Not run |
| PCK-WAV-002 | Cranking differential waveform using Method D2 | Phase D, Method D2 | Blocked | Not run |
| PCK-WAV-003 | Connected and normally loaded cranking waveform | Phase D | Blocked | Not run |
| PCK-WAV-004 | Disconnected or unloaded waveform, only if separately justified | Phase D | Blocked | Not run |
| PCK-WAV-005 | Idle waveform capture | Phase E | Blocked | Not run |
| PCK-SAF-001 | Test-equipment and probe verification | Before Phases B through E | Not started | Not run |
| PCK-SAF-002 | Oscilloscope grounding review | Before Phase D | Not started | Not run |
| PCK-SAF-003 | Connection-diagram review | Before Phases B through E | Not started | Not run |
| PCK-SAF-004 | Engine-start prevention review | Before Phases D and E | Not started | Not run |
| PCK-SAF-005 | Motorcycle stability, fuel, ventilation, and emergency-stop check | Before Phases D and E | Not started | Not run |

Execution status and test result are separate dimensions. Every completed result
shall record date, operator, motorcycle, equipment, probe or lead, connection
point, operating state, environmental conditions, raw value, unit, uncertainty,
evidence reference, and reviewed result classification.

## Evidence storage

Proposed, not-created repository paths are `evidence/pickup/photos/`, `evidence/pickup/measurements/`, `evidence/pickup/waveforms/`, and `evidence/pickup/diagrams/`. Do not store copyrighted manual pages. Retain original waveform files, CSV where supported, original photographs, connection diagrams, and notes; screenshots and edited images shall not replace raw/original evidence. Filenames shall reference the measurement identifier; record checksums where practical.

## Stop criteria

Stop immediately if:

1. Connector identity is uncertain.
2. Pickup-wire identity is uncertain.
3. The planned grounding path is uncertain.
4. Oscilloscope isolation or common-ground behavior is uncertain.
5. Probe model or rating is unknown.
6. Probe attenuation cannot be verified.
7. Probes or back-probes cannot be retained securely.
8. Unexpected voltage is present during a planned resistance measurement.
9. The engine may start unexpectedly.
10. The approved engine-start prevention method cannot be applied.
11. Fuel leakage occurs.
12. Fuel-vapour accumulation is possible.
13. Ignition energy is uncontrolled.
14. Spark-plug leads are unintentionally left open circuit.
15. Wiring becomes hot.
16. Test leads or probes become hot.
17. An instrument becomes hot or unstable.
18. The waveform exceeds the selected input range.
19. The measured signal conflicts with the approved connection diagram.
20. Rotating components cannot be protected.
21. Test leads could contact rotating or hot components.
22. The motorcycle becomes mechanically unstable.
23. The operator cannot immediately stop starter or engine operation.
24. Any applicable precondition becomes invalid during testing.

Stopping a test is not automatically a failed result unless later classified as
such during review.

## Acceptance of the measurement session

The session may be marked Completed only when:

1. All applicable preconditions were satisfied.
2. No unresolved stop criterion existed.
3. Every triggered stop criterion was documented.
4. Equipment identification was recorded.
5. Equipment configuration was recorded.
6. The approved connection diagram was followed.
7. Operating state was recorded.
8. Environmental conditions were recorded.
9. Raw evidence was saved.
10. Screenshots and exports reference the raw evidence.
11. Measurements were repeated where applicable.
12. Repeatability was demonstrated or discrepancies documented.
13. No motorcycle component was damaged.
14. No connector or wiring was damaged.
15. No test equipment was damaged.
16. All temporary connections were removed.
17. The motorcycle was restored to its initial safe configuration.
18. A post-test inspection was completed.
19. Technical review was completed.

Completion of the measurement session does not accept any EFI trigger component
or strategy. Execution status and result classification remain separate.

## Decision boundary

This plan may characterize the original pickup and timing-plate arrangement, but
it cannot by itself accept:

- The original pickup for EFI use.
- The original timing plate for EFI use.
- A trigger decoder.
- A trigger pattern.
- A crank-only synchronization strategy.
- A camshaft sensor.
- A camshaft sensing location.
- A replacement crank sensor.
- An ECU.
- An ignition topology.
- A final signal-conditioning circuit.

Findings shall update [RESEARCH-0003](../research/RESEARCH-0003-trigger-and-synchronization-strategy.md).
Evidence may create new requirements. Component evaluations shall be created for
shortlisted hardware, and an ADR shall be created only after sufficient
evidence supports a trigger and synchronization decision.

## Quality checks

1. [ ] The document is a plan and contains no invented observations or results.
2. [ ] Document status is Draft.
3. [ ] Execution status is Not started.
4. [ ] Review is Technical Review Required.
5. [ ] Waveform capture remains blocked.
6. [ ] Phase E remains explicitly Blocked.
7. [ ] All preconditions initially remain Not satisfied.
8. [ ] Battery operation is not treated as proof of channel isolation.
9. [ ] Oscilloscope channel grounds are treated as common until verified.
10. [ ] Ground clips are never instructed to connect to different potentials.
11. [ ] No ordinary oscilloscope ground clip is instructed to connect directly to a pickup lead.
12. [ ] Method D2 remains Proposal and technically review-required.
13. [ ] Differential measurement remains dependent on verified equipment.
14. [ ] No ignition-primary measurement is included.
15. [ ] No ignition-secondary measurement is included.
16. [ ] No engine-start prevention method is selected.
17. [ ] Resistance within the manual reference range is not treated as proof of dynamic suitability.
18. [ ] Manual values are not treated as confirmed for the 1997 motorcycle.
19. [ ] No pickup, trigger strategy, sensor, ECU, or other component is accepted.
20. [ ] No copyrighted manual pages are included.
21. [ ] Every identifier is unique.
22. [ ] Relative links resolve.
23. [ ] No malformed UTF-8 exists.
24. [ ] No trailing whitespace exists.

## Recommended next action

1. Record Micsig probe models and ratings; review TO1104 manual, battery, and grounding.
2. Determine differential-probe availability; create reviewed connection and start-prevention diagrams.
3. Perform Phase A only after review; begin no electrical work until all applicable preconditions are satisfied.

## Navigation

[Test strategy](test-strategy.md) | [RESEARCH-0002](../research/RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [RESEARCH-0003](../research/RESEARCH-0003-trigger-and-synchronization-strategy.md) | [Testing index](README.md)
