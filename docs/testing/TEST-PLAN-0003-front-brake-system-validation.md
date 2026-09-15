# TEST-PLAN-0003: Front brake system validation

**Document status: Draft**

**Execution status: Not started**

**Test result: Not available**

**Status: Unverified**

**Review: Technical Review Required**

## Purpose and scope

Define staged evidence and safety gates for the candidate front-brake system described in [RESEARCH-0008](../research/RESEARCH-0008-front-brake-system-integration.md): [COMP-0001 master cylinder and lever](../components/COMP-0001-2022-mt07-front-brake-master-cylinder.md), [COMP-0009 caliper pair and associated service parts](../components/COMP-0009-r1-blue-spot-front-brake-calipers.md), actual XJ900S fork/discs/wheel, hoses, banjos, seals and fluid.

No test has been executed. This plan does not authorize road use or establish component, combination, hydraulic-ratio, hose-arrangement or installation acceptance. Reported identities and acquired pads/repair kits retain the evidence classifications in the component records; no new specifications are established here.

## Gate rules and preparation

No gate has passed. Record each phase's execution status separately from its test result and progression decision. A completed activity is not automatically a passing result. Missing prerequisite evidence blocks dependent work.

Before each phase, identify the operator, reviewer, exact test object/configuration, applicable service sources, method, equipment, evidence storage and stop/recovery arrangements. Equipment identity, suitability and calibration information shall be recorded where relevant, not assumed. Define the safe motorcycle support and any wheel/suspension movement method before use. No disassembly or service operation proceeds without an applicable reviewed method.

Pressure, force, hold duration, clearance limits, torque values, fluid specification, target speeds, stopping distances and numerical pass limits are not defined by this plan. Establish applicable values from retained evidence and technical review before the activity that depends on them. Do not fill a missing value from donor appearance or unsupported general practice.

| Phase | Initial execution status | Initial test result | Progression gate |
| --- | --- | --- | --- |
| A — Identity and inspection | Not started | Not available | Identity/condition/service-part evidence reviewed before assembly. |
| B — Engineering review | Not started | Not available | Preliminary configuration and measurement needs may be defined before C; complete technical review using C evidence before B passes. |
| C — Dry fit and clearance | Not started | Not available | A must pass; reviewed safe dry-fit method and preliminary B review define the work. C supplies physical evidence to complete B; B need not have passed to begin C. |
| D — Hydraulic assembly/bleeding | Blocked | Not available | A passes, both B and C pass, and service method and specifications are defined. |
| E — Static hydraulic checks | Blocked | Not available | D passes; static test load/duration/criteria and method reviewed. |
| F — Low-speed dynamic braking | Blocked | Not available | A–E pass, evidence retained and technical review authorizes progression. |
| G — Higher-load / road-use validation | Blocked | Not available | F passes; separate technical review, scope and acceptance criteria defined. |

### Phase A — Identity and component inspection

**Execution status: Not started**

Before assembly, retain exact physical identification where possible, literal markings and photographs. If exact identity cannot be established, record the limitation for technical review; do not infer donor application or service-part applicability.

Inspect and record:

- Master-cylinder body/condition, lever and pivot condition.
- Reservoir, diaphragm and cap; threads and sealing surfaces.
- Caliper body condition; pistons, bores, seals, bleed screws and threads, using the applicable service method for internal inspection.
- Pad identity/condition and both repair kits' exact identity, contents and applicability.

Gate A: required identity, condition and applicability evidence is retained and reviewed. Unresolved defects or service-part applicability block assembly; purchase and visual appearance are insufficient.

### Phase B — Engineering compatibility review

**Execution status: Not started**

Phase B may begin before Phase C to establish the preliminary engineering configuration, required measurements and reviewed safe dry-fit scope. This preliminary review does not pass Gate B or authorize hydraulic assembly or pressurization. Phase C may generate the physical fit, alignment, sweep, routing and clearance evidence needed to complete Phase B.

To complete Phase B before hydraulic installation require:

