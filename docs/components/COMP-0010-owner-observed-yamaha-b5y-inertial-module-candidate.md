# COMP-0010: Owner-observed Yamaha B5Y inertial-module candidate

**Purpose:** Evaluate an on-hand Yamaha B5Y inertial-module candidate without
promoting unverified identity, pinout, protocol, compatibility, or safety
claims.

**Document status: Draft**

Identification, direct observations, connector evidence, compatibility status,
safety boundaries, and recommendation are mandatory.

## Candidate identification

- Component: Yamaha B5Y inertial-module candidate
- Manufacturer: Unverified; project context associates the module with Yamaha
  B5Y hardware
- Source model: Unknown
- Model year or range: Unknown
- OEM part number: Unknown
- Variant identifiers: visible label `B5Y0`; visible marking/serial
  `B5Y000M33S205A`
- Source or listing: Not recorded
- Acquisition context: Acquired / on hand; detailed source not recorded
- Evaluation date: 2026-09-16

## Evaluation status

**Status: Unverified**

**Review: Technical Review Required**

This component is not accepted. Physical possession, visible markings, and
connector presence do not establish exact Yamaha part number, source-model
application, function, electrical interface, protocol, safety suitability, or
project compatibility.

## Intended function

**Status: Unverified**

The module may be relevant as a Yamaha-associated B5Y donor/reference candidate
for future inertial, IMU, or lean-angle-related research. The exact component
function is not established by this record.

The module is not a selected or accepted Level 1 fall-event input. If this
component is ever considered for project use, its data may become relevant only
through an explicitly documented, technically reviewed interface and later
architecture decision.

## Applicable requirements

- SAF-001
- SAF-003
- SAF-004
- SAF-008
- REL-002
- SRV-003
- ARC-001
- ARC-002

These requirements are traceability context only. They do not establish that
this component satisfies any requirement.

## Evidence basis

### Direct owner-observed physical evidence

**Status: Confirmed**

| Observation | Evidence boundary |
| --- | --- |
| Module physically on hand | Owner-observed/project-reported physical possession only |
| Visible label `B5Y0` | Direct visible marking; not an exact part-number confirmation |
| Visible marking/serial `B5Y000M33S205A` | Direct visible marking; exact meaning Unknown |
| Four mounting holes | Physical observation only |
| Metal bushings present in mounting holes | Physical observation only |
| Integrated 4-position connector | Physical observation only |
| Associated connector/harness wire colours observed left-to-right as red/white, blue/black, blue/white, black/white | Visual order when viewed from the wire-entry side in the project-shown orientation; this is not OEM cavity numbering |

### Unverified identity and function

**Status: Unverified**

- Exact Yamaha component function.
- Exact Yamaha part number, including whether any candidate number such as
  `B5Y-8593A-00` applies.
- Exact source-model application and model year.
- Whether this component is specifically an OEM IMU, lean-angle sensor,
  inertial sensor, or other module.
- Whether all observed wiring belongs to a stock MT-10 implementation.
- Exact connector manufacturer, family, housing part number, terminal family,
  sealing system, lock design, and depinning method.
- Pinout, supply voltage, ground assignment, CAN usage, CAN H / CAN L
  assignment, baud rate, protocol, message IDs, scaling, update rate, startup
  behavior, stale-data behavior, diagnostics, and failure behavior.

No wire-function assignment is made by this record.

## Known specifications

| Attribute | Value | Unit | Source | Status |
| --- | --- | --- | --- | --- |
| Visible label | `B5Y0` | Not applicable | Owner-observed physical evidence | Confirmed |
| Visible marking/serial | `B5Y000M33S205A` | Not applicable | Owner-observed physical evidence | Confirmed |
| Mounting holes | 4 | Count | Owner-observed physical evidence | Confirmed |
| Mounting-hole bushings | Metal bushings present | Not applicable | Owner-observed physical evidence | Confirmed |
| Integrated connector | 4 positions observed | Count | Owner-observed physical evidence | Confirmed |
| Exact Yamaha part number | Unknown | Not applicable | No authoritative evidence recorded | Unverified |
| Exact function | Unknown | Not applicable | No authoritative evidence recorded | Unverified |
| Source vehicle/model/year | Unknown | Not applicable | No authoritative evidence recorded | Unverified |

## Physical compatibility

- Dimensions: Unknown; no direct measurements recorded.
- Mounting: four mounting holes with metal bushings observed; bolt spacing,
  fastener size, orientation, isolation requirements, and installation
  constraints Unknown.
- Clearances: Unknown.
- Connectors and routing: integrated 4-position connector observed; connector
  family, mating housing, terminal system, orientation requirements, branch
  routing, strain relief, and environmental suitability Unknown.
- Environmental suitability: Unknown for XJ900S installation.
- Required modifications: Unknown.

### Connector evidence

No separate connector identification record is created by this component
record. The connector identity remains unresolved.

- Housing/family: Unknown.
- Mating side: device/header-side integrated connector observed; associated
  connector/harness side observed only by wire-entry-side colour order.
- Terminal family: Unknown.
- Cavity map/orientation: OEM cavity numbering Unknown. The observed
  left-to-right wire colour order from the wire-entry side, in the
  project-shown orientation, is:
  1. red/white
  2. blue/black
  3. blue/white
  4. black/white
