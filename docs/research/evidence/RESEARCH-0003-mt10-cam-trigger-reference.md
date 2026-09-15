# RESEARCH-0003 evidence: MT-10 cam/cylinder-identification reference

**Document status: Draft**

**Status: Unverified**

**Review: Technical Review Required**

## Purpose and boundary

This evidence record preserves the donor/reference material that informed the
cam-phase proposal in
[RESEARCH-0003](../RESEARCH-0003-trigger-and-synchronization-strategy.md).
It separates Yamaha manual facts for the 2022 MT-10 / MT-10 SP system,
owner-reported visual/reference observations, engineering interpretation, and
remaining unknowns.

The overall evidence remains Unverified because donor visual geometry, XJ900S
applicability, and final implementation remain unresolved even where individual
Yamaha manual facts are confirmed for the manual-stated 2022 MT-10 / MT-10 SP
only.

This record is evidence capture only. It does not select a cam sensor, donor
component, final cam target, air gap, bracket, mounting location, phase angle,
decoder edge, or implementation. It does not accept sequential injection,
introduce a Stage 1 cam-sensor dependency, establish road-use suitability, or
claim XJ900S compatibility.

## Source identification

Status: Confirmed for the manual-stated 2022 MT-10 / MT-10 SP source only.

Source: Yamaha 2022 MT-10 / MT-10 SP Service Manual.

- P/N LIT-11616-35-64.
- Manual/model identifier B5Y-28197-10.
- Models MT10N / MT10NC / MT10SPN / MT10SPNC.
- First edition January 2022.

These source-identification facts are not specifications for the XJ900S.

## Confirmed Yamaha manual facts

Status: Confirmed for the manual-stated 2022 MT-10 / MT-10 SP only.

### Sensor existence and service context

Manual section CAMSHAFTS, pages 5-17 to 5-18, lists one cylinder
identification sensor coupler in the cylinder-head-cover removal procedure and
then lists one cylinder identification sensor in the continuation.

This confirms that the manual-stated stock MT-10 / MT-10 SP system includes a
discrete Yamaha engine-mounted cylinder identification sensor serviced in the
camshaft / cylinder-head-cover context.

This does not establish which camshaft carries the target, target geometry,
sensor technology, air gap, phase angle, or XJ900S applicability.

### Electrical output values

Electrical Specifications, manual page 2-11, gives the stock MT-10 cylinder
identification sensor output voltage values as:

| State | Manual-stated output voltage |
| --- | --- |
| ON | 4.8 V |
| OFF | 0.8 V |

These are OEM-manual values for the stock MT-10 circuit behavior only. They do
not establish sensor internal technology, open-collector or push-pull output,
exact supply voltage, direct compatibility with uaEFI, or electrical
interchangeability with another Yamaha sensor.

### Yamaha functional check

Status: Confirmed for the manual-stated 2022 MT-10 / MT-10 SP only.

Electrical Components, pages 8-48 to 8-49, includes the manual procedure for
checking the cylinder identification sensor. The procedure uses a 3-pin test
harness and measures sensor output voltage while the crankshaft is rotated. The
manual states that over each full rotation of the crankshaft the measured
output follows 0.8 V -> 4.8 V -> 0.8 V -> 4.8 V. This is retained as the
manual-stated service-check sequence only.

This service-test wording does not establish the exact number of physical
target recesses or features, exact number of signal edges per cam revolution,
feature angular width or spacing, exact crank/cam phase, duty cycle, polarity
convention for uaEFI, or final decoder configuration. This record does not
reconcile the manual-stated electrical observation with the proposed
single recessed/missing sector concept.

### DTC / ECU relationship

Status: Confirmed for the manual-stated 2022 MT-10 / MT-10 SP only.

P0340 troubleshooting, manual pages 9-160 to 9-162, describes the fault as
failure to receive the normal signal from the cylinder identification sensor.
For continuity checking, it identifies three conductors between the sensor
coupler and ECU coupler:

| Sensor coupler conductor | ECU coupler conductor |
| --- | --- |
| white/black | white/black |
| blue | blue |
| black/blue | black/blue |

The troubleshooting procedure refers installed-condition sensor checking and
sensor replacement back to CAMSHAFTS page 5-17.

This is evidence that the stock MT-10 system uses a three-conductor cylinder
identification sensor connected to the ECU. It does not assign signal, supply,
or ground roles to those wire colours and does not establish electrical
compatibility with uaEFI.

## Evidence-class separation

Confirmed for 2022 MT-10 manual:

