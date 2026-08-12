# RESEARCH-0005: 1997-on electrical baseline extraction

**Purpose:** Provide a traceable worksheet for extracting and recording the
electrical baseline of the project-recorded 1997 Yamaha XJ900S before any
decision is made about reusing original pickup or ignition hardware for EFI.

**Document status: Draft**

**Status: Unverified**

**Review: Technical Review Required**

## Research question

What schematic-derived information, direct observations, and direct
measurements are required to establish the project motorcycle's electrical,
ignition, pickup, throttle-position, fuel-pump, starter, and engine-stop or
interlock baseline without assuming compatibility with a future Level 1 ECU?

## Scope

### Included

- Pickup coil, original ignition control unit, ignition coils, and TPS.
- Fuel-pump relay, fuel pump, starter request, kill switch, neutral switch,
  clutch switch, sidestand switch, and relevant engine-stop or interlock paths.
- Source references, connector and pin identification, observed wiring,
  circuit-path extraction, direct measurements, evidence references, and open
  questions for the project-recorded 1997 motorcycle.
- Evidence needed before original pickup or ignition hardware can be evaluated
  for EFI reuse.

### Excluded

- Selection or acceptance of an ECU, trigger decoder, sensor, trigger wheel,
  ignition strategy, DBW strategy, fuel-pump circuit, or Level 2 controller.
- Reconstructed wiring, connector pinouts, wire colours, specifications,
  limits, timing angles, trigger geometry, or signal values not supported by a
  retained source or direct evidence.
- Execution of live electrical, cranking, waveform, ignition-primary, or
  ignition-secondary testing.
- Changes to accepted ADR decisions or transfer of Level 1 authority.

## Vehicle and applicability boundary

- Project motorcycle: 1997 Yamaha XJ900S Diversion.
- Project-recorded model designation: 4KM.
- Internal test-object identifier: `XJ900S-01`.
- Exact year-applicable electrical variant and production submodel: Unverified.

Use `XJ900S-01` wherever this record must reference the exact project
motorcycle as a test object. The internal identifier does not establish model,
production, specification, or source applicability beyond the separately
recorded information above.

The complete Yamaha service manual currently referenced by the project is
authoritative for the manual-stated 1995 4KM1 variant only. It is not direct
evidence for the complete 1997 motorcycle. Adjacent-year information may
identify questions but shall not be transferred to the project motorcycle
without explicit applicability evidence or direct inspection.

## Source register

| Source ID | Source | Type | Availability in repository | Applicability and limitation | Information status | Execution status | Result |
| --- | --- | --- | --- | --- | --- | --- | --- |
| ELEC-SRC-001 | Yamaha XJ900S(G) Service Manual, 4KM-28197-20 | Yamaha service manual | Referenced by existing research; copyrighted pages are not stored in the repository | Manual-stated 1995 4KM1 only; 1997 applicability remains Unverified | Confirmed for source identity and stated scope only | Not applicable | Not applicable |
| ELEC-SRC-002 | Photographed 1997-on Haynes schematic | Secondary manual schematic | No usable copy or evidence reference is currently recorded in the repository | Do not reconstruct the schematic; add the exact edition, page, photograph reference, and applicability when available | Unverified | Not applicable | Not applicable |
| ELEC-SRC-003 | Project motorcycle inspection | Direct observation | Not performed for this record | Applies only to the identified motorcycle, date, configuration, and observed access points | Unverified | Not started | Not run |
| ELEC-SRC-004 | Project motorcycle electrical measurements | Direct measurement | Not performed for this record | Requires an approved method, identified instruments, recorded conditions, and retained evidence | Unverified | Not started | Not run |

Marketplace listings, forum posts, connector resemblance, and repeated
unsourced claims may identify research questions. They shall not establish a
Yamaha specification, wiring identity, compatibility, or acceptance.

## Evidence and information classification

Evidence class and information status are separate. Each populated entry shall
identify both.

