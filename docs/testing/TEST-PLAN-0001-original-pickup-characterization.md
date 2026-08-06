# TEST-PLAN-0001: Original pickup characterization

## Purpose

Define a safe, repeatable, and traceable procedure for identifying, inspecting,
measuring, and characterizing the original XJ900S pickup coil and timing-plate
arrangement before deciding whether it is suitable for Level 1 engine
management.

**Document status: Draft**

**Execution status: Not started**

**Test result: Not available**

Review: Technical Review Required

The plan shall not be executed until equipment inventory, probe ratings, scope grounding, connection diagram, and engine-start prevention are technically reviewed. No result classification is assigned before execution.

## Scope

Included: vehicle/engine and pickup identification, wiring/coil routing, static resistance and continuity, plate geometry/timing marks/air gap/space, cranking waveform and optional separately approved idle waveform, signal characteristics, repeatability, timing correlation, configuration, photos, raw evidence, and follow-up analysis.

Excluded: ignition primary/secondary/TCI measurement, high voltage, modification, machining, trigger/ECU selection, EFI suitability decision, strategy acceptance, and road testing. Initial work is low-voltage pickup characterization only.

## Known reference values

For manual-stated 1995 4KM1 only: pickup 446-545 ohms at 20 degrees C; White/Red and White/Green leads; 5 degrees BTDC at 1,000 rpm; 40 degrees BTDC at 5,000 rpm; timing check 950-1,050 rpm; timing-plate bolt 45 Nm. These are comparison references, not 1997 limits. Do not remove or tighten the timing-plate bolt for inspection.

## Test-object and session metadata

No field below has been populated. Record the values during an authorized test
session without inferring a missing identifier or condition.

| Field | Recorded value | Initial state |
| --- | --- | --- |
| Test ID | TEST-PLAN-0001 | Defined |
| Date and time | Not recorded | Not started |
| Operator | Not recorded | Not started |
| Frame/vehicle identifier | 4KM060267 | Project-recorded; verify against the test object |
| Engine number | Not recorded | Not started |
| Ambient temperature | Not recorded | Not started |
| Engine temperature | Not recorded | Not started |
| Battery open-circuit voltage | Not recorded | Not started |
| Battery voltage during cranking | Not recorded | Not started |
| Meter model and serial number | Not recorded | Not started |
| Oscilloscope model and serial number | Not recorded | Not started |
| Probe type and attenuation | Not recorded | Not started |
| Sample rate | Not recorded | Not started |
| Original TCI connected or disconnected | Not recorded | Not started |
| Ignition coils connected or disconnected | Not recorded | Not started |
| Fuel-system state | Not recorded | Not started |
| Spark plugs installed or removed | Not recorded | Not started |

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

No electrical measurement is included in this phase.

1. Record the motorcycle identity, project-recorded frame/vehicle identifier,
   and engine number without inferring production year or submodel from the 4KM
   prefix.
2. Photograph the pickup connector before disconnection or cleaning.
3. Identify and photograph the White/Red and White/Green pickup wires where
   confirmed on the motorcycle.
4. Photograph the complete accessible pickup cable routing.
5. Inspect and record connector lock, seals, terminals, insulation, previous
   repairs, cable exit, and strain relief.
6. Document proximity to ignition wiring, high-tension leads, starter wiring,
   charging wiring, and other high-current paths.
7. Photograph the ignition coils, high-tension lead routing, TCI, timing cover,
   and accessible timing marks.
8. Trace ignition-coil and high-tension-lead routing without assuming cylinder
   pairing or wasted-spark operation.
9. Record visible part identifiers exactly as read. Flag the unresolved
   `4JT051`/`J4T051` ignitor discrepancy rather than normalizing it.
10. Record differences between the project motorcycle and the manual-stated
    1995 4KM1 reference.

### Phase B - Static pickup measurement

1. Switch ignition off, remove the key, and apply the approved accidental
   starter-operation prevention controls.
2. Positively identify and disconnect the pickup so resistance is measured
   directly at the disconnected pickup, isolated from the TCI and energized
   circuitry.
3. Prove absence of voltage using the reviewed method before selecting
   resistance mode. Never use resistance mode on an energized circuit.
4. Record pickup and ambient temperature.
5. Measure lead-to-lead resistance with EQ-001 and record the stable value,
   minimum, maximum, instability, open-circuit indications, and interruptions.
6. Reverse the meter leads and repeat the measurement.
7. Perform a controlled cable-manipulation test while observing resistance;
   avoid pulling, sharp bending, or damage.
8. Repeat the measurement from the TCI-side harness with the TCI disconnected
   and record the result separately.
