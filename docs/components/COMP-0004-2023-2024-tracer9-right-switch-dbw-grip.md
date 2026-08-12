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
  and variant applicability Unknown
- Source or listing: Owner-provided purchase identification; original listing
  URL and seller record are not currently retained in the repository
- Evaluation date: 2026-08-11

## Evaluation status

**Status: Unverified**

**Review: Technical Review Required**

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
| B. Accelerator-position / DBW grip functions | Accelerator-position sensing, channel independence, transfer functions, plausibility, mechanical return, fault behavior, diagnostics, Level 1 interface, and relationship to any separately evaluated throttle actuator | Unverified | Continue research |

Future evidence may change the status or recommendation for either subsystem
without changing the other. Acceptance or rejection of the rider-switch
functions does not accept or reject the DBW/accelerator-position functions.
Acceptance or rejection of the DBW/accelerator-position functions does not
accept or reject the rider-switch functions.

No subsystem, electrical interface, DBW strategy, or component compatibility
is accepted by this separation.

### Confirmed project-provenance information

- The owner reports that the project purchased the assembly.
- The owner identifies the source as a 2023-2024 Yamaha Tracer 9, MTT890/B5U.
- The owner supplied part number `B5U-8291R-10`.

These statements confirm only owner-reported acquisition provenance. They do
not independently verify Yamaha application, exact model-year range, variant,
part-number applicability, electrical specification, DBW compatibility, or
project suitability.

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
| Owner-reported source model | Tracer 9, MTT890/B5U | Not applicable | Owner-provided purchase identification | Confirmed |
| Owner-reported source model years | 2023-2024 | Year range | Owner-provided purchase identification | Confirmed |
| Supplied part number | B5U-8291R-10 | Not applicable | Owner-provided seller/product identification | Confirmed as reported; Yamaha application Unverified |
| Exact Yamaha application and variant | Unknown | Not applicable | No authoritative Yamaha parts source recorded | Unverified |
| Switch functions and contact logic | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Connector identities and pinout | Unknown | Unknown | No authoritative documentation or documented direct inspection recorded | Unverified |
| Supply voltage, current, and signal levels | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Throttle-grip sensor channels and transfer functions | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Sensor redundancy, plausibility, and fault behavior | Unknown | Unknown | No authoritative documentation or validated test recorded | Unverified |
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

- Supply and signals: Unknown; do not energize the assembly until the exact
  pinout, supply, grounds, sensor outputs, switch contacts, and protection needs
  are established from authoritative evidence or a reviewed test method.
- Inputs and outputs: Right-hand switch functions, throttle-grip sensing,
  possible communications, and any actuator relationship are Unknown.
- Communication and diagnostics: Unknown; no discrete, resistive, serial, or
  network interface is assumed.
- Control authority and failure behavior: If DBW were later accepted, direct
  throttle authority would remain Level 1. Non-engine rider-switch functions
  may be assigned according to the accepted Level 1/Level 2 architecture
  without transferring engine authority. Level 2 shall not receive direct
  throttle, fuel, or ignition authority. Missing, shorted, implausible, stale,
  or disagreeing signals and mechanical return behavior remain Unverified.
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
- A production assembly may provide useful packaging evidence if exact identity
  and functions are established.

### Risks and constraints

- Yamaha application, exact variant, and part-number scope are not
  independently verified.
- Connector, pinout, supply, switch logic, sensor topology, transfer functions,
  diagnostics, and failure behavior are unknown.
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
- Authoritative wiring, pinout, electrical limits, switch logic, throttle-sensor
  topology, transfer functions, and diagnostic behavior.
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

Review: Technical Review Required

## Accepted architecture boundary

**Status: Accepted**

[ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) assigns
fuel, ignition, engine synchronization, fuel-pump safety, engine shutdown, and
any later accepted direct DBW authority to Level 1. Level 2 may handle
documented non-engine rider-switch functions according to the accepted
architecture, but that assignment shall not transfer engine authority. Level 2
shall not gain direct fuel, ignition, or throttle authority or become required
for basic engine operation. This component record does not alter that decision.

## Serviceability and availability

- Replaceability and availability: Unknown
- Documentation and connector availability: Official application, wiring,
  pinout, connector, diagnostic, and service information are not recorded.
- Long-term support and alternatives: Unknown

## Decision recommendation

**Recommendation: Continue research**

**Rationale:** The assembly is available for identification, but its official
application, electrical interfaces, mechanical requirements, switch behavior,
DBW safety behavior, and relationship to any future accepted architecture
remain unverified. Bench energization and DBW evaluation are premature until
authoritative information and a reviewed method exist.

## Required validation

- Verify the part number, exact model-year range, market, and variant using an
  authoritative Yamaha parts source.
- Photograph all markings, connectors, cavities, wire colours, harness routing,
  clamp and locating features, grip, and visible condition.
- Obtain authoritative wiring and service information before applying power or
  assuming any pin function.
- Identify switch contacts, supplies, grounds, sensor channels, transfer
  functions, any communication interface, diagnostic behavior, and failure
  states through authoritative evidence and reviewed non-destructive testing.
- Measure mechanical dimensions, operating range, return behavior, free play,
  retention, and clearance using a documented method.
- Keep switch-function evaluation separate from DBW evaluation; acceptance of
  or rejection of either subsystem shall not imply acceptance or rejection of
  the other.
- Create a dedicated DBW requirements, safety, architecture, and validation
  record before any DBW selection or powered motorcycle integration.
- Define acceptance criteria and complete technical review before installation
  or road use.

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
| 2026-08-12 | Added independent rider-switch and accelerator-position/DBW subsystem evaluation boundaries. | Allow separate future status and recommendation without transferring engine authority or accepting either subsystem. |
| 2026-08-11 | Created initial component evaluation record. | Record the purchased candidate and owner-reported provenance without selecting DBW or accepting application, compatibility, or validation. |

## Guidance

Similarity, connector fit, grip movement, and purchase do not establish fit or
acceptance. Keep source provenance, specification, physical compatibility,
electrical compatibility, functional compatibility, safety suitability, and
acceptance separate.

## Navigation

[Component index](README.md) | [Documentation index](../INDEX.md) | [Component evaluation template](../templates/component-evaluation-template.md)