| Evidence or information class | Required record | Permitted conclusion boundary |
| --- | --- | --- |
| Schematic-derived information | Exact source ID, edition or revision, page or figure, model/year applicability, and extracted item | Describes what the cited source shows; it is not direct observation of the project motorcycle |
| Direct observation | Motorcycle identifier, date, observer, access point, photograph or evidence reference, and literal observation | Confirms only what was directly visible on the identified motorcycle in the recorded condition |
| Direct measurement | Motorcycle identifier, date, instrument, connection points, method, conditions, raw value, unit, and evidence reference | Confirms only the recorded measurement within its method, uncertainty, and conditions |
| Engineering assumption | Assumption, reason, dependency, consequence if wrong, and required verification | Remains `Status: Unverified`; it shall not be used as a confirmed fact |
| Proposal | Proposed function or approach, rationale, risks, dependencies, and required evidence | Does not authorize implementation or establish compatibility |
| Accepted decision | ADR or accepted requirement reference and exact decision scope | Applies only within the accepted scope and shall not be expanded by this record |
| Completed validation | Test ID, tested configuration, criteria, retained results, result classification, and review | Applies only to the tested configuration and validated scope |

An observation or measurement does not automatically establish component
identity, source applicability, health, compatibility, or validation. Those
conclusions require their own evidence and review.

## Accepted architecture boundary

**Status: Accepted**

Under [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md),
Level 1 retains authority over fuel, ignition, engine synchronization,
fuel-pump safety, engine state, and engine shutdown. Level 2 may handle
documented non-engine rider inputs or supervisory information, but it shall not
receive direct fuel or ignition authority or become a hidden dependency for
basic engine operation. This baseline extraction does not change that boundary.

## Baseline extraction rules

1. Record the source before transcribing a schematic item.
2. Keep schematic wire colours separate from colours observed on the actual
   motorcycle.
3. Record connector location, connector identification, pin count, terminal
   identification, splices, junctions, grounds, fuses, diodes, and relays only
   where the source or direct evidence shows them.
4. Preserve conflicts between sources and the motorcycle; do not normalize a
   discrepancy without evidence.
5. Record switch states and signal polarity only after the relevant reference
   and test method are defined.
6. Use `Not recorded`, `Not run`, or `Unverified` instead of estimating a value.
7. Do not energize, disconnect, bridge, back-feed, or bypass a safety-related
   circuit under this research record. Electrical execution requires an
   applicable technically reviewed test method.

## Circuit identification and path register

No circuit facts have been populated. Complete the fields from cited sources
and direct inspection without merging those evidence classes.

| Circuit ID | Function | Schematic source and path | Schematic connector, pins, and wire colours | Observed connector location and ID | Observed pin count and wire colours | Direct evidence reference | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| ELB-01 | Pickup coil to original ignition control unit | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-02 | Original ignition control unit power, ground, inputs, and outputs | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-03 | Ignition coil supply and control paths | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-04 | TPS supply, reference, signal, and return paths | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-05 | Fuel-pump relay coil and switched-contact paths | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-06 | Fuel-pump supply, return, protection, and connector path | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-07 | Starter-request input and starter-control path | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-08 | Kill-switch or engine-stop-switch path | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-09 | Neutral-switch path | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-10 | Clutch-switch path | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-11 | Sidestand-switch path | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-12 | Starter-interlock relay, diode, junction, or equivalent logic path | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| ELB-13 | Engine-stop path affecting ignition and fuel-pump operation | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |

## Component identification register

Record markings exactly as observed. Do not resolve the existing
`4JT051`/`J4T051` ignitor discrepancy without access to the underlying source.

| Item ID | Component | Installed location | Marking or part number observed | Schematic or catalogue identification | Evidence reference | Status |
| --- | --- | --- | --- | --- | --- | --- |
| EID-01 | Pickup coil | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-02 | Original ignition control unit | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-03 | Ignition coil A | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-04 | Ignition coil B | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-05 | TPS | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-06 | Fuel-pump relay | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-07 | Fuel pump | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-08 | Starter relay or starter-cutoff device | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |
| EID-09 | Interlock relay, diode assembly, or equivalent device | Not recorded | Not recorded | Not recorded | Not recorded | Unverified |

