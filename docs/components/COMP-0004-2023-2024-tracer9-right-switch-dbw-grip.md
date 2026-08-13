# COMP-0004: Owner-Reported 2023-2024 Yamaha Tracer 9 Right Switch and DBW Grip

**Purpose:** Record and evaluate the purchased right-hand switch assembly with
integrated drive-by-wire throttle grip as a candidate without selecting DBW or
establishing Yamaha application, compatibility, acceptance, or validation.

**Document status: Draft**

Identification, evidence, compatibility status, safety, and recommendation are
mandatory.

## Candidate identification

- Component: Right-hand switch assembly with integrated drive-by-wire throttle
  grip - owner-provided identification
- Manufacturer: Yamaha - owner-provided identification; marking not recorded
- Source model: Tracer 9, MTT890/B5U - owner-provided identification; official
  Yamaha application not independently verified
- Model year or range: 2023-2024 - owner-provided identification; official
  Yamaha application not independently verified
- OEM part number: `B5U-8291R-10` - supplied part number; Yamaha application
  and exact variant not independently verified
- Variant identifiers: MTT890/B5U - owner-provided identification; exact market
  and variant applicability Unverified
- Source or listing: Owner-provided purchase identification; original listing
  URL and seller record are not currently retained in the repository
- Evaluation date: 2026-08-11

## Evaluation status

**Status: Unverified**

**Review: Technical Review Required**

## Source register

| Source ID | Source | Scope and evidence boundary |
| --- | --- | --- |
| COMP-0004-SRC-001 | Owner-reported purchase identification | Acquisition provenance only; does not confirm Yamaha application, exact model-year range, market, variant, marking, condition, connector, electrical specification, compatibility, or acceptance. |
| COMP-0004-SRC-002 | *2024 Yamaha Tracer 9 GT+ Service Manual*, BLG-28197-70-E0; model MTT09DAR; first edition May 2023; Yamaha Motor Co., Ltd. | Authoritative Yamaha evidence only for the documented MTT09DAR 2024 Tracer 9 GT+ donor/reference architecture. It does not identify, establish electrical equivalence of, or officially apply to the purchased owner-reported MTT890/B5U assembly with supplied part number `B5U-8291R-10`. |

## Intended function

The assembly is recorded for evaluation as a possible source of right-hand
rider switches and a DBW throttle-grip mechanism. No project use is selected.
The current accepted architecture permits cable throttle initially; DBW remains
a separately evaluated future proposal requiring a dedicated decision, safety
architecture, redundant sensing and plausibility evidence, actuator control,
fault handling, safe states, and validation.

## Subsystem evaluation boundaries

The assembly remains one component record, but its two functional subsystems
shall be evaluated independently.

| Subsystem | Evaluation scope | Current status | Current recommendation |
| --- | --- | --- | --- |
| A. Rider switch functions | Individual switch functions, contact or communication behavior, connector and electrical interface, diagnostics, engine-stop or starter relevance, Level 1/Level 2 assignment, and physical integration | Unverified | Continue research |
| B. Accelerator-position / DBW grip functions | Accelerator-position sensing, channel independence, transfer functions, plausibility, mechanical return, fault behavior, diagnostics, Level 1 interface, and relationship to any separately evaluated throttle actuator | Unverified for purchased candidate and project | Continue research |

Future evidence may change the status or recommendation for either subsystem
without changing the other. Acceptance or rejection of the rider-switch
functions does not accept or reject the DBW/accelerator-position functions.
Acceptance or rejection of the DBW/accelerator-position functions does not
accept or reject the rider-switch functions.

No subsystem, electrical interface, DBW strategy, or component compatibility
is accepted by this separation.

### Confirmed project-provenance information

**Status: Confirmed**

- The owner reports that the project purchased the assembly.
- The owner identifies the source as a 2023-2024 Yamaha Tracer 9, MTT890/B5U.
- The owner supplied part number `B5U-8291R-10`.

These statements confirm only owner-reported acquisition provenance. They do
not independently verify Yamaha application, exact model-year range, variant,
part-number applicability, electrical specification, DBW compatibility, or
project suitability.

