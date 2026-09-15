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
- Candidate interface architectures as proposals only; current CAD/prototype geometry exploration recorded separately from measurements.

### Excluded

- Final adapter design, released CAD dimensions, machining drawings, manufacturing release, or accepted material selection.
- Final injector selection, fuel-pressure design, DBW control strategy, rusEFI electrical compatibility, final component acceptance, or road-use validation.

## Source register

| Source ID | Source | Type | Relevance and evidence boundary |
| --- | --- | --- | --- |
| INT-SRC-001 | [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md) | Repository component record | Current project record for the purchased owner-reported MT-10 candidate with measured candidate geometry and remaining unresolved dimensions. It does not establish physical compatibility or transfer donor-system facts to the physical candidate. |
| INT-SRC-002 | *Yamaha 2022 MT-10 / MT-10SP Service Manual*, LIT-11616-35-64, B5Y-28197-10, 2022 MT-10 / MT-10SP, MT10N / MT10NC / MT10SPN / MT10SPNC | Yamaha service manual, recorded through COMP-0005 | The documented donor system uses a throttle-body assembly. `THROTTLE BODIES / Removing the throttle bodies` begins on printed page 7-9; its removal table on 7-10 lists 4 throttle-body joint clamp screws, the throttle-body assembly, and 2 throttle-body joints. This is donor-system construction and removal/service evidence only, not proof that the purchased physical candidate is identical. The printed removal/interface reference is 7-9–7-10. This source supplies no recorded dimensions, centre spacing, insertion depth, angle, joint part numbers, cylinder-head mounting geometry, or XJ compatibility. |
| INT-SRC-003 | Owner-reported XJ intake photographic measurements | Owner-reported photographs showing calipers | Values are readings reported from photographs. They are not Yamaha specifications, direct measurements under this record, measurements verified on XJ900S-01, or evidence of MT-10 compatibility. |

Owner direct measurement and separate CAD evidence: [RESEARCH-0006 measurement record](evidence/RESEARCH-0006-mt10-throttle-body-direct-measurements.md). This is evidence about the on-hand candidate only, not donor-manual specifications.

## Evidence boundaries

- **Donor-manual facts** describe the manual's documented MT-10 donor system only; they do not identify, measure, or prove the condition of the purchased candidate.
- **Owner-reported photographic measurements** are Unverified readings from photographs, not direct project-motorcycle measurements. Displayed decimal precision does not establish tolerance or uncertainty.
- **Owner-performed direct measurements and observations** now record the on-hand MT-10 candidate geometry in the linked evidence. The measurement/documentation date is recorded as 2026-08-14. Missing measuring-tool identity, detailed method, calibration information, and photograph metadata remain explicit limitations; they are not invented or treated as satisfying the full measurement-method requirements. Future measurement records shall capture those details.
- **CAD/prototype progress** records geometry exploration only, not physical measurement or validation.
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

Owner-performed direct physical measurements of the on-hand candidate are now available:

| Parameter | Direct measured value | Datum / scope |
| --- | --- | --- |
| Port centre spacing 1–2 | 84.0 mm | Measured physical candidate |
| Port centre spacing 2–3 | 84.0 mm | Measured physical candidate |
| Port centre spacing 3–4 | 84.0 mm | Measured physical candidate |
| Engine-side cylindrical interface OD | 52.0 mm | External mating section |
| Engine-side internal bore ID | 42.8 mm | Engine-side interface |
| Straight/cylindrical interface length | 10.5 mm | From engine-side end face |
| OD groove start | 4.5 mm | From engine-side end face; corrected by direct remeasurement |
| OD groove width | 3.0 mm | Physically present groove |
| OD groove depth | 0.95 mm | Physically present groove |

The groove-start position was corrected by direct remeasurement from the earlier 3.0 mm reading to 4.5 mm from the end face; the earlier position is superseded. Groove width remains 3.0 mm. Groove-bottom diameter was not directly measured.

The bore continues inward beyond the external 10.5 mm section. No external bead or step over that section was observed; the groove is present. The bearing-centre reference is approximately 32 mm from the end face, and the four runner interfaces share the same nominal axis orientation as observed. These observations do not quantify runner angles/offsets or establish fit.

See the [evidence record](evidence/RESEARCH-0006-mt10-throttle-body-direct-measurements.md) for limitations and packaging observations requiring datum refinement. Still required are per-runner raw records/method details, usable clamp zone, total width, lateral and axial offsets, quantified runner angle, remaining joint geometry, injector position, fuel-rail envelope, and complete servo/TPS clearance envelope.

### 4. Four-cylinder array compatibility

Per-runner diameter compatibility and complete four-cylinder compatibility are separate questions. Direct measurements must compare XJ spacing 1–2, 2–3, and 3–4 against the corresponding MT-10 spacings; accumulated outer-runner offset; angular mismatch; and axial mismatch. The MT-10 spacings are 84.0 mm each; this does not establish four-cylinder compatibility until equivalent XJ spacing and relevant angles/offsets are directly measured. The final axial relationship remains unresolved.

## Compatibility matrix

