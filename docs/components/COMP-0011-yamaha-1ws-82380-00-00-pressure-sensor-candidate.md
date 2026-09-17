# COMP-0011: Yamaha 1WS-82380-00-00 pressure-sensor candidate

**Purpose:** Evaluate the separate loose Yamaha `1WS-82380-00-00`
pressure-sensor candidate without establishing Yamaha application,
calibration, electrical compatibility, or final project acceptance.

**Document status: Draft**

Identification, evidence, compatibility status, safety boundaries, and
recommendation are mandatory.

## Candidate identification

- Component: Separate loose Yamaha pressure-sensor candidate
- Manufacturer: Yamaha — project-supplied identifier context only
- Source model: Unknown
- Model year or range: Unknown
- OEM part number: `1WS-82380-00-00` — project-supplied identifier
- Variant identifiers: `1WS-82380` short form
- Source or listing: Not recorded
- Acquisition context: Separate loose candidate reported as on hand for spare,
  reference, or test use
- Evaluation date: 2026-09-17

## Evaluation status

**Status: Unverified**

**Review: Technical Review Required**

This component is not accepted. A supplied part number, physical possession,
possible visual similarity to another Yamaha sensor, or possible usefulness as
a spare/reference/test item does not establish Yamaha application, exact
function, pinout, supply voltage, pressure range, transfer function,
calibration, uaEFI compatibility, or safety suitability.

## Intended function

**Status: Proposal**

Evaluate the loose `1WS-82380-00-00` pressure-sensor candidate as
reference/test hardware for future MAP/intake-pressure evidence work. This is
not a selected production MAP sensor and not an accepted Diversion 2027
component.

## Applicable requirements

- SYS-007
- SYS-008
- SYS-009
- SAF-003
- SAF-004
- REL-002
- SRV-003
- ARC-001
- DEV-002
- DEV-003
- DOC-002
- DOC-003
- DOC-006
- DOC-008

These requirements are traceability context only. They do not establish that
this component satisfies any requirement.

## Evidence basis

### Supplied/project-reported evidence

**Status: Unverified**

| Item | Evidence boundary |
| --- | --- |
| Supplied/project-reported part number | `1WS-82380-00-00`; retained as project-supplied identifier only |
| Short-form identifier | `1WS-82380`; shorthand only |
| Acquisition/on-hand status | Separate loose pressure-sensor candidate reported as physically on hand |
| Possible project use | Spare/reference/test candidate only; not selected or accepted |

### Explicitly unresolved identity and application

**Status: Unverified**

- Exact Yamaha application.
- Whether any MT-07 application applies.
- Exact pressure-sensor function.
- Exact sensor manufacturer, internal architecture, pressure element, and
  temperature compensation.
- Connector identity, mating housing, terminal family, cavity numbering,
  locking, sealing, depinning method, and crimp data.
- Pinout, supply/reference requirement, ground/reference architecture, signal
  output, output impedance, pressure units, valid pressure range, absolute
  versus gauge behavior, atmospheric output, open/short fault behavior,
  transfer function, calibration, and plausibility behavior.
- Electrical protection and wiring-protection requirements.
- uaEFI/rusEFI compatibility.
- Physical mounting and hose/port interface.
- Final project acceptance.

Do not infer official Yamaha application from the `1WS` prefix. Do not state
that this is an MT-07 sensor unless authoritative retained evidence establishes
that application.

## Known specifications

