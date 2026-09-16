# RESEARCH-0009: Smart ignition coil candidate evaluation

**Purpose:** Record evidence gaps and comparison criteria for production
smart-ignition-coil candidates for XJ900S Level 1 ignition with Super uaEFI.

**Document status: Draft**

Status: Unverified

Review: Technical Review Required

## Research question

Which production smart ignition-coil candidates could satisfy the XJ900S
Level-1 ignition requirements with Super uaEFI while preserving safe electrical
drive, serviceability, physical packaging and future sequential-ignition
support?

## Scope

### Included

- Candidate comparison for four production smart-coil families:
  - GM LS2 / LS3-style remote smart coil;
  - GM D585 truck smart coil;
  - VAG / Audi `06E 905 115 E/G` family direct COP;
  - Toyota / Denso `90919-02240` direct COP.
- Electrical, physical, serviceability, and evidence fields that must be
  established before any candidate can be connected to the project ECU.
- Safety boundaries for dwell, trigger behavior, current, grounding,
  protection, and packaging.
- Next evidence-producing actions needed before narrowing the candidate set.

### Excluded

- Selection, acceptance, road approval, or purchase recommendation for any
  ignition coil.
- Final ignition architecture, dwell settings, coil-current limits, connector
  pinouts, harness design, bracket design, or calibration values.
- COMP records for candidate coils.
- Bench-test procedure creation or authorization to energize any coil.
- Changes to architecture, ADRs, system requirements, component inventory, or
  test plans.

## Current status

**Status: Unverified**

**Review: Technical Review Required**

Ignition remains a Level 1 safety-critical function. This record does not make
any candidate selected, accepted, electrically compatible, physically
compatible, or road-approved.

[RESEARCH-0007](RESEARCH-0007-super-uaefi-stage1-hardware-feasibility.md)
records that the pinned Super uaEFI schematic implements the relevant ignition
outputs as logic-level/smart-coil outputs by default, with an onboard IGBT
population option. This hardware default does not select the project's final
ignition architecture or a smart-coil candidate. The exact delivered Super
uaEFI hardware revision, onboard IGBT population, final ignition architecture,
and exact coil choice remain unresolved. No proposed smart-coil architecture
is accepted by this record.

## Sources