- Verified master-cylinder bore evidence and effective lever geometry where required.
- Verified active caliper piston counts/diameters and number of calipers.
- Documented hydraulic calculation, with effective-area convention, inputs, assumptions and baseline applicability recorded as a derived engineering calculation.
- Mechanical interface measurements and disc/pad-sweep assessment from the research matrix.
- Defined hose topology/routing, banjo design/orientation, sealing interfaces and bleed strategy.
- Fluid specification from authoritative evidence applicable to the verified system parts.
- Technical review of the proposed configuration and the methods/criteria for dependent work.

Gate B: the engineering reviewer assesses all required evidence, including evidence returned from Phase C, and records whether the proposed configuration meets the reviewed engineering criteria. Preliminary review alone cannot pass Gate B. Both B and C must pass before Phase D begins. If these matters are unresolved, hydraulic installation and later powered/dynamic phases remain Blocked. No numerical acceptable hydraulic ratio is set here.

### Phase C — Dry physical fit and clearance

**Execution status: Not started**

Phase A must pass before controlled dry-fit work. Use the reviewed safe dry-fit method and preliminary configuration/measurement scope defined in Phase B; completed Gate B approval is not a prerequisite for this evidence-gathering work. Return all physical fit, alignment, sweep, routing and clearance evidence generated in Phase C to the engineering review to complete Phase B. Both B and C must pass before Phase D hydraulic assembly and bleeding may begin. Phase C does not establish hydraulic compatibility or authorize pressurization; physical fit alone supplies no hydraulic-pressure or braking-performance evidence.

Verify and retain caliper mounting, fastener engagement, disc centring/alignment, pad sweep, wheel/rim/spoke and fork clearance where applicable, banjo clearance, hose routing, reservoir orientation/operating range and lever/switchgear/throttle clearance. Cover full left/right steering lock and full relevant suspension movement, including combined positions under the reviewed safe method.

No contact, tension, crushing, sharp bends or unsafe routing is permitted. Define evidence-backed clearance criteria before execution; do not invent numerical limits. Record measured datums, movement range and limitations. An incomplete movement envelope cannot pass this gate.

Gate C: retained dry-fit/clearance evidence meets the reviewed criteria; unresolved contact, alignment, sweep, engagement or routing issues block D.

### Phase D — Hydraulic assembly and bleeding

**Execution status: Blocked**

Only after A–C pass and the applicable service method is defined, record the exact installed parts/configuration, fluid and its source/specification, hoses, banjos, sealing washers, sealing surfaces, torque sources and values, bleed method and final bleed condition. Verify bleed orientation and the ability to remove trapped air using that method.

No torque value, fluid specification, hose specification or washer interchangeability is inferred here. Undefined service specifications block execution.

Gate D: assembly and bleeding records are complete and meet the reviewed method; final bleed condition and configuration are reviewed for static testing. Successful bleeding is not full validation.

### Phase E — Static pressure, leak, release and residual-pressure checks

**Execution status: Blocked**

Keep the motorcycle stationary and secured. Before execution, separately define and technically review the pressure-hold duration/load, equipment, repetition, release/drag assessment method and numerical criteria where required. No pressure, force, duration or numerical pass limit is invented by this plan.

Require and record:

- Repeated lever applications and a sustained pressure-hold test using the reviewed duration/load.
- Inspection of every sealing point; stable lever behavior and usable travel without bottoming.
- Correct piston application and complete release.
- Free wheel rotation after release and no residual drag attributable to trapped hydraulic pressure, assessed by the reviewed method.
- No leaks, hose movement, component contact or abnormal deformation.

Unexplained drag or lever behavior requires investigation; wheel rotation alone does not quantify residual pressure. Do not improvise a pressurized-system intervention to diagnose a failure.

Gate E: all static evidence meets the reviewed criteria, with no unresolved anomaly; retain pressure-hold, leak, release and residual-pressure records for technical review before F.

### Phase F — Controlled low-speed dynamic braking

**Execution status: Blocked**