## Schematic extraction worksheet

Use one row per source-derived node, connector, pin, wire, splice, protection
device, switch contact, relay contact, or ground relevant to ELB-01 through
ELB-13. Add rows during extraction; do not infer omitted detail.

| Extraction ID | Circuit ID | Source ID and page/figure | Source-stated model/year | From node | Via connector, pin, colour, or device | To node | Information status | Notes or conflict |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SCH-001 | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not recorded |

## Direct-observation worksheet

| Observation ID | Circuit or item ID | Date | Motorcycle configuration | Literal observation | Connector and pin detail | Observed wire colours | Photo or evidence reference | Information status | Execution status | Result |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| OBS-001 | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not started | Not run |

## Direct-measurement worksheet

This register records only measurements performed under a separately reviewed
method. Pickup measurements shall use the stable `PCK-01` through `PCK-09`
record in [TEST-PLAN-0001](../testing/TEST-PLAN-0001-original-pickup-characterization.md).

| Measurement ID | Circuit or item ID | Date | Instrument and identifier | Connection points | Motorcycle and circuit state | Method and conditions | Raw value and unit | Evidence reference | Information status | Execution status | Result |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ELB-M-001 | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded |  | Not recorded | Unverified | Not started | Not run |

No measured value, switch state, or operational result is recorded by this
document revision.

## Engine-stop and interlock state record

The conditions below identify recording needs, not expected Yamaha behavior.
Exact safe test states and permitted manipulations require technical review
before execution.

| Condition ID | Condition to document | Key state | Kill-switch state | Gear and neutral state | Clutch-switch state | Sidestand-switch state | Starter request and response | Fuel-pump state | Ignition or engine-stop response | Evidence | Information status | Execution status | Result |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ESI-01 | Motorcycle as found before manipulation | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not started | Not run |
| ESI-02 | A source-supported starter-permitted condition | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not started | Not run |
| ESI-03 | A source-supported starter-inhibited condition | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not started | Not run |
| ESI-04 | Engine-stop or kill input activation under an approved method | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not started | Not run |
| ESI-05 | Neutral, clutch, and sidestand interaction under an approved method | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not started | Not run |
| ESI-06 | Starter, ignition-control, and fuel-pump path relationship | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Not recorded | Unverified | Not started | Not run |

## Measurement and execution boundary

**Execution status: Not started**

**Result: Not run**

Review: Technical Review Required

Before any electrical execution, identify the applicable schematic, test
object, connector, instrument, probe or lead, connection diagram, power and
ground state, circuit-isolation requirements, expected signal category,
hazards, safe state, stop conditions, and recovery method. Do not use
resistance mode on an energized circuit. Pickup waveform work remains blocked
by the safety and equipment gates in TEST-PLAN-0001.

Ignition-primary and ignition-secondary probing are outside this record. A
live-engine or cranking observation shall not proceed merely because the
motorcycle can be started or the instrument is battery powered.

## Evaluation criteria

### Source and traceability criteria

- Every schematic-derived entry identifies an exact source and applicability
  boundary.
- Direct observations and direct measurements identify the exact motorcycle,
  date, configuration, method, and retained evidence.
- Schematic and observed wire colours are recorded separately.
- Conflicts, missing information, and uncertain identifiers remain explicit.

No numerical source-quality threshold is defined by this record.

### Circuit-baseline evaluation criteria

- Relevant components, connectors, pins, branches, protection devices,
  grounds, and control paths are traceable for each in-scope circuit.
- Starter, kill, neutral, clutch, sidestand, fuel-pump, and ignition or
  engine-stop relationships are documented without bypassing safety logic.
- Any electrical measurement is interpreted only within its method,
  conditions, uncertainty, and source applicability.

