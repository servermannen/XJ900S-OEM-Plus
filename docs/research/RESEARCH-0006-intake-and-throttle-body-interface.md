# RESEARCH-0006: XJ900S to MT-10 Intake and Throttle-Body Interface

**Purpose:** Define and evaluate the mechanical and airflow interface requirements between the project XJ900S cylinder-head/intake-joint side and the purchased owner-reported 2022 Yamaha MT-10 throttle-body candidate without establishing physical compatibility, selecting an adapter architecture, or accepting an intake implementation.

**Document status: Draft**

**Status: Unverified**

**Review: Technical Review Required**

The intake interface affects fuel delivery, throttle operation, engine behaviour, sealing, and later safety-critical integration. Technical review is required before safety-relevant design, powered or functional testing, or acceptance is based on this record. Non-invasive identification and dimensional measurement may provide the evidence required for that review when performed using an appropriate documented method.

## Research question

What direct geometry, packaging, sealing, injector-targeting, and service evidence is required to determine whether, and by which later-proposed means, the purchased owner-reported MT-10 throttle-body candidate could interface with the XJ900S intake side?

## Scope

### Included

- XJ900S cylinder-head and intake-joint interfaces relevant to EFI conversion.
- Original XJ intake-joint geometry, the MT-10 engine-side interface, and the complete four-cylinder array.
- Diameters, centre spacing, mating and insertion lengths, angles, offsets, clamp zones, sealing, clearance, material requirements, airflow transition, injector targeting, serviceability, reversibility, and direct measurements.
- Candidate interface architectures as proposals only.

### Excluded

- Final adapter design, CAD dimensions, machining drawings, manufacturing release, or accepted material selection.
- Final injector selection, fuel-pressure design, DBW control strategy, rusEFI electrical compatibility, final component acceptance, or road-use validation.

## Source register

| Source ID | Source | Type | Relevance and evidence boundary |
| --- | --- | --- | --- |
| INT-SRC-001 | [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md) | Repository component record | Current project record for the purchased owner-reported MT-10 candidate and its explicitly Unverified dimensions. It does not establish physical compatibility or transfer donor-system facts to the physical candidate. |
| INT-SRC-002 | *Yamaha 2022 MT-10 / MT-10SP Service Manual*, LIT-11616-35-64, B5Y-28197-10, 2022 MT-10 / MT-10SP, MT10N / MT10NC / MT10SPN / MT10SPNC | Yamaha service manual, recorded through COMP-0005 | The documented donor system uses a throttle-body assembly. `THROTTLE BODIES / Removing the throttle bodies` begins on printed page 7-9; its removal table on 7-10 lists 4 throttle-body joint clamp screws, the throttle-body assembly, and 2 throttle-body joints. This is donor-system construction and removal/service evidence only, not proof that the purchased physical candidate is identical. The printed removal/interface reference is 7-9–7-10. This source supplies no recorded dimensions, centre spacing, insertion depth, angle, joint part numbers, cylinder-head mounting geometry, or XJ compatibility. |
| INT-SRC-003 | Owner-reported XJ intake photographic measurements | Owner-reported photographs showing calipers | Values are readings reported from photographs. They are not Yamaha specifications, direct measurements under this record, measurements verified on XJ900S-01, or evidence of MT-10 compatibility. |

## Evidence boundaries

- **Donor-manual facts** describe the manual's documented MT-10 donor system only; they do not identify, measure, or prove the condition of the purchased candidate.
- **Owner-reported photographic measurements** are Unverified readings from photographs, not direct project-motorcycle measurements. Displayed decimal precision does not establish tolerance or uncertainty.
- **Direct future measurements** become evidence only when they identify the object, datum, tool, method, date, raw value, and supporting evidence.
- **Engineering assumptions** remain assumptions until supported by evidence. **Proposals** are options for later evaluation, and **Accepted** decisions are not made by this record.

A matching nominal diameter does not establish compatibility. It cannot alone establish array spacing, engagement, clamp retention, sealing, angle, injector targeting, clearance, or serviceability.

## Interface decomposition

### 1. XJ cylinder-head interface

Required future evidence is intake-port geometry at a defined datum, mounting fastener geometry, intake-joint attachment geometry, head-side seal geometry, port centre spacing, runner angle, and available clearance.

### 2. XJ original intake-joint interface

Required future evidence is head-side ID, carburetor-side ID and OD, overall length, insertion depth, usable clamping length, metal insert/aluminium-section geometry, elastomer geometry, wall thickness, centre spacing, angular orientation, and condition.

| Parameter | Value | Evidence class | Status | Boundary |
| --- | --- | --- | --- | --- |
| Carburetor-side ID | 39.80 mm | Owner-reported photographic measurement | Unverified | Not a Yamaha specification or a direct measurement of XJ900S-01. |
| Aluminium-section ID | 33.80 mm | Owner-reported photographic measurement | Unverified | Not a Yamaha specification or a direct measurement of XJ900S-01. |
| Carburetor-side OD | 53.19 mm | Owner-reported photographic measurement | Unverified | Not a Yamaha specification or a direct measurement of XJ900S-01. |