## Confirmed Yamaha Tracer 9 GT+ reference architecture

**Status: Confirmed**

Confirmed in this section applies only to the documented MTT09DAR 2024 Tracer
9 GT+ donor/reference architecture in COMP-0004-SRC-002. It is not a direct
observation of the purchased MTT890/B5U physical candidate.

### Dual accelerator-position sensing

The Yamaha reference system monitors two accelerator-position sensor signals:

- Diagnostic code 14 - accelerator position sensor signal 1
- Diagnostic code 15 - accelerator position sensor signal 2

For both channels in the documented MTT09DAR system, Yamaha diagnostic-tool
display values are 14-18 fully closed, 82-92 fully open, and 7-12 when the
throttle grip is moved past normal closed position in the deceleration
direction. These are diagnostic-tool display values only; they are not volts,
degrees, percentages, or direct transfer-function values. No linearity is
inferred.

### APS diagnostic trouble codes

The documented Yamaha reference architecture includes P2122, P2123, P2127,
P2128, and P2138.

- P2122 and P2127 low-voltage detection: 0.25 V or less.
- P2123 and P2128 high-voltage detection: 4.75 V or more.
- P2138: difference/deviation between accelerator-position sensor output
  voltage 1 and output voltage 2.

These DTC thresholds are reference-system fault-detection criteria. They do
not establish normal operating endpoints, sensor transfer functions, or a
supply voltage for the purchased candidate.

### Documented APS-to-ECU conductors

The MTT09DAR ECU layout and troubleshooting document six APS conductor paths:
White/Red, Yellow, Yellow/Red, Brown, White/Black, and Yellow/Black.

| MTT09DAR ECU cavity | Conductor colour |
| --- | --- |
| 35 | White/Red |
| 42 | Yellow |
| 45 | Yellow/Red |
| 51 | Brown |
| 54 | White/Black |
| 57 | Yellow/Black |

These are donor/reference-system ECU cavity assignments only, not the purchased
assembly's connector cavity numbers. The source is not used here to assign
Vref, ground, APS1, or APS2 functions to individual wire colours. The ECU
layout treats the grip-warmer circuit separately from these six APS conductor
paths; this does not establish the purchased assembly's connector partition or
internal wiring.

### Service relationship to right handlebar switch

In the MTT09DAR APS troubleshooting procedure, if the two APS diagnostic checks
do not pass, Yamaha instructs replacement of the `handlebar switch (right)`.
This supports only that Yamaha treats the accelerator-position sensor as
service-integrated with the right-handlebar-switch assembly in this documented
reference architecture. The purchased B5U assembly has not been physically
verified to have the same construction.

### Documented APS fail-safe behavior

For P2122, P2123, P2127, P2128, and P2138, the documented Yamaha reference
system records poor engine response, loss of engine power, and unstable idle.
Where documented, its response includes accelerator opening fixed to 0 degrees,
YCC-T evacuation activated, output restricted, O2 feedback not carried out,
fuel cut prohibited by accelerator opening, ISC feedback not carried out, ISC
learning not carried out, quick shift not carried out, and ACC fixed OFF.

These are Yamaha donor/reference-system responses, not accepted Diversion 2027
safe states. They shall not be copied into the project without a dedicated
safety analysis and accepted design.

### Yamaha evidence locations

| Subject | Printed reference in COMP-0004-SRC-002 |
| --- | --- |
| ECU coupler layout and APS conductors | 9-9–9-11 |
| APS self-diagnostic and DTC table | 9-73 |
| P2122, P2123, P2127, P2128, and P2138 troubleshooting | 9-282–9-284 |
| Diagnostic modes 14/15 and right-handlebar-switch replacement | 9-284 |

## Applicable requirements