| Attribute | Value | Unit | Source | Status |
| --- | --- | --- | --- | --- |
| Supplied/project-reported part number | `1WS-82380-00-00` | Not applicable | Project discussion | Unverified |
| Short-form identifier | `1WS-82380` | Not applicable | Derived from supplied identifier | Unverified |
| Physical state | Separate loose pressure-sensor candidate reported on hand | Not applicable | Project discussion | Unverified |
| Exact Yamaha application | Unknown | Not applicable | No authoritative evidence recorded | Unverified |
| Exact function | Unknown; pressure/MAP role remains a candidate interpretation | Not applicable | No authoritative evidence recorded | Unverified |
| Connector identity | Unknown | Not applicable | No retained connector evidence | Unverified |
| Pinout | Unknown | Not applicable | No retained pinout evidence | Unverified |
| Supply/reference | Unknown | V | No retained electrical evidence | Unverified |
| Ground/reference | Unknown | Not applicable | No retained electrical evidence | Unverified |
| Signal output | Unknown | V | No retained electrical evidence | Unverified |
| Pressure range | Unknown | kPa or other units Unknown | No retained pressure evidence | Unverified |
| Transfer function | Unknown | Not applicable | No retained calibration evidence | Unverified |
| Absolute/gauge behavior | Unknown | Not applicable | No retained pressure evidence | Unverified |
| Temperature compensation | Unknown | Not applicable | No retained evidence | Unverified |
| Electrical protection requirements | Unknown | Not applicable | No retained evidence | Unverified |
| uaEFI compatibility | Unknown | Not applicable | No retained compatibility evidence | Unverified |
| Final acceptance | Not accepted | Not applicable | Project status | Unverified |

No 5 V requirement, 0.5-4.5 V transfer, 100 kPa, 115 kPa, 250 kPa range,
Bosch/Denso architecture, connector cavity order, or wire-colour function is
established by this record.

## Physical compatibility

- Dimensions: Unknown.
- Mounting: Unknown.
- Pressure port/hose interface: Unknown.
- Clearances: Unknown.
- Connectors and routing: Unknown.
- Environmental suitability: Unknown for XJ900S installation.
- Required modifications: Unknown.

### Connector evidence

No separate connector identification record is created by this component
record. The connector identity remains unresolved.

- Housing/family: Unknown.
- Mating side: Unknown.
- Terminal family: Unknown.
- Cavity map/orientation: Unknown.
- Primary locking method: Unknown.
- Secondary lock / TPA / retainer: Unknown.
- Seal/cavity plug: Unknown.
- Removal tool and depinning method: Unknown.
- Crimp tool/terminal replacement data: Unknown.
- Pin functions: Unknown.
- Unresolved evidence: all connector identity, serviceability, cavity
  numbering, terminal, sealing, depinning, and crimp data.

Physical mating or a housing that looks identical to another Yamaha sensor
does not establish electrical or calibration equivalence.

## Electrical or functional compatibility

- Supply/reference: Unknown.
- Ground/reference architecture: Unknown.
- Signal output: Unknown.
- Output voltage range: Unknown.
- Transfer function and calibration: Unknown.
- Pressure units and valid range: Unknown.
- Absolute versus gauge behavior: Unknown.
- Behavior at atmospheric pressure: Unknown.
- Open/short fault behavior: Unknown.
- Sensor plausibility behavior: Unknown.
- ECU ADC/input range compatibility: Unknown.
- rusEFI calibration implementation: Unknown.
- Power-up behavior: Unknown.
- Wiring protection: Unknown.
- uaEFI compatibility: Unverified.

The existence of Super uaEFI B26 / `MM100_IN_MAP1_ANALOG`, B16 +5 V, or B23
GNDA resources does not prove compatibility with this Yamaha candidate. A
sensor producing plausible voltage would not establish correct calibration.

## Integration assessment

### Benefits

- The candidate is reported as a separate loose on-hand item and may be useful
  as spare/reference/test hardware.
- The supplied `1WS-82380-00-00` identifier gives a starting point for later
  authoritative Yamaha parts research.

### Risks and constraints

- Incorrect Yamaha application.
- Incorrect pressure-sensor function.
- Wrong supply/reference voltage.
- Incorrect ground/reference routing.
- Incorrect pinout or connector cavity orientation.
- Wrong pressure range or absolute/gauge assumption.
- Wrong transfer function or calibration.
- ADC range mismatch.
- Missing open/short/fault behavior.
- Treating spare/reference/test usefulness as production selection.