- Locking/TPA status: primary lock Unknown; secondary lock / TPA / retainer
  Unknown.
- Removal tool: Unknown.
- Pin functions: Unknown.
- Unresolved evidence: authoritative connector identification, device-side and
  harness-side housing details, terminal family, seal system, cavity numbering
  orientation, depinning method, crimp data, and supported circuit/function
  evidence.

The left-to-right colour order above is a visual observation only and is not
OEM cavity numbering. No temporary project cavity numbers are assigned.

## Electrical or functional compatibility

- Physical connector presence: integrated 4-position connector observed;
  physical mating compatibility remains Unverified.
- Electrical identity: Unknown.
- Supply and signals: Unknown.
- Inputs and outputs: Unknown.
- Communication and diagnostics: Unknown; CAN usage, CAN H / CAN L assignment,
  baud rate, protocol, message IDs, scaling, update rate, startup behavior,
  stale-data behavior, diagnostics, and failure behavior are all Unverified.
- Control authority and failure behavior: no project control authority is
  assigned; failure behavior Unknown.
- Required interface hardware: Unknown.
- Functional compatibility: Unverified.
- Safety suitability: Unverified.
- Final acceptance: not accepted.

Connector appearance, cavity count, wire colour, or physical possession alone
is not compatibility evidence.

## Integration assessment

### Benefits

- The component is physically on hand and may be useful as a B5Y reference
  hardware candidate for future inertial-module research.
- Observed markings and connector/wire-colour evidence provide a starting
  point for later identification work.

### Risks and constraints

- Incorrect pin assignment.
- Wrong supply voltage.
- Bus loading.
- Ground offset.
- Message misinterpretation.
- Stale or frozen data.
- Missing data.
- Startup transient.
- Communication fault.
- False motion or lean interpretation.
- Hidden dependency on Level 1.
- Treating wire colours, cavity count, or visible markings as confirmed
  electrical identity.

### Required adaptations

- None accepted.
- Any future use would require documented connector identification, electrical
  characterization, protocol analysis, fault handling, and technical review.

### Missing evidence

- Authoritative Yamaha part-number and application evidence.
- Direct physical measurements and full photographic evidence set.
- Connector family, exact housings, terminal family, lock design, seal system,
  depinning method, and crimp/terminal replacement data.
- Verified OEM cavity numbering and orientation.
- Pinout, voltage limits, ground reference, communication physical layer,
  protocol, message definitions, timing, startup behavior, diagnostic behavior,
  stale-data behavior, and failure behavior.
- Defined project interface, authority boundary, validation plan, and technical
  review.

## Safety assessment

**Review: Technical Review Required**

Unknown inertial-module data or protocol must not become a dependency for
initial reliable Level 1 operation.

This module has no hidden authority over fuel, ignition, throttle, engine
shutdown, fuel-pump safety, engine synchronization, or any other Level 1
safety-critical function. It must not directly command shutdown, torque
reduction, throttle behavior, injector behavior, ignition behavior, or
fuel-pump behavior in the XJ900S project.

Safe project behavior must not depend on this module until a future design
explicitly defines the interface, authority, diagnostics, stale-data handling,
fault behavior, and validation method, and that design receives technical
review.

## Serviceability and availability

- Replaceability and availability: Unknown.
- Documentation and connector availability: Unknown.
- Long-term support and alternatives: Unknown.

## Decision recommendation

**Recommendation: Continue research**

**Rationale:** The module is physically on hand and may be useful as a
Yamaha-associated B5Y donor/reference candidate, but identity, exact function,
part number, source application, connector identity, pinout, interface,
protocol, failure behavior, and project suitability remain unresolved.

Do not use `Accept` while material compatibility questions remain unresolved.

## Required validation

- Photograph the module, label, marking/serial, mounting features, connector
  face, wire-entry side, latch/lock features, and associated harness context.
- Record direct measurements where physical fit or orientation matters.
- Establish authoritative Yamaha part-number and application evidence, or keep
  identity Unknown.
- Identify connector family, exact housings, terminal system, locking,
  sealing, depinning, and crimp data from authoritative sources or controlled
  physical evidence.
- Establish OEM cavity numbering before using any cavity references.
- Determine pinout, voltage limits, grounding, communication physical layer,
  protocol, diagnostics, and failure behavior through a reviewed method before
  energization or integration.
- Define and technically review any future interface before using module data
  for project decisions or control behavior.

## Traceability

- Related research: [RESEARCH-0007: Super uaEFI Stage 1 hardware
  feasibility](../research/RESEARCH-0007-super-uaefi-stage1-hardware-feasibility.md)
- Related ADRs: None
- Related tests: None
- Roadmap stage: Future research/reference only; not a Stage 1 dependency

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-16 | Created initial component evaluation record. | Preserve on-hand B5Y module observations without promoting unverified identity, pinout, protocol, compatibility, or safety claims. |

## Guidance

Similarity, visible markings, connector presence, wire colours, marketplace
identification, or purchase/acquisition evidence do not establish fit,
electrical identity, protocol, safety suitability, or acceptance.

## Navigation

[Component index](README.md) | [Purchased / on-hand inventory](PURCHASED-ON-HAND-INVENTORY.md) | [Documentation index](../INDEX.md)