| Source | Type | Date accessed | Relevance | Reliability notes |
| --- | --- | --- | --- | --- |
| [RESEARCH-0002: Level 1 I/O and trigger requirements](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | Project research | 2026-09-16 | Defines the requirement for four ignition commands and preserves logic-level versus power-driving as coil/module-dependent. | Project requirement-planning record; does not select coils. |
| [RESEARCH-0007: Super uaEFI Stage 1 hardware feasibility](RESEARCH-0007-super-uaefi-stage1-hardware-feasibility.md) | Project research | 2026-09-16 | Records B2/B3 Stage 1 ignition commands, default logic/smart-coil direction, onboard IGBT option, and HG-05 ignition-driver gate. | Static allocation only; delivered ECU revision and driver population remain Unverified. |
| [System architecture](../architecture/system-architecture.md) | Project architecture | 2026-09-16 | Keeps fuel, ignition, engine authority, and safety-critical behavior inside Level 1. | Does not select an ignition component. |
| [System requirements](../requirements/system-requirements.md) | Project requirements | 2026-09-16 | Defines safety, serviceability, electrical protection, documentation, and validation requirements applicable to ignition. | Requirement record only; implementation evidence remains required. |
| [TEST-PLAN-0002: Trigger decoder and timing validation](../testing/TEST-PLAN-0002-trigger-decoder-and-timing-validation.md) | Project test plan | 2026-09-16 | Requires identified ECU configuration, safe output disablement, reviewed live-ignition method, and fixed-timing validation before running ignition work. | Future plan; no coil testing has been executed. |
| Project research/discussion candidate set retained in this record | Project discussion input | 2026-09-16 | Preserves the four candidate families to evaluate. | Not authoritative electrical, pinout, physical, or application evidence. |

## Candidate comparison matrix

All candidate data below is deliberately evidence-bounded. Where authoritative
OEM or manufacturer evidence has not been retained in the repository, the
field remains `Unknown` or `Unverified`. Aftermarket cross-reference pages,
marketplace listings, and repeated internet claims are not treated as
authoritative electrical specifications.

| Dimension | GM LS2 / LS3-style remote smart coil | GM D585 truck smart coil | VAG / Audi `06E 905 115 E/G` family direct COP | Toyota / Denso `90919-02240` direct COP |
| --- | --- | --- | --- | --- |
| Candidate name/family | GM LS2 / LS3-style remote smart coil | GM D585 truck smart coil | VAG / Audi direct COP family | Toyota / Denso direct COP family |
| Exact known part number / family identifier | LS2 / LS3-style family; exact OEM part number Unknown | D585 family; exact OEM part number Unknown | `06E 905 115 E/G` family identifier; suffix interchangeability Unverified | `90919-02240` family identifier; exact manufacturer details Unverified |
| Original application | Unverified | Unverified | Unverified | Unverified |
| Coil architecture | Project candidate classification: remote coil with HT lead; authoritative candidate-specific confirmation not yet retained | Project candidate classification: remote coil with HT lead; authoritative candidate-specific confirmation not yet retained | Project candidate classification: direct COP; authoritative exact-family / suffix confirmation not yet retained | Project candidate classification: direct COP; authoritative candidate-specific confirmation not yet retained |
| Internal igniter | Unverified; candidate is discussed as smart-coil family only | Unverified; candidate is discussed as smart-coil family only | Not established by retained authoritative evidence | Not established by retained authoritative evidence |
| Trigger input voltage level | Unknown | Unknown | Unknown | Unknown |
| Trigger polarity | Unknown | Unknown | Unknown | Unknown |
| Dwell requirement / dwell curve | Unknown; common approximate GM-style figures are Unverified | Unknown; common approximate GM-style figures are Unverified | Unknown | Unknown |
| Maximum or typical primary current | Unknown | Unknown | Unknown | Unknown |
| Logic input current/load | Unknown | Unknown | Unknown | Unknown |
| Supply-voltage range | Unknown | Unknown | Unknown | Unknown |
| Ground architecture | Unknown; logic ground, power ground, shared/separate relationship requires authoritative evidence | Unknown; logic ground, power ground, shared/separate relationship requires authoritative evidence | Unknown; logic ground, power ground, shared/separate relationship requires authoritative evidence | Unknown; logic ground, power ground, shared/separate relationship requires authoritative evidence |
| Connector housing | Unknown | Unknown | Unknown | Unknown |
| Terminal family | Unknown | Unknown | Unknown | Unknown |
| Pin count | Unknown | Unknown | Unknown | Unknown |
| Authoritative pinout | Unknown | Unknown | Unknown | Unknown |
| Suppression / internal protection | Unknown | Unknown | Unknown | Unknown |
| Physical dimensions | Unknown | Unknown | Unknown | Unknown |
| Spark-plug terminal/boot arrangement | Requires separate HT lead and boot evidence; XJ plug-terminal relationship Unverified | Requires separate HT lead and boot evidence; XJ plug-terminal relationship Unverified | Unknown; direct relationship to XJ plug terminal Unverified | Unknown; direct relationship to XJ plug terminal Unverified |
| Thermal mounting requirements | Unknown; bracket, heat path, and vibration exposure require evidence | Unknown; bracket, heat path, and vibration exposure require evidence | Unknown; head and plug-well thermal exposure require evidence | Unknown; head and plug-well thermal exposure require evidence |
| Service availability | Unverified | Unverified | Unverified | Unverified |
| Evidence quality | Candidate family retained from project discussion; insufficient authoritative evidence | Candidate family retained from project discussion; insufficient authoritative evidence | Candidate family retained from project discussion; insufficient authoritative evidence | Candidate family retained from project discussion; insufficient authoritative evidence |
| XJ900S physical compatibility status | Unverified; remote layout may reduce dependence on plug-well dimensions but still requires mounting and HT-lead evidence | Unverified; remote layout may reduce dependence on plug-well dimensions but still requires mounting and HT-lead evidence | Unverified; depends on actual XJ900S plug-well and cylinder-head geometry | Unverified; depends on actual XJ900S plug-well and cylinder-head geometry |
| uaEFI electrical compatibility status | Unverified; actual output architecture and coil input architecture must both be established | Unverified; actual output architecture and coil input architecture must both be established | Unverified; actual output architecture and coil input architecture must both be established | Unverified; actual output architecture and coil input architecture must both be established |
| Outstanding evidence | Exact part number, application, input thresholds, polarity, dwell/current data, grounds, connector, pinout, protection, dimensions, thermal requirements, service data, XJ mounting and HT-lead path | Exact part number, application, input thresholds, polarity, dwell/current data, grounds, connector, pinout, protection, dimensions, thermal requirements, service data, XJ mounting and HT-lead path | Authoritative suffix interchangeability, application, input thresholds, polarity, dwell/current data, grounds, connector, pinout, protection, dimensions, boot geometry, service data, XJ plug-well fit | Authoritative application, input thresholds, polarity, dwell/current data, grounds, connector, pinout, protection, dimensions, boot geometry, service data, XJ plug-well fit |

## Physical integration distinction

### Remote-coil candidates

Status: Unverified

The GM LS2 / LS3-style and GM D585 candidates are project-classified as
remote-coil plus HT-lead candidates pending authoritative candidate-specific
confirmation. If that classification is verified, the architecture may reduce
dependence on XJ900S spark-plug well dimensions compared with direct COP
candidates, but it does not prove fitment.

Required physical evidence before any remote candidate can progress:

- mounting location;
- bracket concept and attachment evidence;
- HT lead length;
- plug-terminal compatibility;
- insulation and boot suitability;
- heat and vibration exposure;
- routing and service access;
- coil-body clearance and connector clearance;
- strain relief and water/debris exposure.

The XJ900S spark-plug terminal arrangement remains a project concern. Preserve
the current working concern that the XJ900S uses an M4-style spark-plug
terminal arrangement unless authoritative current project evidence establishes
a more exact description. Compatibility shall not be inferred from visual
similarity.

### Direct-COP candidates

Status: Unverified

The VAG / Audi `06E 905 115 E/G` and Toyota / Denso `90919-02240` candidates
are project-classified as direct COP candidates pending authoritative
exact-family, suffix, or candidate-specific confirmation. If that
classification is verified, direct-COP suitability depends on actual XJ900S
plug-well and cylinder-head geometry. No direct fit is claimed.

Required XJ900S measurements and evidence include at least:

- plug-well or access diameter;
- usable depth;
- spark-plug terminal height;
- coil-body OD envelope;
- boot OD and length;
- head-cover interference;
- electrical connector clearance;
- removal and service clearance;
- installed heat exposure;
- sealing and contamination behavior.

The same M4-style spark-plug terminal concern applies. Compatibility shall not
be inferred from visual similarity or from another engine's application list.

## Super uaEFI electrical compatibility gate

Status: Unverified

Review: Technical Review Required

Before any candidate coil is connected, the project must establish both the
actual Super uaEFI output architecture and the candidate coil input
architecture. No bench connection is authorized until both sides are verified.
The phrase `5 V trigger` alone is not proof of electrical compatibility.

Minimum required Super uaEFI evidence:

- exact PCB and hardware revision of the delivered unit;
- whether the relevant ignition outputs are logic-level or IGBT/high-current
  outputs for the actual delivered unit;
- output high and low voltage characteristics;
- permitted source and sink current;
- required pull-up or pull-down behavior;
- boot and default output state;
- polarity and inversion behavior;
- power-up and power-down behavior;
- fault handling;
- output protection;
- exact ignition output pins;
- effect of onboard IGBT population options;
- safe no-spark state.

Minimum required coil-side evidence:

- trigger input thresholds;
- trigger input load and current;
- correct ground relationship;
- coil supply protection and fusing;
- dwell-current behavior;
- thermal behavior;
- internal igniter architecture;
- input polarity;
- behavior for open and shorted trigger wiring;
- documented pinout and connector terminal family.

The safe state for ignition faults is no unintended spark and ignition energy
removed where a fault requires shutdown.

## Dwell and coil-current evidence

Status: Unverified

Review: Technical Review Required

Dwell and current evidence must remain separated by evidence class:

| Evidence class | Use in this record | Acceptance boundary |
| --- | --- | --- |
| OEM or manufacturer dwell data | Preferred source for candidate-specific dwell, input, current, thermal, and grounding behavior. | Required before final settings can be considered. |
| Third-party bench data | May identify useful questions and approximate behavior if method, hardware, and limitations are retained. | Does not become Confirmed without adequate method review and applicability analysis. |
| Forum or community data | May show recurring claims or known problem areas. | Not sufficient for final settings, compatibility, or safety claims. |
| Unsupported repeated claims | Recorded only as unsupported claims if relevant. | Must not be promoted to project fact. |

Known project working figures, such as approximately 3.5 ms sometimes cited
for GM-style coils, remain Unverified unless supported by authoritative
candidate-specific evidence or by a reviewed project bench method. This record
does not define final dwell settings.

Required future validation shall include current/dwell characterization using
a safe reviewed bench method before engine use. That future method must define
current limitation, fire protection, output disablement, heat monitoring,
instrumentation, stop conditions, and evidence retention before any coil is
energized.

## Failure modes and safety concerns

Review: Technical Review Required

The following failure modes must be considered before any candidate progresses:

- output-stage damage from incorrect coil architecture;
- excessive dwell or coil overheating;
- excessive primary current;
- insufficient dwell or weak spark;
- wrong trigger polarity;
- unintended spark during boot, reset, or power-down;
- ground offset;
- logic-ground current contamination;
- open or shorted trigger wire;
- open or shorted coil primary;
- connector mis-pin;
- power-feed fault;
- thermal overload;
- EMI or noise coupling into crank/cam inputs;
- HT insulation breakdown;
- plug or boot disconnection;
- bracket or coil loosening;
- fire risk from electrical fault.

No probability or severity scoring is assigned in this record.

## Candidate assessment

Status: Unverified

The evidence is insufficient to rank or select a candidate.

Remote GM-style coils may simplify physical packaging and service access
because they do not require the coil body to fit inside the plug-well envelope,
but they require separate HT leads, mounting brackets, heat and vibration
evidence, and plug-terminal compatibility.

Direct COP candidates may reduce HT-lead count and could support a compact
future sequential-ignition layout, but they demand much tighter physical
compatibility evidence at the XJ cylinder head, plug wells, boots, and
electrical connector clearance.

Exact electrical architecture must be proven for every candidate. No candidate
has enough retained evidence for acceptance.

## Evidence required before narrowing the candidate set

1. Verify the exact delivered Super uaEFI hardware revision and ignition-output
   hardware population.
2. Obtain authoritative datasheets or service documentation for each
   candidate's pinout, input architecture, dwell, current, grounding, and
   connector.
3. Obtain or directly measure XJ900S plug-well and spark-plug-access geometry.
4. Narrow the candidate set only after the same evidence fields are available
   for each candidate.
5. Define a technically reviewed bench test before energizing any coil.

This record does not create that bench test plan.

## Measurements

| Item | Value | Unit | Method | Source | Status |
| --- | --- | --- | --- | --- | --- |
| XJ900S plug-well / access diameter | Unknown | Unknown | Not measured in this record | Not available | Unverified |
| XJ900S usable plug-well depth | Unknown | Unknown | Not measured in this record | Not available | Unverified |
| XJ900S spark-plug terminal height | Unknown | Unknown | Not measured in this record | Not available | Unverified |
| Candidate coil dimensions | Unknown | Unknown | Not measured in this record | Not available | Unverified |
| Candidate boot OD and length | Unknown | Unknown | Not measured in this record | Not available | Unverified |
| Candidate trigger input threshold | Unknown | Unknown | Not measured in this record | Not available | Unverified |
| Candidate dwell-current behavior | Unknown | Unknown | Not measured in this record | Not available | Unverified |

## Decision impact

- Related requirements: SYS-008, SYS-009, SAF-003, SAF-004, SAF-006,
  SAF-007, REL-002, REL-006, SRV-002, SRV-003, SRV-004, ARC-001, ARC-007,
  ARC-008, DEV-002, DEV-003, DEV-008, DOC-002, DOC-003, DOC-006, DOC-008.
- Related research: [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md),
  [RESEARCH-0007](RESEARCH-0007-super-uaefi-stage1-hardware-feasibility.md).
- Related test planning: [TEST-PLAN-0002](../testing/TEST-PLAN-0002-trigger-decoder-and-timing-validation.md).
- Related components: None. Do not create COMP records for these coils until
  a later task explicitly selects a component record scope.
- ADR required: No ADR is created by this research record. A later ignition
  architecture selection may require a decision record.
- Recommended next action: produce the missing ECU hardware-revision,
  candidate-coil authoritative-documentation, and XJ900S physical-measurement
  evidence before defining any coil bench test.

## Conclusion

The retained evidence is insufficient for acceptance of any smart ignition
coil candidate. The next evidence-producing action is to verify the exact
delivered Super uaEFI hardware revision and ignition-output population, then
collect authoritative candidate-coil documentation and direct XJ900S packaging
measurements before any candidate is narrowed or energized.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-16 | Created smart ignition-coil candidate evaluation record. | Preserve the Level 1 ignition candidate set and safety/evidence gates without selecting a coil. |

## Navigation

[Research index](README.md) | [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [RESEARCH-0007](RESEARCH-0007-super-uaefi-stage1-hardware-feasibility.md) | [TEST-PLAN-0002](../testing/TEST-PLAN-0002-trigger-decoder-and-timing-validation.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Documentation index](../INDEX.md)