9. Do not invent a permitted harness-resistance delta. Retain the raw values
   for later review.
10. Make pickup-lead-to-ground observations only after topology and grounding
    review defines a safe and meaningful method.
11. EQ-004 may provide a separately identified repeatability measurement.
12. Compare only with the manual-stated 1995 4KM1 reference range and preserve
    the 1997 applicability limitation. An in-range resistance does not prove
    dynamic, decoder, or EFI suitability.

Do not use a megohmmeter or high-voltage insulation tester on the pickup,
harness, TCI, or connected motorcycle circuitry.

### Phase C - Mechanical inspection

1. Photograph the timing-plate area before cleaning or disturbing contamination.
2. Remove only the service cover required by the reviewed method. Do not loosen
   the timing-plate bolt merely for inspection.
3. Photograph the pickup body, magnetic face, potting, cable exit, mount,
   timing plate, centre retention, pins, fasteners, marks, pointer, routing,
   seals, contact marks, contamination, and previous modification.
4. Identify and record the visible trigger-feature count.
5. Measure visible feature width, feature height, gaps, and rotor diameter where
   accessible with an appropriate non-damaging method.
6. Measure pickup air gap at all relevant trigger features and record minimum,
   maximum, and variation.
7. Measure radial and axial runout only where a valid reference surface and safe
   method are available; record values without inventing Yamaha limits.
8. Record available radial, axial, and cover clearance without treating it as
   component compatibility.
9. Prevent debris entry and restore the inspected area to its approved safe
   configuration.

Do not drill, grind, weld, or otherwise modify the original timing plate. Do
not infer dimensions or angles from photographs.

### Phase D - Cranking waveform planning

**Execution status: Blocked**

Waveform capture remains blocked until probe identity and rating are verified,
the oscilloscope grounding architecture is technically reviewed, a connection
diagram is approved, the motorcycle is secured, fuel and ignition risks are
controlled, unintended engine start is prevented, and an emergency-stop method
is available.

When approved, record separate configurations with spark plugs installed and,
only if separately safe and justified, spark plugs removed. Capture minimum and
maximum peak-to-peak amplitude, event count per revolution, event spacing,
polarity, irregular intervals, ringing, noise, missing events, false events,
battery voltage, approximate cranking speed, and repeatability. Preserve the
raw scope waveform and configuration for every capture.

#### Method D1 &mdash; True differential measurement

**Status: Unverified**

Use a suitable differential probe across the pickup leads only after its
identity, rating, range, and common-mode capability have been verified through
technical review. This remains the preferred method where verified suitable
differential-probe equipment is available.

#### Method D2 &mdash; Two-channel subtraction

**Status: Proposal**

Use two-channel subtraction only with both ordinary oscilloscope ground clips
at one approved reference point, matched probes and attenuation, and a
technically reviewed common-mode range. This method remains blocked pending
technical review of the TO1104 grounding architecture, pickup circuit,
common-mode range, probe matching, and connection diagram.

### Phase E - Idle waveform capture

**Execution status: Blocked**

Requires reviewed cranking work, retained probes, restored operation, ventilation, thermal/rotating protection, and approved shutdown. No ignition-primary or secondary measurement.

No idle capture may proceed until the cranking tests and all live-engine safety
preconditions have been reviewed. This phase excludes ignition-primary and
ignition-secondary probing.

## Planned timing correlation

**Execution status: Blocked**

Review: Technical Review Required

Develop and approve a separate method for correlating pickup trigger events to
true cylinder-1 top dead centre (TDC). Use a degree wheel and a repeatable TDC
measurement method. Do not rely only on painted factory timing marks, the
piston's apparent highest dial-indicator point, or the stated ignition timing.

The method shall record:

- Geometric trigger position.
- Electrical zero crossing.
- Selected signal edge.
- Angle relative to true cylinder-1 TDC.