- Yamaha calls the device a cylinder identification sensor.
- One sensor and one sensor coupler are shown in the relevant service
  procedure.
- OEM output values are 4.8 V ON and 0.8 V OFF.
- P0340 concerns loss of the normal cylinder-identification signal.
- The service troubleshooting shows three conductors between sensor and ECU.
- Sensor service is referenced to the CAMSHAFTS section.

Unverified visual/reference evidence:

- Exact physical location relative to cylinders 2 and 3.
- Exhaust-side orientation.
- Association with the exhaust camshaft target.
- Ring/annular target topology.
- Recessed/cut-out appearance.
- Approximately 7-8 mm visual axial-width estimate.
- Approximately 20-30 mm visual diameter-increase estimate.

Engineering interpretation / Proposal:

- The MT-10 topology is relevant OEM reference material for evaluating a future
  XJ900S cam-phase target.
- A concentric ferromagnetic target with a recessed/missing sector remains a
  candidate concept.
- A defined target edge may later provide the CMP reference after mechanical
  and electrical validation.

The engineering interpretation is a proposal, not an accepted design.

## Owner-reported visual/reference observations

Status: Unverified

The following points preserve owner-reported visual observations and visual
estimates from the referenced manual/marketplace-photo review. They are not
Yamaha specifications and are not direct dimensional measurements unless
separately stated.

- The sensor appears on the exhaust side of the cylinder head.
- In the referenced view it appears located approximately between cylinders 2
  and 3.
- The apparent trigger feature is associated with the exhaust camshaft.
- The visible feature appears as an annular/ring-like raised section around
  the camshaft with a recessed/cut-out sector.
- The owner visually estimated the axial width of this ring-like section at
  approximately 7-8 mm.
- The owner visually estimated its outside diameter as approximately 20-30 mm
  greater than the adjacent camshaft shaft/body diameter.
- The visible recess appears to be the feature used by the sensor.

These are visual estimates only. The 7-8 mm and 20-30 mm values are not direct
measurements, have no assigned tolerances, and are not derived from image
pixels. They do not establish angular width, recess depth, exact outside
diameter, exact sensor air gap, or the number of target features over the full
360-degree circumference.

Where RESEARCH-0003 uses the concept of one recessed or missing sector, that
remains a proposal/reference concept rather than confirmed MT-10 geometry.

## Evidence limitations

This evidence does not establish:

- Exact MT-10 sensor Yamaha part number.
- Exact exhaust-camshaft Yamaha part number.
- B67-12170-00-00 applicability.
- B67-12180-00-00 applicability.
- Whether either of those candidate part numbers is intake or exhaust.
- Exact target manufacturing geometry.
- Exact target material.
- Exact target OD.
- Exact target width.
- Exact recess depth.
- Exact recess angle.
- Number of target features over a complete revolution.
- Exact sensor-to-target air gap.
- Sensor internal technology.
- Sensor supply voltage.
- Sensor output-driver architecture.
- Sensor pin functions.
- Signal polarity as interpreted by uaEFI.
- Electrical compatibility with uaEFI.
- Final decoder edge.
- Phase angle relative to #1 compression TDC.
- Physical compatibility with the XJ900S.
- A mounting method.
- Safety suitability.
- Validation.
- Acceptance.

If any of those items are established elsewhere later with stronger evidence,
that evidence should be linked from the applicable research, component, test,
or decision record rather than silently promoted here.

## Remaining evidence / next evidence

Status: Unverified

- Obtain authoritative Yamaha parts-catalogue evidence for the exact 2022
  MT-10 cylinder-identification sensor and relevant camshaft part numbers.
- Establish which exact camshaft carries the OEM target.
- Obtain photographs that show the complete target circumference and sensor
  relationship with known orientation.
- Directly measure donor target:
  - shaft/body diameter at a defined datum,
  - target OD,
  - target axial width,
  - recess depth,
  - recess angular width,
  - target axial position,
  - sensor air gap,
  - sensor axis/target relationship.
- Establish the target edge position relative to a defined mechanical timing
  datum.
- Establish sensor pin functions and electrical behavior from authoritative
  documentation or controlled bench measurement.
- Only after those facts exist, assess candidate uaEFI input compatibility and
  prototype geometry.

None of these next-evidence items is complete in this record.

## Traceability

- [RESEARCH-0003 trigger and synchronization strategy](../RESEARCH-0003-trigger-and-synchronization-strategy.md)
- [TEST-PLAN-0002 trigger decoder and timing validation](../../testing/TEST-PLAN-0002-trigger-decoder-and-timing-validation.md)