No Yamaha electrical limit is created where an authoritative applicable source
or accepted project criterion is absent.

### Pickup and EFI decision-readiness criteria

- Pickup electrical health, waveform, polarity, frequency, geometry,
  mechanical reference, repeatability, and timing correlation are retained as
  separate evidence categories.
- Synchronization robustness and candidate-ECU decoder compatibility are
  evaluated under TEST-PLAN-0002 only after TEST-PLAN-0001 evidence and safety
  gates are satisfied.
- An accepted decision requires traceable evidence, defined criteria,
  technical review, and an ADR where applicable.

No pickup, ignition component, trigger strategy, ECU, or decoder is accepted
by completion of this worksheet.

## Explicit non-validation statements

- Continuity or plausible resistance does not establish suitability as an EFI
  crankshaft-position source.
- Successful engine cranking or starting does not validate trigger quality.
- Waveform quality, trigger geometry, synchronization robustness, and ECU
  decoder compatibility remain separate validation questions.
- Original motorcycle operation does not establish compatibility with a
  replacement ECU, signal-conditioning circuit, ignition strategy, or
  fuel-pump control architecture.

## Open questions

- Which exact 1997-on Haynes edition, schematic page, and photographed evidence
  are available, and what model-year applicability does the source state?
- Which connectors, pins, colours, components, splices, grounds, fuses, relays,
  and diodes are present on the project motorcycle?
- How do the starter, kill, neutral, clutch, and sidestand paths interact with
  the original ignition control unit and fuel-pump circuit?
- Which observations or measurements can be performed without disturbing
  original safety logic, and which require a new reviewed test plan?
- What evidence differences exist between the manual-stated 1995 4KM1 source,
  the 1997-on secondary schematic, and the project motorcycle?

## Decision impact

- Related requirements: SYS-008 through SYS-010, SYS-013, SAF-003, SAF-004,
  SAF-006 through SAF-008, SRV-003, ARC-001, ARC-003 through ARC-008, DEV-001
  through DEV-008, and DOC-001 through DOC-009.
- Related architecture: Level 1 engine management and documented Level 1/Level
  2 interface boundaries.
- Related research: [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md)
  and [RESEARCH-0003](RESEARCH-0003-trigger-and-synchronization-strategy.md).
- Related tests: [TEST-PLAN-0001](../testing/TEST-PLAN-0001-original-pickup-characterization.md)
  and [TEST-PLAN-0002](../testing/TEST-PLAN-0002-trigger-decoder-and-timing-validation.md).
- Roadmap stages: Stage 1 baseline motorcycle validation and Stage 2
  requirements and measurement capture.
- ADR required: Yes before accepting a trigger, synchronization, ignition, DBW,
  or materially changed control-authority decision.

## Recommended next action

1. Record the exact 1997-on Haynes schematic evidence reference if the source
   becomes available; do not copy copyrighted pages into the repository.
2. Complete non-invasive identification and photography before populating any
   direct-observation field.
3. Prepare reviewed connection and safety methods before electrical
   measurement or state testing.
4. Use TEST-PLAN-0001 for pickup characterization and TEST-PLAN-0002 only after
   its predecessor evidence and gates are satisfied.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-12 | Replaced the full vehicle identifier with internal test-object identifier `XJ900S-01`. | Keep exact test-object references non-sensitive without changing the recorded model or year. |
| 2026-08-11 | Created the 1997-on electrical baseline extraction record. | Provide an evidence-classified worksheet for source extraction, direct observation, and later reviewed measurements before EFI reuse decisions. |

## Navigation

[Research index](README.md) | [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [RESEARCH-0003](RESEARCH-0003-trigger-and-synchronization-strategy.md) | [TEST-PLAN-0001](../testing/TEST-PLAN-0001-original-pickup-characterization.md) | [TEST-PLAN-0002](../testing/TEST-PLAN-0002-trigger-decoder-and-timing-validation.md) | [System architecture](../architecture/system-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [Documentation index](../INDEX.md)