Do not specify crankshaft rotation direction until it is verified from an
applicable service source. Do not use the planned correlation to imply a
selected ECU-detected edge or trigger offset.

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
| PCK-RES-005 | Controlled pickup-cable manipulation observation | Phase B | Not started | Not run |
| PCK-RES-006 | TCI-side harness resistance with TCI disconnected | Phase B | Not started | Not run |
| PCK-GEO-001 | Visible timing-feature count | Phase C | Not started | Not run |
| PCK-GEO-002 | Timing-feature widths and gaps | Phase C | Not started | Not run |
| PCK-GEO-003 | Pickup air gap | Phase C | Not started | Not run |
| PCK-GEO-004 | Available radial and axial clearance | Phase C | Not started | Not run |
| PCK-GEO-005 | Timing-cover clearance | Phase C | Not started | Not run |
| PCK-GEO-006 | Visible feature height and rotor diameter where accessible | Phase C | Not started | Not run |
| PCK-GEO-007 | Radial runout where a valid reference and safe method exist | Phase C | Not started | Not run |
| PCK-GEO-008 | Axial runout where a valid reference and safe method exist | Phase C | Not started | Not run |
| PCK-WAV-001 | Cranking differential waveform using Method D1 | Phase D, Method D1 | Blocked | Not run |
| PCK-WAV-002 | Cranking differential waveform using Method D2 | Phase D, Method D2 | Blocked | Not run |
| PCK-WAV-003 | Connected and normally loaded cranking waveform | Phase D | Blocked | Not run |
| PCK-WAV-004 | Disconnected or unloaded waveform, only if separately justified | Phase D | Blocked | Not run |
| PCK-WAV-005 | Idle waveform capture | Phase E | Blocked | Not run |
| PCK-TDC-001 | Repeatable true cylinder-1 TDC determination | Planned timing correlation | Blocked | Not run |
| PCK-TDC-002 | Geometric and electrical trigger correlation to true cylinder-1 TDC | Planned timing correlation | Blocked | Not run |
| PCK-SAF-001 | Test-equipment and probe verification | Before Phases B through E | Not started | Not run |
| PCK-SAF-002 | Oscilloscope grounding review | Before Phase D | Not started | Not run |
| PCK-SAF-003 | Connection-diagram review | Before Phases B through E | Not started | Not run |
| PCK-SAF-004 | Engine-start prevention review | Before Phases D and E | Not started | Not run |
| PCK-SAF-005 | Motorcycle stability, fuel, ventilation, and emergency-stop check | Before Phases D and E | Not started | Not run |

Execution status and test result are separate dimensions. Every completed result
shall record date, operator, motorcycle, equipment, probe or lead, connection
point, operating state, environmental conditions, raw value, unit, uncertainty,
evidence reference, and reviewed result classification.

## Evidence handling and storage

Proposed, not-created repository paths are `evidence/pickup/photos/`,
`evidence/pickup/measurements/`, `evidence/pickup/waveforms/`, and
`evidence/pickup/diagrams/`. Do not store copyrighted manual pages. Retain
original waveform files, CSV exports where supported, original photographs,
screenshots, connection diagrams, operator notes, and equipment records.
Screenshots and edited images shall not replace raw/original evidence.
Filenames shall reference the measurement identifier; record checksums where
practical.

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

## Decision gates

No gate is passed. Each gate requires retained evidence and technical review
where applicable.

| Gate | Required evidence | Initial state |
| --- | --- | --- |
| Gate 1 - Pickup electrical health | Direct pickup resistance in both meter directions, temperature, cable-manipulation stability, interruptions, and separately recorded TCI-side harness measurement. | Not evaluated |
| Gate 2 - Mechanical timing-plate health | Before-cleaning photographs, feature geometry, pickup and mount condition, air-gap range and variation, retention, contact/contamination observations, and available runout evidence. | Not evaluated |
| Gate 3 - Cranking waveform quality | Approved differential capture, cranking voltage and speed, amplitude range, event count/spacing, polarity, noise, ringing, missing/false events, and configuration. | Blocked pending waveform preconditions |
| Gate 4 - Repeatability and timing correlation | Repeated captures plus reviewed correlation of geometric position, zero crossing, selected edge, and angle to true cylinder-1 TDC. | Blocked pending prior gates and separate review |

The output of this plan is evidence for later decoder testing. Passing any gate
does not by itself accept the pickup, timing plate, sensor technology, trigger
pattern, decoder, ECU, or synchronization strategy.

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
25. [ ] Test result remains Not available until execution evidence is reviewed.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-06 | Expanded test-object metadata, phased methods, timing correlation, evidence handling, and decision gates. | Prepare complete, blocked characterization evidence before decoder or component selection. |

## Recommended next action

1. Record Micsig probe models and ratings; review TO1104 manual, battery, and grounding.
2. Determine differential-probe availability; create reviewed connection and start-prevention diagrams.
3. Perform Phase A only after review; begin no electrical work until all applicable preconditions are satisfied.

## Navigation

[Test strategy](test-strategy.md) | [TEST-PLAN-0002](TEST-PLAN-0002-trigger-decoder-and-timing-validation.md) | [RESEARCH-0002](../research/RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [RESEARCH-0003](../research/RESEARCH-0003-trigger-and-synchronization-strategy.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [Testing index](README.md)
