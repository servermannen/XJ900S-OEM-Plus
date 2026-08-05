# COMP-0002: 2022 Yamaha MT-07 Clutch Lever and Perch

**Purpose:** Evaluate the acquired clutch lever and perch assembly as a
candidate component without establishing compatibility, acceptance, or
validation.

**Document status: Draft**

Identification, evidence, compatibility status, safety, and recommendation are
mandatory.

## Candidate identification

- Component: Clutch lever and perch assembly
- Manufacturer: Yamaha
- Source model: MT-07 — owner-provided identification; official Yamaha
  application not independently verified
- Model year or range: 2022 — owner-provided identification; official Yamaha
  application not independently verified
- OEM part number: Unknown
- Variant identifiers: Unknown
- Source or listing: Owner-provided purchase identification; original listing
  URL is not currently recorded in the repository
- Evaluation date: 2026-08-06

## Evaluation status

**Status: Unverified**

**Review: Technical Review Required**

## Intended function

The intended project function is operation of the XJ900S cable-operated
clutch. This intended use does not establish compatibility with the original
XJ900S clutch cable, cable nipple, adjuster, switchgear, handlebar, or clutch
release mechanism.

### Confirmed project-provenance information

- The owner identifies the acquired assembly as originating from a 2022 Yamaha
  MT-07.
- The project has acquired the assembly.
- The intended project function is operation of the XJ900S cable-operated
  clutch.

The owner-provided source-model identification records the project's
acquisition history. It is not independent Yamaha catalogue verification.

## Applicable requirements