Unblock only after A–E pass, evidence is retained and technical review explicitly authorizes progression for the exact configuration. Define the operator, protective arrangements, test area, recovery method, conditions, stop criteria and evidence-backed speed/application progression before execution.

Use a controlled closed/private test environment, low initial speed, progressive brake application and repeated post-stop inspections. No public-road validation is included at this stage. Do not invent target speeds or stopping distances. Stop for any listed anomaly; a completed stop does not establish full validation.

Gate F: the defined controlled scope passes and its observations, anomalies and inspections receive technical review before G is considered.

### Phase G — Higher-load / road-use validation

**Execution status: Blocked**

Requires separate technical review and defined acceptance criteria before use. Define higher-load, repeated-braking and thermal evaluation, fade/degradation observations, dynamic conditions, post-test inspections and any road-use prerequisites in that separate reviewed scope. This plan grants no road-use approval.

Successful installation, successful bleeding, one stop or a brief ride shall not constitute full validation. Any later acceptance decision must state the exact configuration, tested scope, evidence and remaining limitations.

## Safe state, stop conditions and recovery

Default safe state: motorcycle stationary and secured; no dynamic testing when evidence gates are incomplete; brake system not considered road-ready.

Stop testing immediately on leakage, changing lever feel, abnormal drag, interference, hose movement, component movement, unusual heat, noise, misalignment, unexpected wheel lock or any unexplained behavior. Dynamic phases require a separately reviewed stopping/recovery method; do not assume the suspect brake remains available for recovery.

After stopping, secure the motorcycle using the reviewed method, prevent further dynamic use, retain the configuration and evidence, document the anomaly and investigate its cause. Resume only after corrective work, affected earlier checks and the revised method receive technical review. Do not bypass a failed gate or erase failed observations.

## Required test records and result classification

Retain, for each phase and configuration:

- Exact component identities, installed configuration and revision/change history.
- Measurements, calculations, datums, equipment/method metadata and photographs.
- Torque sources/values when established; fluid source/specification; hose, banjo, washer and service-part identities.
- Bleed record, pressure-hold record, release/drag and residual-pressure record, and clearance record.
- Dynamic-test configuration and conditions, operator, date/time and post-stop inspections when later executed.
- Anomalies, deviations, corrective work, repeated checks and raw evidence references.
- Execution status, separate result classification, reviewer and progression decision with scope/limitations.

Use [test-strategy result classifications](test-strategy.md#test-result-classification) for executed evidence. A missing or blocked activity has no passing result. The current overall execution status remains Not started and the test result remains Not available; no result classification is assigned as if execution had occurred.

## Traceability

- Research and evidence needs: [RESEARCH-0008](../research/RESEARCH-0008-front-brake-system-integration.md).
- Requirements: [SAF-004](../requirements/system-requirements.md#saf-004), [SAF-005](../requirements/system-requirements.md#saf-005), [REL-002](../requirements/system-requirements.md#rel-002), [SRV-001](../requirements/system-requirements.md#srv-001), [SRV-002](../requirements/system-requirements.md#srv-002), [DEV-002](../requirements/system-requirements.md#dev-002), [DEV-003](../requirements/system-requirements.md#dev-003), [DEV-005](../requirements/system-requirements.md#dev-005), [DEV-006](../requirements/system-requirements.md#dev-006), [DEV-007](../requirements/system-requirements.md#dev-007), [DEV-008](../requirements/system-requirements.md#dev-008).
- Roadmap context: [Stage 2](../implementation/roadmap.md#stage-2--requirements-and-measurement-capture) and [Stage 8](../implementation/roadmap.md#stage-8--reliability-and-safety-validation); no stage is completed by creating this plan.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-15 | Created staged front-brake validation plan; no execution or results. | Define evidence gates, safe states and review requirements before dynamic progression. |

## Navigation

[Testing index](README.md) | [Test strategy](test-strategy.md) | [Research record](../research/RESEARCH-0008-front-brake-system-integration.md) | [Documentation index](../INDEX.md)