| Interface parameter | XJ value | MT-10 value | Evidence class | Status | Compatibility conclusion | Required validation |
| --- | --- | --- | --- | --- | --- | --- |
| Head-side port geometry | Not measured | Not measured | None | Unverified | Unverified | Direct datum-controlled measurements on both interfaces. |
| XJ joint carburetor-side ID / MT-10 runner OD | 39.80 mm, owner-reported photograph | 52.0 mm engine-side OD | Owner-reported photograph / owner direct measurement | Unverified | Unverified | Direct measurements, including usable engagement and clamp zone. |
| XJ aluminium-section ID / MT-10 internal bore | 33.80 mm, owner-reported photograph | 42.8 mm engine-side ID | Owner-reported photograph / owner direct measurement | Unverified | Unverified | Direct XJ joint measurement and later airflow assessment. |
| XJ joint carburetor-side OD | 53.19 mm, owner-reported photograph | 52.0 mm engine-side OD | Owner-reported photograph / owner direct measurement | Unverified | Unverified | Direct XJ joint and candidate interface measurements. |
| Centre spacing 1–2 | Not measured | 84.0 mm | Owner direct measurement, MT-10 only | Unverified | Unverified | Direct measurements at defined common datums. |
| Centre spacing 2–3 | Not measured | 84.0 mm | Owner direct measurement, MT-10 only | Unverified | Unverified | Direct measurements at defined common datums. |
| Centre spacing 3–4 | Not measured | 84.0 mm | Owner direct measurement, MT-10 only | Unverified | Unverified | Direct measurements at defined common datums. |
| Mating length and clamp zone | Not measured | 10.5 mm straight cylindrical section from end face; usable clamp zone unresolved | Owner direct measurement, MT-10 only | Unverified | Unverified | Direct measurement and retention/sealing evaluation. |
| Runner angle and offsets | Not measured | Same nominal axis orientation observed; quantified angles/offsets not measured | Owner direct observation, MT-10 only | Unverified | Unverified | Direct geometry and clearance assessment. |
| Injector targeting and envelope | Not measured | Not measured | None | Unverified | Unverified | Direct location measurement and spray-path assessment. |

## Current CAD/prototype progress

The owner-reported current Fusion model includes:

- A revolved MT-10 port/interface profile and four port bodies.
- Parameter `TB_Port_Pitch = 84.0 mm`, with centre spacing verified as 84.0 mm in the model.
- Packaging/keep-out bodies for P2/P3 and P4.
- An XJ-side construction mid-plane at 126 mm and four XJ-side centres.
- Construction/profile circles using the current working diameters.
- An initial P2 loft test from the MT-10 Ø42.8 mm side toward the XJ P2 Ø33.8 mm side.

This is CAD/prototype design progress, not validation. The loft is a geometry exploration only. The 126 mm value is a current CAD construction/reference value; independent physical evidence establishing it as a physical dimension is not supplied. Successful CAD construction does not establish physical fit, airflow quality, injector targeting, sealing, structural adequacy, manufacturability, or acceptance.

Packaging observations of approximately 8 mm at P2, 7 mm at P3, and 11 mm at P4 are preserved in the linked evidence with datum refinement required. They do not establish a complete clearance envelope or design constraints.

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
| Purchased MT-10 candidate | Engine-side OD/ID, cylindrical length, groove geometry; usable clamp zone | OD 52.0 mm, ID 42.8 mm, length 10.5 mm; groove start 4.5 mm, width 3.0 mm, depth 0.95 mm recorded; groove-bottom diameter and usable clamp zone unresolved | Linked owner direct evidence; per-runner raw records and missing method metadata still required. |
| Purchased MT-10 candidate | Centre spacing 1–2, 2–3, and 3–4; total assembly width; runner angle/offset | Spacings 84.0 mm each recorded; total width and quantified angles/offsets not measured | Linked owner direct evidence; defined datums and missing method metadata still required. |
| Purchased MT-10 candidate | Injector position relative to runner; fuel-rail, servo, TPS, connector, and fuel-hose clearance envelopes | Not measured | Datum, tool, date, purchased-object identity, photograph/evidence reference, raw values, units. |
| MT-10 donor throttle-body joints, if separately evaluated | Exact identity/part number; throttle-body-side ID; engine/head-side ID; length; mounting geometry; bolt pattern; angle; seal method | Not measured | Object identity, authoritative source or direct evidence, datum, tool, date, raw values, units. |

## Measurement method requirements

Every direct measurement shall identify defined datums, a calibrated or identified measurement tool, measurement date, test-object identity, photograph/evidence reference, raw value, and unit. Repeat measurements where useful. Do not infer dimensions from perspective photographs, and do not invent tolerances.

The supplied owner direct measurements are retained with explicit metadata gaps in the evidence file. They do not establish manufacturing tolerances or complete this measurement campaign. Final axial relationship, clamp/retention design, material choice, complete clearance envelope, sealing strategy, and final adapter architecture remain unresolved.

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
- Owner direct measurement and CAD record: [RESEARCH-0006 evidence](evidence/RESEARCH-0006-mt10-throttle-body-direct-measurements.md). Further measurement records and validation test records remain outstanding.

## Change history

Dates below identify documentation updates, not measurement dates.

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-15 | Added owner direct MT-10 measurements, groove-position correction, updated measurement/matrix entries, and separate CAD progress with linked evidence. | Preserve completed characterization without implying compatibility, validation, or architecture acceptance. |
| 2026-08-13 | Created initial intake and throttle-body interface research record. | Define the evidence-bounded measurement campaign without accepting an interface solution. |

## Navigation

[Research index](README.md) | [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [Documentation index](../INDEX.md)