### 3. MT-10 throttle-body engine-side interface

Required future evidence is OD per runner, insertion/mating length, usable clamp zone, runner centre spacing 1–2, 2–3, and 3–4, total width, lateral and axial offsets, runner angle, throttle-body joint interface geometry, injector position, fuel-rail envelope, and servo/TPS clearance envelope.

### 4. Four-cylinder array compatibility

Per-runner diameter compatibility and complete four-cylinder compatibility are separate questions. Direct measurements must compare XJ spacing 1–2, 2–3, and 3–4 against the corresponding MT-10 spacings; accumulated outer-runner offset; angular mismatch; and axial mismatch. No comparison or calculation is made until direct measurements exist.

## Compatibility matrix

| Interface parameter | XJ value | MT-10 value | Evidence class | Status | Compatibility conclusion | Required validation |
| --- | --- | --- | --- | --- | --- | --- |
| Head-side port geometry | Not measured | Not measured | None | Unverified | Unverified | Direct datum-controlled measurements on both interfaces. |
| XJ joint carburetor-side ID / MT-10 runner OD | 39.80 mm, owner-reported photograph | Not measured | Owner-reported photograph / none | Unverified | Unverified | Direct measurements, including usable engagement and clamp zone. |
| XJ aluminium-section ID | 33.80 mm, owner-reported photograph | Not measured | Owner-reported photograph / none | Unverified | Unverified | Direct XJ joint measurement and later airflow assessment. |
| XJ joint carburetor-side OD | 53.19 mm, owner-reported photograph | Not measured | Owner-reported photograph / none | Unverified | Unverified | Direct XJ joint and candidate interface measurements. |
| Centre spacing 1–2 | Not measured | Not measured | None | Unverified | Unverified | Direct measurements at defined common datums. |
| Centre spacing 2–3 | Not measured | Not measured | None | Unverified | Unverified | Direct measurements at defined common datums. |
| Centre spacing 3–4 | Not measured | Not measured | None | Unverified | Unverified | Direct measurements at defined common datums. |
| Mating length and clamp zone | Not measured | Not measured | None | Unverified | Unverified | Direct measurement and retention/sealing evaluation. |
| Runner angle and offsets | Not measured | Not measured | None | Unverified | Unverified | Direct geometry and clearance assessment. |
| Injector targeting and envelope | Not measured | Not measured | None | Unverified | Unverified | Direct location measurement and spray-path assessment. |

## Injector targeting

Mechanical attachment alone is insufficient because injectors are part of the MT-10 throttle-body assembly. Future evaluation shall establish injector centreline, spray direction, distance to the intake-port entry and valve region, whether an adapter introduces a wall or ledge into the spray path, whether lateral or angular runner adaptation changes targeting, and wall-wetting risk. This record does not infer injector spray angle or target location.

## Airflow transition considerations

Mechanical compatibility is separate from airflow suitability. Future analysis shall consider throttle-bore area; XJ port and joint area; local steps; taper/transition geometry; abrupt contractions or expansions; runner symmetry; effective runner length; and injector interaction. No area ratio is calculated from owner-reported dimensions, and those values are not an accepted design basis.

## Candidate interface architectures

### Proposal A — retain XJ original intake joints

**Status: Proposal**

Evaluate whether the MT-10 engine-side interface can be coupled to the original XJ joints. Potential benefits are the least invasive cylinder-head interface, potential reversibility, and retained original head attachment. Risks include diameter or spacing mismatch, inadequate clamping length, unsuitable ageing elastomer, angle mismatch, and injector targeting. This proposal does not state that the arrangement will work.

### Proposal B — MT-10 throttle-body joints plus XJ adapter

**Status: Proposal**

Evaluate retaining the donor-side MT-10 joint interface and creating a mechanical adapter toward the XJ cylinder head. A potential benefit is preserving the donor throttle-body mating interface. Risks include additional parts and interfaces, package length, sealing, mounting stiffness, injector targeting, and serviceability. MT-10 joints are not assumed to fit the XJ head.

### Proposal C — purpose-designed hybrid intake

**Status: Proposal**

Evaluate a new XJ-side rigid interface combined with a replaceable elastomer coupling toward the MT-10 throttle body. Geometry could address spacing and angular mismatch, while a replaceable flexible coupling could improve serviceability. Risks include custom engineering, material qualification, fatigue/vibration, sealing, manufacturing repeatability, and heat/fuel-vapour exposure. No material is selected.

## Material and construction requirements

Later options shall be evaluated for fuel-vapour resistance, oil-mist resistance, temperature suitability, vacuum sealing, vibration isolation, fatigue resistance, creep resistance, clamp retention, dimensional stability, replaceability, inspectability, manufacturability, and long-term serviceability. No TPU, silicone, polyurethane, FKM, NBR, aluminium alloy, or other specific material is selected. Final material selection requires evidence and later validation.

## Direct measurement plan

