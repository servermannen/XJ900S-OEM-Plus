# COMP-0005: Owner-Reported 2022 Yamaha MT-10 Throttle-Body Assembly

**Purpose:** Record and evaluate the purchased four-cylinder owner-reported 2022 Yamaha MT-10 throttle-body assembly as a Level 1 EFI candidate without establishing exact Yamaha application, XJ900S compatibility, rusEFI compatibility, DBW acceptance, or road-use suitability.

**Document status: Draft**

## Candidate identification

- Component: Owner-reported complete four-cylinder throttle-body assembly
- Manufacturer: Yamaha — owner-reported identification
- Source model: 2022 MT-10 RN781/B5Y — seller/purchase identification
- Model year or range: 2022 — seller/purchase identification
- OEM part number: Unknown
- Variant identifiers: RN781/B5Y — exact application, market, and variant Unverified
- Source or listing: Owner-reported purchase identification; original seller record not retained
- Evaluation date: 2026-08-13

## Evaluation status

**Status: Unverified**

**Review: Technical Review Required**

Purchase provenance and donor-system information do not establish the physical candidate's identity, condition, compatibility, safety suitability, or acceptance.

## Source register

| Source ID | Source | Scope and evidence boundary |
| --- | --- | --- |
| COMP-0005-SRC-001 | Owner-reported purchase identification | Acquisition provenance only; does not confirm Yamaha application, exact variant, OEM assembly part number, condition, compatibility, or acceptance. |
| COMP-0005-SRC-002 | *Yamaha 2022 MT-10 / MT-10SP Service Manual*, LIT-11616-35-64; Yamaha identifier B5Y-28197-10; first edition January 2022 | Authoritative only for the documented donor system and manual models MT10N, MT10NC, MT10SPN, and MT10SPNC. It does not identify the purchased component or independently confirm RN781 applicability. |
| COMP-0005-SRC-003 | Recent project discussion of a pressure/MAP-sensor candidate physically associated with the on-hand throttle-body assembly | Project discussion/direct-observation context only. It preserves that a pressure-sensor candidate is physically associated with the assembly; it does not establish exact sensor identity, Yamaha part number, official donor application, MAP function, pinout, connector identity, pressure range, transfer function, calibration, or uaEFI compatibility. |

## Intended function

**Status: Proposal**

The complete assembly should continue to be evaluated as the project's primary four-cylinder EFI throttle-body candidate pending dimensional, electrical, functional, integration, and safety validation. This is not an accepted component selection or DBW acceptance.

## Applicable requirements