- [SYS-003](../requirements/system-requirements.md#sys-003)
- [SYS-006](../requirements/system-requirements.md#sys-006)
- [SAF-005](../requirements/system-requirements.md#saf-005)
- [REL-002](../requirements/system-requirements.md#rel-002)
- [REL-004](../requirements/system-requirements.md#rel-004)
- [REL-006](../requirements/system-requirements.md#rel-006)
- [SRV-001](../requirements/system-requirements.md#srv-001)
- [SRV-002](../requirements/system-requirements.md#srv-002)
- [SRV-004](../requirements/system-requirements.md#srv-004)
- [SRV-006](../requirements/system-requirements.md#srv-006)
- [DEV-003](../requirements/system-requirements.md#dev-003)
- [DOC-002](../requirements/system-requirements.md#doc-002)
- [DOC-003](../requirements/system-requirements.md#doc-003)
- [DOC-006](../requirements/system-requirements.md#doc-006)
- [DOC-008](../requirements/system-requirements.md#doc-008)

## Known specifications

| Attribute | Value | Unit | Source | Status |
| --- | --- | --- | --- | --- |
| Owner-reported source model | MT-07 | Not applicable | Owner-provided identification | Confirmed |
| Owner-reported source model year | 2022 | Year | Owner-provided identification | Confirmed |
| OEM part number | Unknown | Not applicable | No authoritative documentation recorded | Unverified |
| Handlebar clamp specification | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Lever pivot and cable geometry | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Cable nipple dimensions | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Cable adjuster dimensions and thread | Unknown | Unknown | No authoritative documentation or documented direct measurement recorded | Unverified |
| Clutch-switch configuration | Unknown | Unknown | No authoritative documentation or documented inspection recorded | Unverified |

## Physical compatibility

- Dimensions: Unknown
- Mounting: Compatibility with the XJ900S handlebar and mounting arrangement is
  Unknown.
- Clearances: Lever reach, switchgear clearance, and full-steering-lock
  clearance are Unknown.
- Connectors and routing: Clutch-switch connection and clutch-cable routing are
  Unknown.
- Environmental suitability: Condition and suitability for the project
  environment have not been evaluated.
- Required modifications: Unknown

Placement on a handlebar, appearance, source model, or an apparent clamp fit
does not establish physical compatibility.

## Electrical or functional compatibility

- Supply and signals: Clutch-switch configuration and electrical interface
  requirements are Unknown.
- Inputs and outputs: Lever, cable, and clutch-release geometry and their
  functional relationship are Unknown.
- Communication and diagnostics: No communication or diagnostic interface is
  established by the current evidence.
- Control authority and failure behavior: The assembly is intended to operate
  the clutch cable; installed behavior, return action, and failure response have
  not been evaluated.
- Required interface hardware: Cable, adjuster, nipple, switch, or adaptation
  requirements are Unknown.

Connector appearance alone is not compatibility evidence.

## Integration assessment

### Benefits

- The acquired assembly is available for documented inspection, measurement,
  and bench evaluation.

### Risks and constraints

- The source-model identity and exact OEM part number lack independent Yamaha
  catalogue verification.
- Compatibility with the original XJ900S clutch cable, cable nipple, adjuster,
  switchgear, handlebar, and clutch release mechanism is Unknown.
- Incorrect lever or cable geometry, routing, clearance, free play, or return
  action could prevent complete clutch engagement or disengagement.
- Condition and wear have not been evaluated.

### Required adaptations

- Unknown; no adaptation is defined or approved by this record.

### Missing evidence

- Authoritative Yamaha identification and application evidence.
- Handlebar clamp, lever pivot, cable nipple seat, cable adjuster, and effective
  lever geometry measurements.
- Comparative XJ900S lever, perch, cable, and clutch-release requirements.
- Cable routing, clearance, travel, free-play, engagement, disengagement, return,
  clutch-drag, and clutch-slip evidence.
- Defined acceptance criteria and completed technical review.

## Safety assessment

This candidate would directly affect clutch control. Incorrect geometry,
routing, clearance, free play, condition, or return action could impair
controllability or prevent complete clutch engagement or disengagement. No
physical compatibility, functional compatibility, installation safety, road
readiness, or validation is established by this record.

Review: Technical Review Required

## Serviceability and availability

- Replaceability and availability: Unknown
- Documentation and connector availability: Official application,
  specification, parts-catalogue, and clutch-switch documentation have not been
  recorded.
- Long-term support and alternatives: Unknown

## Decision recommendation

**Recommendation: Bench evaluate**

**Rationale:** The acquired assembly can be inspected and measured, but its
identity, condition, dimensions, cable relationship, physical integration, and
functional safety remain unverified. Acquisition does not constitute component
acceptance.

Do not use `Accept` while material compatibility questions remain unresolved.

## Required validation

- Verify the exact Yamaha OEM part number and 2022 MT-07 application using an
  official Yamaha parts catalogue or other authoritative Yamaha documentation.
- Measure and document the handlebar clamp, lever pivot, cable nipple seat,
  cable adjuster, and effective lever geometry.
- Compare those measurements with the original XJ900S clutch lever, perch,
  cable, and release requirements.
- Verify cable routing through the full steering range without binding,
  stretching, sharp bends, or unintended clutch actuation.
- Verify switchgear clearance, lever reach, full lever travel, free play, full
  clutch disengagement, complete clutch engagement, and return action.
- Check for clutch drag and clutch slip under controlled conditions.
- Establish whether the original XJ900S cable can be used safely or whether a
  documented replacement or adaptation is required.
- Define acceptance criteria before road testing.
- Require stationary and controlled functional validation before road use.

## Traceability

- Related research: None recorded
- Related ADRs: None; no final component-selection decision is recorded
- Related tests: None recorded
- Roadmap stage: [Stage 2 — requirements and measurement
  capture](../implementation/roadmap.md#stage-2--requirements-and-measurement-capture);
  [Stage 8 — reliability and safety
  validation](../implementation/roadmap.md#stage-8--reliability-and-safety-validation);
  [Stage 9 — OEM+ refinement](../implementation/roadmap.md#stage-9--oem-refinement),
  only after technical validation

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-06 | Created initial component evaluation record. | Record the acquired candidate and unresolved evidence needs without accepting or validating it. |

## Guidance

Similarity and purchase do not establish fit or acceptance. Keep availability,
specification, physical/electrical compatibility, and acceptance separate.
Record exact variants and model years. Safety-critical candidates need review
and test evidence.

## Navigation

[Component index](README.md) | [Documentation index](../INDEX.md) | [Component evaluation template](../templates/component-evaluation-template.md)