| Object | Measurement | Status | Required recorded evidence |
| --- | --- | --- | --- |
| XJ900S-01 | Cylinder-head intake port ID at defined datum; intake-joint head-side ID; intake-joint carb-side ID; intake-joint carb-side OD | Not measured | Datum, tool, date, object identity, photograph/evidence reference, raw values, units. |
| XJ900S-01 | Intake-joint overall length; insertion/mating depth; usable clamp length; metal insert/aluminium-section geometry; elastomer geometry/profile; elastomer wall thickness; intake-joint angular orientation/indexing where applicable; head mounting bolt/stud spacing; head-side seal geometry | Not measured | Datum, tool, date, object identity, photograph/evidence reference, raw values, units. |
| XJ900S-01 | Centre spacing 1–2, 2–3, and 3–4; runner angle; head datum to carb mating plane; surrounding clearance envelope | Not measured | Datum, tool, date, object identity, photograph/evidence reference, raw values, units. |
| Purchased MT-10 candidate | Engine-side OD #1, #2, #3, and #4; insertion length; usable clamp zone | Not measured | Datum, tool, date, purchased-object identity, photograph/evidence reference, raw values, units. |
| Purchased MT-10 candidate | Centre spacing 1–2, 2–3, and 3–4; total assembly width; runner angle/offset | Not measured | Datum, tool, date, purchased-object identity, photograph/evidence reference, raw values, units. |
| Purchased MT-10 candidate | Injector position relative to runner; fuel-rail, servo, TPS, connector, and fuel-hose clearance envelopes | Not measured | Datum, tool, date, purchased-object identity, photograph/evidence reference, raw values, units. |
| MT-10 donor throttle-body joints, if separately evaluated | Exact identity/part number; throttle-body-side ID; engine/head-side ID; length; mounting geometry; bolt pattern; angle; seal method | Not measured | Object identity, authoritative source or direct evidence, datum, tool, date, raw values, units. |

## Measurement method requirements

Every direct measurement shall identify defined datums, a calibrated or identified measurement tool, measurement date, test-object identity, photograph/evidence reference, raw value, and unit. Repeat measurements where useful. Do not infer dimensions from perspective photographs, and do not invent tolerances.

## Safety and failure considerations

Evaluate intake-air leaks, clamp-retention loss, elastomer cracking, adapter loosening, fuel or injector interference, throttle linkage or servo interference, contact with frame/tank/airbox, heat degradation, vibration fatigue, debris ingestion, and uneven cylinder airflow. A successful static fit does not validate the design.

**Review: Technical Review Required**

## Serviceability and reversibility

Later designs shall be evaluated for throttle-body removal without unnecessary engine disassembly; replaceable joints and seals; accessible clamps and fasteners; visible inspection points; obtainable service parts; reproducible assembly position; no undocumented alignment procedure; and reversibility where practical.

## Decision state

**Recommendation: Continue interface characterization**

There is enough evidence to define the interface and measurement campaign, but not enough verified geometry to determine whether the purchased MT-10 throttle-body assembly can be integrated directly, through original XJ joints, through MT-10 donor joints, or through a custom adapter. No architecture is recommended or accepted.

## Exit criteria for this research stage

Before a preferred interface architecture can be recommended, require direct XJ geometry measurements; direct MT-10 geometry measurements; four-runner spacing comparison; usable clamp/mating geometry; injector-targeting assessment; clearance assessment; sealing strategy; serviceability assessment; documented risks; and evidence-backed material requirements.

Prototype-feasibility evidence may support choosing the next prototype only; it is distinct from final acceptance and does not require full production validation at this stage.

## Traceability

- Component candidate: [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md).
- Applicable requirements: [SYS-007](../requirements/system-requirements.md#sys-007), [SYS-008](../requirements/system-requirements.md#sys-008), [SYS-009](../requirements/system-requirements.md#sys-009), [SAF-004](../requirements/system-requirements.md#saf-004), [REL-002](../requirements/system-requirements.md#rel-002), [REL-004](../requirements/system-requirements.md#rel-004), [SRV-001](../requirements/system-requirements.md#srv-001), [SRV-002](../requirements/system-requirements.md#srv-002), [ARC-001](../requirements/system-requirements.md#arc-001), [DEV-002](../requirements/system-requirements.md#dev-002), [DEV-003](../requirements/system-requirements.md#dev-003), and [DEV-008](../requirements/system-requirements.md#dev-008).
- Architecture boundary: [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md); Level 1 retains engine-critical fuel and any later direct throttle authority. This record does not select a throttle strategy.
- Roadmap: [Stage 2](../implementation/roadmap.md#stage-2--requirements-and-measurement-capture) and [Stage 3](../implementation/roadmap.md#stage-3--engine-management-concept-validation).
- Related I/O research: [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md).
- Future measurement and test records: Not yet created.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-13 | Created initial intake and throttle-body interface research record. | Define the evidence-bounded measurement campaign without accepting an interface solution. |

## Navigation

[Research index](README.md) | [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [Documentation index](../INDEX.md)