- [SYS-003](../requirements/system-requirements.md#sys-003)
- [SYS-006](../requirements/system-requirements.md#sys-006)
- [SYS-009](../requirements/system-requirements.md#sys-009)
- [SYS-010](../requirements/system-requirements.md#sys-010)
- [SYS-011](../requirements/system-requirements.md#sys-011)
- [SAF-002](../requirements/system-requirements.md#saf-002)
- [SAF-003](../requirements/system-requirements.md#saf-003)
- [SAF-004](../requirements/system-requirements.md#saf-004)
- [SAF-005](../requirements/system-requirements.md#saf-005)
- [SAF-007](../requirements/system-requirements.md#saf-007)
- [REL-002](../requirements/system-requirements.md#rel-002)
- [REL-004](../requirements/system-requirements.md#rel-004)
- [REL-006](../requirements/system-requirements.md#rel-006)
- [SRV-001](../requirements/system-requirements.md#srv-001)
- [SRV-002](../requirements/system-requirements.md#srv-002)
- [SRV-003](../requirements/system-requirements.md#srv-003)
- [SRV-004](../requirements/system-requirements.md#srv-004)
- [ARC-001](../requirements/system-requirements.md#arc-001)
- [ARC-003](../requirements/system-requirements.md#arc-003)
- [ARC-004](../requirements/system-requirements.md#arc-004)
- [ARC-006](../requirements/system-requirements.md#arc-006)
- [ARC-008](../requirements/system-requirements.md#arc-008)
- [DEV-002](../requirements/system-requirements.md#dev-002)
- [DEV-003](../requirements/system-requirements.md#dev-003)
- [DEV-008](../requirements/system-requirements.md#dev-008)
- [DOC-002](../requirements/system-requirements.md#doc-002)
- [DOC-003](../requirements/system-requirements.md#doc-003)
- [DOC-006](../requirements/system-requirements.md#doc-006)
- [DOC-008](../requirements/system-requirements.md#doc-008)

## Known specifications

| Attribute | Value | Unit | Source | Status |
| --- | --- | --- | --- | --- |
| Owner-reported source model | Tracer 9, MTT890/B5U | Not applicable | Owner-provided purchase identification | Confirmed as owner-reported provenance |
| Owner-reported source model years | 2023-2024 | Year range | Owner-provided purchase identification | Confirmed as owner-reported provenance |
| Supplied part number | B5U-8291R-10 | Not applicable | Owner-provided seller/product identification | Confirmed as reported; Yamaha application Unverified |
| Exact Yamaha application and variant | Unknown | Not applicable | No authoritative Yamaha parts source recorded | Unverified |
| Switch functions and contact logic | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Connector identities and purchased-candidate pinout | Unknown | Unknown | No authoritative documentation or documented direct inspection recorded | Unverified |
| Purchased-candidate supply voltage, current, and signal levels | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Throttle-grip sensor channels and transfer functions | MTT09DAR reference system: dual monitored APS channels; purchased-candidate topology and transfer functions Unknown | Not applicable | Yamaha service manual; no documented direct candidate measurement | Confirmed for reference architecture; Unverified for purchased candidate |
| Sensor redundancy, plausibility, and fault behavior | MTT09DAR reference system: dual APS channels, deviation monitoring, and documented donor fail-safe behavior; purchased candidate and project implementation Unknown | Not applicable | Yamaha service manual; no candidate validation | Confirmed for reference architecture; Unverified for purchased candidate and project |
| Mechanical clamp, grip, and handlebar dimensions | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |

## Physical compatibility

- Dimensions: Unknown
- Mounting: Handlebar diameter, clamp arrangement, locating features, throttle
  tube or grip arrangement, and retention are Unknown.
- Clearances: Brake lever, master cylinder, handguard, tank, fairing, cable or
  harness, and full-steering-lock clearances are Unknown.
- Connectors and routing: Connector families, pin count, harness length,
  strain relief, sealing, routing, and bend radius are Unknown.
- Environmental suitability: Used condition, sealing, water protection,
  vibration suitability, temperature range, and wear have not been evaluated.
- Required modifications: Unknown; no handlebar drilling, connector adaptation,
  harness alteration, or throttle integration is defined or approved.

Connector fit, clamp fit, grip movement, or physical resemblance does not
establish electrical, functional, DBW, or safety compatibility.

## Electrical or functional compatibility

- Supply and signals: The MTT09DAR source documents reference-system APS paths
  and diagnostic criteria, but the purchased candidate's exact pinout, supply,
  grounds, sensor outputs, switch contacts, and protection needs remain
  Unverified. Do not energize it until positive connector/pin identification
  and a reviewed test method exist.
- Inputs and outputs: Rider-switch functions remain independently Unverified.
  Throttle-grip sensing, possible communications, and any actuator relationship
  remain Unverified for the purchased candidate.
- Communication and diagnostics: Unknown; no discrete, resistive, serial, or
  network interface is assumed for the purchased candidate.
- Control authority and failure behavior: If DBW were later accepted, direct
  throttle authority would remain Level 1. Non-engine rider-switch functions
  may be assigned according to the accepted Level 1/Level 2 architecture
  without transferring engine authority. Level 2 shall not receive direct
  throttle, fuel, or ignition authority. The Yamaha donor ECU connection is
  useful reference evidence only, not an accepted project implementation.
- Required interface hardware: Connector mates, supply and protection circuits,
  sensor interfaces, possible network hardware, throttle actuator, and
  mechanical adaptations are Unknown.

The assembly's integrated DBW grip does not establish that the project has a
compatible throttle actuator, ECU, firmware strategy, redundant sensing path,
or safe-state design.

## Integration assessment

### Benefits

- The purchased assembly is available for non-destructive identification,
  inspection, and later reviewed bench characterization.
- The Yamaha reference architecture provides authoritative production-reference
  evidence for a dual-channel APS architecture and associated safety-monitoring
  pattern, without verifying physical-candidate identity, topology, or
  compatibility.

### Risks and constraints

- Official Yamaha application of `B5U-8291R-10`; exact model-year coverage;
  exact market/variant; markings; connector manufacturer/family; physical
  connector cavity numbering; exact purchased-candidate pinout; actual wire
  colours; harness branching; supply/reference, ground, and APS signal
  assignments; voltage-versus-angle and channel-correlation functions;
  mechanical grip angle; return force; hysteresis; wear; environmental
  condition; and rusEFI compatibility remain Unverified.
- DBW is not selected, and this component shall not create a hidden DBW or
  donor-system dependency.
- Incorrect energization or interpretation could damage the assembly or create
  unsafe throttle, starter, or engine-stop behavior.
- Mechanical installation could impair throttle return, braking control,
  steering clearance, or access to engine-stop controls.

### Required adaptations

- Unknown; no adaptation is proposed or accepted.

### Missing evidence

- Authoritative Yamaha parts-catalogue application and exact variant evidence.
- Retained seller record, photographs, markings, connector identities, and
  harness details.
- Purchased-candidate pinout, electrical limits, switch logic, sensor topology,
  transfer functions, and diagnostic behavior.
- Mechanical dimensions, operating angle, return behavior, wear, sealing, and
  environmental condition.
- An accepted throttle strategy, Level 1 authority design, safety analysis,
  plausibility rules, safe states, fault handling, and validation plan.

## Safety assessment

The assembly contains rider controls and an integrated DBW throttle grip. An
incorrect electrical interface, mechanical fit, signal interpretation, failure
response, or authority assignment could cause loss of engine-stop function,
unexpected starter behavior, incorrect throttle demand, failure to return, or
unintended engine output. No DBW architecture, throttle compatibility,
switch-function compatibility, installation safety, or road readiness is
established.

The reference system's two-channel APS and Yamaha plausibility monitoring
demonstrate the type of redundancy and fault detection used in a production
system. They do not establish that merely reading two analogue channels is
sufficient for Diversion 2027. Project acceptance will require defined channel
plausibility rules, electrical fault handling, mechanical return behavior, safe
state, throttle-actuator coordination, power/reset behavior, diagnostics, and
fault-injection validation. This component record does not define those final
rules.

Review: Technical Review Required

## Accepted architecture boundary

**Status: Accepted**

[ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) assigns
fuel, ignition, engine synchronization, fuel-pump safety, engine shutdown, and
any later accepted direct DBW authority to Level 1. Level 2 may handle
documented non-engine rider-switch functions according to the accepted
architecture, but that assignment shall not transfer engine authority. Level 2
shall not receive direct throttle, fuel, or ignition authority and shall not
become required for basic engine operation. This component record does not
alter that decision.

## Serviceability and availability

- Replaceability and availability: Unknown
- Documentation and connector availability: Yamaha MTT09DAR donor/reference
  service documentation is recorded; exact purchased-component application,
  parts, connectors, and interfaces are not.
- Long-term support and alternatives: Unknown

## Decision recommendation

**Recommendation: Continue research**

**Rationale:** The Yamaha reference architecture provides authoritative
production-reference evidence for APS architecture and safety monitoring, but
the physical candidate's official application, identity, electrical interfaces,
mechanical requirements, switch behavior, DBW safety behavior, and compatibility
remain Unverified. Bench energization and DBW evaluation are premature until
positive identification and a reviewed method exist.

## Required validation

### Future direct inspection

- Verify the part number, exact model-year range, market, and variant using an
  authoritative Yamaha parts catalogue; marketplace listings do not establish
  official application.
- Photograph all labels and moulded markings.
- Photograph every connector from terminal and harness sides; record connector
  cavity counts, populated cavities, actual wire colours, harness branching,
  and connector/manufacturer markings.
- Record mechanical grip travel, any over-closed/deceleration-direction movement
  if physically present, free return behavior, visible wear/damage, and clamp
  and locating geometry.

### Future electrical characterization

Only after positive connector/pin identification and a reviewed method:

- Identify sensor supply/reference paths, sensor grounds, APS channel 1, and
  APS channel 2.
- Measure output versus grip angle and both channels simultaneously;
  characterize correlation, closed, open, and any over-closed region.
- Repeat measurements for hysteresis and repeatability.
- Test open/short fault behavior only in a controlled bench system after a
  dedicated safety method exists.

Do not energize the component merely to match Yamaha diagnostic values, and do
not prescribe an arbitrary supply voltage from the 0.25/4.75 V DTC thresholds.

Keep rider-switch evaluation separate from DBW evaluation; acceptance of or
rejection of either subsystem shall not imply acceptance or rejection of the
other. Create a dedicated DBW requirements, safety, architecture, and
validation record before any DBW selection or powered motorcycle integration.
Define acceptance criteria and complete technical review before installation or
road use.

## Traceability

- Related research: [RESEARCH-0002](../research/RESEARCH-0002-level-1-io-and-trigger-requirements.md)
  and [RESEARCH-0005](../research/RESEARCH-0005-1997-on-electrical-baseline.md)
- Related ADRs: [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md);
  no DBW or component-selection ADR is recorded
- Related tests: None recorded
- Roadmap stage: [Stage 2 - requirements and measurement
  capture](../implementation/roadmap.md#stage-2--requirements-and-measurement-capture)
  and [Stage 3 - engine-management concept
  validation](../implementation/roadmap.md#stage-3--engine-management-concept-validation)

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-13 | Added authoritative Yamaha Tracer 9 GT+ APS reference-architecture extraction. | Add donor/reference evidence without verifying purchased-candidate identity or accepting DBW. |
| 2026-08-12 | Added independent rider-switch and accelerator-position/DBW subsystem evaluation boundaries. | Allow separate future status and recommendation without transferring engine authority or accepting either subsystem. |
| 2026-08-11 | Created initial component evaluation record. | Record the purchased candidate and owner-reported provenance without selecting DBW or accepting application, compatibility, or validation. |

## Guidance

Similarity, connector fit, grip movement, purchase, and donor-system
documentation do not establish physical identity, fit, electrical/function
compatibility, safety suitability, or acceptance. Keep source provenance,
donor/reference-system facts, direct observations, measurements, proposals, and
accepted decisions separate.

## Navigation

[Component index](README.md) | [Documentation index](../INDEX.md) | [Component evaluation template](../templates/component-evaluation-template.md)