### Required adaptations

- None accepted.
- Any future use requires authoritative identity/application evidence or
  carefully retained direct evidence, connector identification, pinout,
  electrical interface definition, calibration evidence, and technical review.

### Missing evidence

- Authoritative Yamaha application and part-number evidence.
- Complete photographs and literal marking transcription.
- Connector family, exact housing, mating housing/header, terminal family,
  cavity numbering and viewing orientation, locking, sealing, depinning, and
  crimp data.
- Pinout, supply/reference, ground/reference, signal output, pressure range,
  absolute/gauge behavior, atmospheric output, fault behavior, transfer
  function, calibration, power-up behavior, and protection requirements.
- uaEFI/rusEFI MAP configuration and validation evidence.
- Physical mounting/pressure plumbing evidence.
- A technically reviewed bench-test method before energization.

## Safety assessment

**Review: Technical Review Required**

MAP/intake-pressure sensing is part of Level 1 engine-management fuel and
ignition calculation. Incorrect identity, wiring, pressure scaling, or
calibration can cause incorrect fueling or load estimation.

Do not authorize powered testing from generic three-pin automotive sensor
conventions. Before any powered work, require positive connector
identification, pinout evidence, supply/reference evidence, current-limited
and protected test method, expected output limits, stop conditions, and
retained validation evidence.

## Serviceability and availability

- Replaceability and availability: Unknown.
- Documentation and connector availability: Unknown.
- Long-term support and alternatives: Unknown.

## Decision recommendation

**Recommendation: Continue research**

**Rationale:** The separate loose `1WS-82380-00-00` candidate is reported on
hand and may be useful as spare/reference/test hardware, but exact Yamaha
application, function, connector identity, pinout, supply/reference, pressure
range, transfer function, calibration, uaEFI compatibility, safety
suitability, and acceptance remain unresolved.

Do not use `Accept` while material compatibility questions remain unresolved.

## Required validation

- Preserve photographs of all markings and the connector face before relying
  on any identity claim.
- Establish authoritative Yamaha part-number/application evidence, or retain
  application as Unknown.
- Identify connector housing, mating housing/header, terminal family, cavity
  numbering orientation, locks, seals, depinning method, and crimp/terminal
  replacement data.
- Establish pinout, supply/reference, ground/reference, signal output, output
  voltage range, pressure units and range, absolute/gauge behavior,
  atmospheric output, transfer function, calibration, and fault behavior.
- Confirm ECU ADC/input range compatibility and rusEFI calibration
  implementation only after sensor evidence exists.
- Define and technically review any powered test method before energization.
- Keep this loose candidate separate from the MT-10 throttle-body-associated
  pressure-sensor candidate unless direct evidence proves a relationship.

## Traceability

- Related research: [RESEARCH-0007: Super uaEFI Stage 1 hardware
  feasibility](../research/RESEARCH-0007-super-uaefi-stage1-hardware-feasibility.md)
- Related component: [COMP-0005: Owner-reported 2022 Yamaha MT-10
  throttle-body assembly](COMP-0005-2022-mt10-throttle-body-assembly.md)
- Related ADRs: None
- Related tests: None
- Roadmap stage: Stage 3 / Stage 4 evidence candidate only; not selected for
  production use

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-17 | Created initial component evaluation record. | Preserve the separate loose `1WS-82380-00-00` pressure-sensor candidate without promoting unverified Yamaha application, pinout, calibration, compatibility, or acceptance. |

## Guidance

Physical possession, a supplied Yamaha identifier, donor context, matching
connector appearance, physical fit, or plausible voltage output do not
establish electrical identity, pressure range, transfer function, calibration,
uaEFI compatibility, safety suitability, or acceptance.

## Navigation

[Component index](README.md) | [Purchased / on-hand inventory](PURCHASED-ON-HAND-INVENTORY.md) | [Documentation index](../INDEX.md)
