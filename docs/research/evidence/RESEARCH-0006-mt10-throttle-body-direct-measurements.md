# RESEARCH-0006 evidence: MT-10 throttle-body direct measurements and CAD progress

**Document status: Draft**

**Status: Unverified**

**Review: Technical Review Required**

## Object and evidence type

Object: the on-hand four-cylinder throttle-body assembly identified by the owner as a 2022 Yamaha MT-10 assembly, recorded in [COMP-0005](../../components/COMP-0005-2022-mt10-throttle-body-assembly.md).

Evidence type: owner-performed direct physical measurements and direct observations supplied for this documentation update. These establish dimensions of the measured physical candidate only and are not Yamaha specifications. CAD/prototype progress and owner direct/CAD packaging observations are recorded separately below. Overall compatibility and acceptance remain Unverified.

Measurement/documentation date for the owner-performed direct MT-10 measurements in this evidence set: **2026-08-14**, as established by the owner-provided project chronology. This is a shared date for the measurement work, not a separate date or timestamp for each individual measurement.

Measuring-tool identities, calibration records, detailed measurement methods, photograph identifiers, uncertainty, and tolerances were not supplied with this evidence. The record preserves the supplied values without inventing that metadata or implying that the full research measurement-method requirements have been met.

## Measurement table

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

## Direct observation table

| Feature | Owner direct observation | Boundary |
| --- | --- | --- |
| Internal bore | The 42.8 mm internal bore continues farther inward than the measured 10.5 mm external mating section. | Full inward extent not measured. |
| External bead | No external bead observed at the engine-side interface. | Observation of this candidate only. |
| External step | No external step observed over the measured 10.5 mm cylindrical section. | Does not describe the entire runner. |
| OD groove | Groove physically present. | Groove-bottom diameter was not directly measured and is not calculated here. |
| Bearing-centre reference | Previously measured approximately 32 mm from the engine-side end face. | Approximate owner measurement; reference details require refinement. |
| Runner axes | The four measured runner interfaces share the same nominal axis orientation as observed on the assembly. | No quantified angle, offset, or XJ alignment established. |

## Correction history: groove position

The earlier project reading placed the groove start at **3.0 mm from the engine-side end face**. Direct remeasurement corrected that position to **4.5 mm from the end face**. The earlier 3.0 mm position is superseded and must not be used as the current value. The separately measured **3.0 mm groove width** remains current. Both groove-position values belong to the measurement work documented on **2026-08-14**. Beyond the original-reading-then-correction order, the exact sequence and timestamps within that work were not separately recorded; no different dates are assigned to the two readings.

## Packaging observations requiring datum refinement

These are retained owner direct/CAD packaging observations, not production drawings or design constraints. Their geometric meaning is not extended here; datum, direction, surfaces, and full envelope require refinement before design use.

| Location | Retained project observation |
| --- | --- |
| P2 | ETB/gear-housing clearance relevant to the first 10.5 mm interface region: approximately 8 mm. |
| P3 | Corresponding clearance: approximately 7 mm. |
| P4 | Outer keep-out observation: approximately 11 mm. |

## CAD state

The owner-reported current Fusion model includes:

- A revolved MT-10 port/interface profile and four port bodies.
- Parameter `TB_Port_Pitch = 84.0 mm`, with centre spacing verified as 84.0 mm in the model.
- Packaging/keep-out bodies for P2/P3 and P4.
- An XJ-side construction mid-plane at 126 mm and four XJ-side centres.
- Construction/profile circles using the current working diameters.
- An initial P2 loft test from the MT-10 Ø42.8 mm side toward the XJ P2 Ø33.8 mm side.

This is CAD/prototype design progress, not validation. The loft is a geometry exploration only. The 126 mm value is a current CAD construction/reference value; independent physical evidence establishing it as a physical dimension is not supplied. Successful CAD construction does not establish physical fit, airflow quality, injector targeting, sealing, structural adequacy, manufacturability, or acceptance.

## Unresolved measurements and design work

- Groove-bottom diameter: not directly measured.
- Full inward extent of the 42.8 mm bore; throttle bore at other defined datums; per-runner raw dimension records and measurement-method details.
- XJ runner spacing, intake angle, relevant angles/offsets, and final axial relationship to the MT-10 assembly.
- Total assembly width, complete clearance envelope, airbox-side geometry, and injector position/targeting.
- Usable clamp zone, final clamp/retention design, sealing strategy, material choice, manufacturing tolerances, and final adapter architecture.

The XJ-side working values remain 39.80 mm carburetor-side ID, 33.80 mm aluminium-section ID, and 53.19 mm carburetor-side OD: owner-reported photographic measurements, Unverified, as classified in [RESEARCH-0006](../RESEARCH-0006-intake-and-throttle-body-interface.md). CAD use does not upgrade their evidence class.

## Evidence limitations

These measurements and observations do not establish exact Yamaha OEM assembly part number, donor application, XJ900S compatibility, final adapter geometry, manufacturing tolerances, electrical compatibility, DBW acceptance, safety suitability, or final component acceptance. No tolerance or measurement uncertainty is inferred from displayed precision.

The measured MT-10 spacing of 84.0 mm does not establish four-cylinder compatibility until equivalent XJ spacing and relevant angles/offsets are directly measured and assessed. No Proposal A, B, or C is accepted by this evidence. Physical measurement evidence, donor-manual facts, CAD construction, and validation remain separate.

## Traceability

- [RESEARCH-0006 intake-interface research](../RESEARCH-0006-intake-and-throttle-body-interface.md)
- [COMP-0005 component candidate](../../components/COMP-0005-2022-mt10-throttle-body-assembly.md)