- [SYS-003](../requirements/system-requirements.md#sys-003), [SYS-006](../requirements/system-requirements.md#sys-006), [SYS-009](../requirements/system-requirements.md#sys-009), and [SYS-011](../requirements/system-requirements.md#sys-011)
- [SAF-003](../requirements/system-requirements.md#saf-003), [SAF-004](../requirements/system-requirements.md#saf-004), [SAF-005](../requirements/system-requirements.md#saf-005), and [SAF-007](../requirements/system-requirements.md#saf-007)
- [REL-002](../requirements/system-requirements.md#rel-002), [REL-004](../requirements/system-requirements.md#rel-004), and [REL-006](../requirements/system-requirements.md#rel-006)
- [SRV-001](../requirements/system-requirements.md#srv-001), [SRV-002](../requirements/system-requirements.md#srv-002), [SRV-003](../requirements/system-requirements.md#srv-003), and [SRV-004](../requirements/system-requirements.md#srv-004)
- [ARC-001](../requirements/system-requirements.md#arc-001), [ARC-003](../requirements/system-requirements.md#arc-003), [ARC-004](../requirements/system-requirements.md#arc-004), [ARC-006](../requirements/system-requirements.md#arc-006), and [ARC-008](../requirements/system-requirements.md#arc-008)
- [DEV-002](../requirements/system-requirements.md#dev-002), [DEV-003](../requirements/system-requirements.md#dev-003), [DEV-008](../requirements/system-requirements.md#dev-008), [DOC-002](../requirements/system-requirements.md#doc-002), [DOC-003](../requirements/system-requirements.md#doc-003), [DOC-006](../requirements/system-requirements.md#doc-006), and [DOC-008](../requirements/system-requirements.md#doc-008)

## Confirmed project-provenance information

**Status: Confirmed**

- The owner reports that the project purchased a complete throttle-body assembly.
- The seller/purchase identification described it as a 2022 Yamaha MT-10 RN781/B5Y throttle-body assembly.

These are acquisition/provenance facts only. They do not independently confirm Yamaha application, exact variant, OEM assembly part number, condition, compatibility, or acceptance. B5Y is consistent with the manual family in COMP-0005-SRC-002; this is not independent confirmation of RN781.

## Confirmed Yamaha donor-system architecture

**Status: Confirmed**

The documented 2022 MT-10 uses a four-cylinder throttle-body assembly, four individual injectors, a throttle servo motor, a TPS, and separate accelerator-position sensing. The TPS system has two monitored signal channels.

| Area | Documented donor-system information |
| --- | --- |
| TPS diagnostics | P0122, P0123, P0222, P0223, and P2135. P2135 is the deviation/plausibility relationship between TPS outputs 1 and 2. Applicable TPS circuit descriptions use 0.25 V or lower and 4.75 V or higher thresholds. |
| Diagnostic displays | Yamaha diagnostic code 01 is TPS signal 1 and code 13 is TPS signal 2. For code 01, fully closed is 11–21 and fully open is 96–107. These are donor diagnostic-display values, not volts, degrees, percentages, or a transfer function. |
| Servo / YCC-T | Diagnostic monitoring includes P0638. Its troubleshooting path lists electrical, mechanical, fuse, servo, wiring/connector, and ECU causes. The Electronic throttle valve fuse is 7.5 A: this is a donor circuit fuse rating, not normal, stall, or motor current. |
| Servo check | The direct servo functional check uses two C-size cells, approximately 3 V total, and specifically prohibits use of a 12 V battery. |
| Documented conductors | Servo-to-ECU conductors include Yellow/Red and Light Green/Red. TPS troubleshooting identifies White, Black/Green, Blue, and Black between TPS and ECU. The source does not assign Vref, sensor ground, TPS1, or TPS2 to those TPS wire colours. |
| Injectors / service | Individual injector diagnostics include P0201 through P0204. Fuel rail and injectors are serviceable in the procedure, with fuel-system precautions. Significant impact/drop damage or cracked/damaged throttle bodies require replacement as a set. Cleaning cautions prohibit inappropriate solvents/caustic cleaners on sensitive parts and disturbing adjustment features without an applicable procedure. |

These facts are confirmed only for the documented Yamaha donor system, not as direct observations of the purchased component.

### Yamaha service-manual evidence locations

The following locations identify where the retained Yamaha service-manual
evidence was extracted. Printed section/page references are recorded where
verified; any remaining location not yet captured stays explicitly unresolved.

| Subject | Yamaha manual topic/location | Printed reference |
| --- | --- | --- |
| Throttle-body service/removal | Throttle-body assembly service/removal procedure; cleaning/replacement information | 7-14–7-15 |
| Electronic throttle valve fuse | Electronic throttle valve fuse specification | 2-12 |
| Throttle-servo check | Checking the throttle servo motor | 8-47 |
| TPS diagnostic displays | Diagnostic code sensor-operation table for TPS signals | 9-77–9-78 |
| TPS fault diagnostics | P0122, P0123, P0222, P0223, and P2135 diagnostic descriptions | Unresolved; printed reference not yet captured |
| YCC-T / servo fault diagnostics | P0638 YCC-T/throttle-servo troubleshooting | 9-221–9-222 |
| Injector fault diagnostics | P0201 through P0204 injector diagnostic descriptions | Unresolved; printed reference not yet captured |

## Known specifications

| Attribute | Value | Source | Status |
| --- | --- | --- | --- |
| Exact Yamaha throttle-body assembly part number | Unknown | No authoritative purchased-component identity | Unverified |
| Purchased-component markings and condition | Not inspected or recorded | No documented inspection | Unverified |
| MT-10 throttle-body-associated pressure-sensor candidate | Physically associated with the on-hand throttle-body assembly in recent project discussion; exact markings not retained in this repository | Project discussion only | Unverified |
| Engine-side geometry and port spacing | Direct measured values recorded below | Owner-performed measurements; linked RESEARCH-0006 evidence | Measured candidate only; compatibility Unverified |
| Pinout, injector data, servo characteristics, TPS transfer functions, and mechanical throttle range | Unknown | No authoritative or measured purchased-component evidence for these attributes | Unverified |

## Physical construction and service information

The documented donor procedure treats fuel rail and injectors as serviceable and requires fuel-system precautions. The purchased assembly's construction, condition, modifications, sealing, and serviceability remain Unverified.

## Throttle-position sensing

The documented donor system separates accelerator-position sensing from TPS sensing and monitors two TPS channels. Purchased-component terminal identity, pinout, transfer function, voltage-versus-angle relation, and channel correlation remain Unverified.

## Throttle-servo / YCC-T information

The donor direct functional check uses approximately 3 V from two C-size cells and explicitly prohibits a 12 V battery. This is not permission to energize the purchased component. No direct 12 V application to the throttle servo is permitted based on this procedure; this record invents no safe current limit.

## Fuel injectors and fuel rail

The donor system has four individual injector diagnostics, P0201 through P0204. Exact injector part number, flow rate, dead time, spray pattern, connector family, fuel-rail interface, and purchased configuration remain Unverified.

## Throttle-body-associated pressure-sensor candidate

**Status: Unverified**

Recent project discussion identified a pressure/MAP-sensor candidate
physically associated with the on-hand owner-reported 2022 MT-10
throttle-body assembly. That physical association is not promoted here into a
confirmed MAP function, exact Yamaha identity, donor application, electrical
interface, or calibration.

This candidate is recorded as the **MT-10 throttle-body-associated
pressure-sensor candidate** until stronger retained evidence exists.

Known and unresolved evidence:

| Attribute | Evidence boundary | Status |
| --- | --- | --- |
| Physical presence / association | Project discussion records a pressure-sensor candidate physically associated with the on-hand throttle-body assembly | Unverified beyond project-discussion context |
| Visible markings | Not retained in this repository | Unverified |
| Exact Yamaha part number | Not established | Unverified |
| Exact donor application | Not established for the sensor itself | Unverified |
| Exact function | Pressure/MAP function is project interpretation only | Unverified |
| Connector identity, cavity numbering, and terminals | Unknown | Unverified |
| Pinout, supply/reference, ground, and signal output | Unknown | Unverified |
| Pressure range, absolute/gauge behavior, transfer function, and calibration | Unknown | Unverified |
| uaEFI compatibility | Not established | Unverified |

The separate loose Yamaha `1WS-82380-00-00` pressure-sensor candidate is a
different physical item and is not part of this throttle-body assembly record.
Evidence about either item shall not be propagated to the other. Similar
appearance, physical fit, or a plausible sensor voltage would not establish
electrical interchangeability, pressure transfer function, calibration, or
uaEFI compatibility.

## Donor diagnostics and fault handling

Donor diagnostic information does not establish a project diagnostic implementation, rusEFI compatibility, fault strategy, safe-state behavior, or DBW acceptance.

## Physical compatibility

Physical compatibility remains Unverified despite the candidate measurements now available. Intake integration is evaluated in [RESEARCH-0006](../research/RESEARCH-0006-intake-and-throttle-body-interface.md); no final adapter or component is accepted.

### Measured physical candidate data

Source: [owner direct measurements and CAD progress](../research/evidence/RESEARCH-0006-mt10-throttle-body-direct-measurements.md). These are owner-performed direct physical measurements of the on-hand candidate, not Yamaha specifications or confirmation of donor application. Measurement metadata and limitations are retained in the evidence file.

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

The earlier groove-start reading of 3.0 mm from the end face is superseded by direct remeasurement to 4.5 mm; 3.0 mm remains the groove width. Groove-bottom diameter was not directly measured and is not inferred here.

The 42.8 mm internal bore continues inward beyond the measured 10.5 mm external mating section. No external bead was observed at the engine-side interface, and no external step was observed over that section. The groove is physically present. The previously measured bearing-centre reference is approximately 32 mm from the engine-side end face. The four measured runner interfaces share the same nominal axis orientation as observed; quantified angles and offsets remain unresolved.

Packaging observations for P2/P3/P4 are retained in the linked evidence under “Packaging observations requiring datum refinement”; they are not design constraints or a complete clearance envelope.

### CAD/prototype progress

The owner-reported current Fusion model includes:

- A revolved MT-10 port/interface profile and four port bodies.
- Parameter `TB_Port_Pitch = 84.0 mm`, with centre spacing verified as 84.0 mm in the model.
- Packaging/keep-out bodies for P2/P3 and P4.
- An XJ-side construction mid-plane at 126 mm and four XJ-side centres.
- Construction/profile circles using the current working diameters.
- An initial P2 loft test from the MT-10 Ø42.8 mm side toward the XJ P2 Ø33.8 mm side.

This is CAD/prototype design progress, not validation. The loft is a geometry exploration only. The 126 mm value is a current CAD construction/reference value; independent physical evidence establishing it as a physical dimension is not supplied. Successful CAD construction does not establish physical fit, airflow quality, injector targeting, sealing, structural adequacy, manufacturability, or acceptance.

## Electrical or functional compatibility

Electrical and functional compatibility with rusEFI, the XJ900S, and a project DBW strategy is Unverified. Connector manufacturer/family, cavity numbering, purchased-component pinout, injector specifications, servo winding resistance/current/stall current/gearing, mechanical throttle-angle range, powered default/rest behavior, and TPS transfer functions are Unknown.

## Integration assessment

### Benefits

**Status: Proposal**

If the purchased assembly is confirmed to correspond to the documented 2022
MT-10 donor configuration, that donor architecture offers a production Yamaha
four-cylinder throttle-body system with four injectors and a fuel rail,
electronic throttle actuation, dual monitored throttle-position signals, and
useful Yamaha diagnostic/service documentation. These donor-system
characteristics do not establish that they are present on the purchased
physical candidate, nor do they establish XJ900S or rusEFI compatibility.

### Risks and constraints

Exact physical identity, remaining mechanical dimensions, XJ900S intake interface, injector characterization, connector/pin identification, electrical compatibility, DBW control strategy, rusEFI compatibility, and safety validation remain unresolved.

### Required adaptations

Final adaptations remain Unknown. Intake-interface proposals and CAD geometry exploration are recorded in RESEARCH-0006; no mechanical, electrical, software, connector, fuel-system, or control adaptation is accepted.

### Missing evidence

All unresolved identity, measurement, electrical, injector, functional, integration, and safety evidence remains required.

## Safety assessment

Throttle control and fuel delivery are safety-critical. Before any powered test, the physical component must be positively identified; connector and terminals must be identified; a controlled test method must be defined; electrical limits and connection method must be reviewed; mechanical movement must be made safe; and test evidence and stop conditions must be defined.

**Review: Technical Review Required**

## Accepted architecture boundary

**Status: Accepted**

[ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) retains engine-critical control in Level 1. Any future accepted direct throttle authority belongs to Level 1. Level 2 shall not gain direct throttle, fuel, or ignition authority and shall not become a hidden dependency for basic engine operation. This record does not alter ADR-0002 or imply DBW acceptance.

## Serviceability and availability

- Replaceability and availability: Unverified.
- Documentation: Yamaha donor-system service documentation is recorded; exact purchased-component application, parts, connectors, and interfaces are not.
- Long-term support and alternatives: Unverified.

## Decision recommendation

**Recommendation: Continue evaluation as primary throttle-body candidate**

This means continued evaluation, not acceptance. Material unresolved issues include exact physical identity, remaining mechanical dimensions, XJ900S intake interface, injector characterization, connector/pin identification, electrical compatibility, DBW control strategy, rusEFI compatibility, and safety validation.

## Direct inspection and measurement still required

### Mechanical and intake geometry

Recorded engine-side OD, ID, cylindrical length, groove geometry, and port spacings are listed above. Still required: per-runner raw dimension records and method details; groove-bottom diameter; full inward bore extent; throttle bore diameter at other defined datums; usable clamp zone and retention/sealing design; airbox-side OD and length; overall width; runner centreline offsets; bridge/bracket dimensions; injector angle relative to runner centreline; injector location from a defined engine-side datum; fuel-rail envelope; front-to-rear depth; servo and TPS housing envelopes; and connector/fuel-hose clearance envelope.

### Physical identification

Still required: photographs of all markings; literal marking transcription; connector photographs; cavity counts; populated cavities; terminal type/size where identifiable; retained wire colours where present; visible condition; impact/drop damage; corrosion; repairs; modified fasteners; disturbed adjustment marks; and sealing condition.

### Unpowered electrical characterization

Only after positive terminal identification and an approved method: injector resistance, relevant TPS resistance observations if technically meaningful, servo terminal identification, and continuity observations needed to establish connector topology. Do not use arbitrary probing or assign pin functions from resistance alone.

### Functional bench characterization

Only after a dedicated reviewed method exists: servo opening/closing; return behavior after removal of power; mechanical binding; throttle angle versus TPS channel 1 and 2; channel correlation/plausibility; repeatability; hysteresis; and, if needed and safely measurable, servo current during controlled unloaded movement. Stall-current testing is not required at this stage.

### Injector and fuel data

Still required: injector markings; authoritative OEM/manufacturer identity if obtainable; connector family; injector dimensions; fuel-rail inlet/interface identification; relevant seal dimensions; and authoritative flow and latency/dead-time data if available. Prefer authoritative manufacturer/Yamaha data first; no flow-bench test is proposed merely because data is absent.

## Required validation

- Verify exact physical candidate identity from markings and authoritative Yamaha evidence where available.
- Complete the listed inspections and measurements without treating them as compatibility evidence in isolation.
- Define and technically review electrical and functional bench methods before energization.
- Evaluate mechanical XJ900S integration in [RESEARCH-0006](../research/RESEARCH-0006-intake-and-throttle-body-interface.md).
- Define safety, fault handling, integration, and road-use validation before any acceptance.

## Traceability

- Related research: [RESEARCH-0002](../research/RESEARCH-0002-level-1-io-and-trigger-requirements.md) and [RESEARCH-0005](../research/RESEARCH-0005-1997-on-electrical-baseline.md)
- Related ADR: [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md)
- Related tests: None recorded
- Roadmap: [Stage 2](../implementation/roadmap.md#stage-2--requirements-and-measurement-capture), [Stage 3](../implementation/roadmap.md#stage-3--engine-management-concept-validation), and [Stage 4](../implementation/roadmap.md#stage-4--efi-bench-system)

## Change history

Dates below identify documentation updates, not measurement dates.

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-17 | Added evidence-bound MT-10 throttle-body-associated pressure-sensor candidate section and separated it from the loose `1WS-82380-00-00` candidate. | Preserve recent pressure-sensor discussion without inventing identity, MAP function, pinout, calibration, or compatibility. |
| 2026-09-15 | Recorded owner direct geometry, explicit groove-position correction, and separate CAD progress with linked RESEARCH-0006 evidence. | Replace resolved dimension gaps while preserving identity, compatibility, and safety-review boundaries. |
| 2026-08-13 | Created the initial component evaluation from purchase provenance and Yamaha 2022 MT-10 service-manual source extraction. | Record donor-system evidence and explicit uncertainty without physical inspection or test execution. |

## Guidance

Purchase, donor-system documentation, appearance, and a proposed use do not establish physical identity, fit, electrical/function compatibility, safety suitability, or acceptance. Keep provenance, donor-system facts, direct observations, measurements, proposals, and accepted decisions separate.

## Navigation

[Component index](README.md) | [Documentation index](../INDEX.md) | [Component evaluation template](../templates/component-evaluation-template.md)
