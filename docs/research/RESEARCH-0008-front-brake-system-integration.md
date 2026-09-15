# RESEARCH-0008: Front brake system integration

**Purpose:** Define the evidence needed to evaluate the complete candidate front-brake system.

**Document status: Draft**

**Status: Unverified**

**Review: Technical Review Required**

## Research question

What evidence is required to establish whether the candidate MT-07 front master cylinder, R1 Blue Spot front calipers, XJ900S fork/discs/wheel, brake lines and associated service parts can form a hydraulically, mechanically, functionally and safely compatible front-brake system?

## Scope

Included: master-cylinder-to-caliper hydraulic relationship; master-cylinder bore and lever geometry; caliper piston configuration and effective hydraulic area; original XJ900S disc/fork/wheel interfaces; mounting geometry; disc diameter, thickness, offset and pad sweep; hose topology/routing; banjo geometry/orientation; sealing washers/faces; bleed orientation and trapped-air removal; steering, suspension, wheel/rim/spoke and fork clearance; reservoir orientation/operating range; switchgear/throttle/lever clearance; pad and repair-kit applicability; fluid compatibility; pressure retention, release and residual pressure; thermal/dynamic braking behavior; serviceability and inspection access.

Excluded: component-selection acceptance, released installation/service instructions, numerical acceptance limits, road-use approval, and import of Wemoto order details. No hydraulic or mechanical specification is inferred from a reported donor name or part number.

## Sources and current evidence

Repository records reviewed on 2026-09-15; this is not a purchase or measurement date.

| Source | Evidence and boundary |
| --- | --- |
| [COMP-0001](../components/COMP-0001-2022-mt07-front-brake-master-cylinder.md) | Acquired owner-reported 2022 Yamaha MT-07 master-cylinder and lever assembly; seller-reported `1XB-2580A-00-00`. Exact identity/application and specifications remain Unverified. |
| [COMP-0009](../components/COMP-0009-r1-blue-spot-front-brake-calipers.md) | Acquired owner/project-reported Yamaha R1 "Blue Spot" front caliper pair; reported right `5JJ-2580U-00-00`, left `5JJ-25880T-00-00`. Exact physical identity/application remain Unverified. |
| [Purchased/on-hand inventory](../components/PURCHASED-ON-HAND-INVENTORY.md) | Availability/provenance only. Two repair kits and EBC pads are reported acquired for COMP-0009; exact identification and applicability remain Unverified. No order details are imported here. |
| [System requirements](../requirements/system-requirements.md) and [test strategy](../testing/test-strategy.md) | Project safety, evidence and review obligations; not component specifications or test results. |

Both component records already record the intended pairing. The components are available for evaluation. Neither record establishes hydraulic compatibility, installed physical compatibility, or road readiness. No new measurements, authoritative donor specifications, completed tests or resolved identity conflicts are supplied by this research record.

## Evidence boundaries

| Evidence category | Current state and required distinction |
| --- | --- |
| Acquisition/availability | Owner/project-reported acquisition is recorded; it does not establish health, identity or suitability. |
| Component identity/specification | Unverified; retain physical markings, photographs and applicable authoritative Yamaha/manufacturer evidence. Seller/owner reports are not Yamaha-confirmed facts. |
| Physical compatibility | Unverified; requires measured installed interfaces and complete movement/clearance evidence. |
| Hydraulic compatibility | Unverified; requires supported inputs, documented analysis and technical review. |
| Functional compatibility | Unverified; requires pressure, release, residual-pressure and dynamic evidence for the exact configuration. |
| Safety suitability | Unverified; requires assessment of hazards, service condition, thermal behavior and applicable validation evidence. |
| Final acceptance | Not established; availability, a calculated ratio, apparent fit or initial operation cannot establish acceptance. |

Direct measurement records shall identify the object, datum, method, measuring equipment, date, units, raw readings and supporting photographs. Record missing metadata explicitly; do not invent uncertainty, tolerance or calibration status. Retain conflicts and source applicability limits for review.

## Hydraulic analysis

**Status: Unverified**

No ratio is calculated because the required inputs are not supported in the current records.

| Minimum input | Current evidence / required work |
| --- | --- |
| Exact master-cylinder piston diameter | Unknown; obtain applicable authoritative evidence or documented direct measurement. |
| Effective lever geometry / mechanical ratio | Unknown; establish geometry and the operating conditions relevant to the analysis. |
| Exact number and diameters of active caliper pistons | Unknown; identify and document each caliper's actual configuration. |
| Number of calipers | Two reported acquired; verify both physical units and the configuration used in the analysis. |
| Total effective caliper hydraulic area | Not calculated; define the area convention for the verified caliper design and document all included pistons/calipers. |
| Selected hose topology | Not selected; retain a circuit/routing drawing and exact proposed connections. |
| Comparison baseline | Original XJ900S or verified donor-system baseline not established here; retain applicability and equivalent calculation conventions if later obtained. |

Any future hydraulic ratio shall be labelled **derived engineering calculation**, not an OEM specification. State its definition, units, assumptions, source inputs and limitations. Technical review shall assess usable lever travel, master-cylinder bottoming risk, pressure/displacement relationship and the limitations of any baseline comparison. Do not define an acceptable ratio numerically without evidence and technical review. A ratio alone does not establish braking performance or safety.

## Mechanical interface verification matrix

All rows require evidence for the actual XJ900S fork/discs/wheel and candidate installed configuration. No dimensions or clearance limits are supplied here.

| Interface | Required verification/evidence | Initial status |
| --- | --- | --- |
| Caliper mounting-centre spacing | Direct measurements of caliper and fork mounting centres at defined datums. | Unverified |
| Mounting fastener/interface | Threads, fastener identity, seating faces, engagement and applicable service specifications. | Unverified |
| Axial caliper position | Caliper position relative to disc centre plane and mounting datums. | Unverified |
| Disc diameter | Actual disc identity and measured diameter with applicable source comparison. | Unverified |
| Disc thickness | Measured thickness and applicable disc/pad/caliper limits from retained evidence. | Unverified |
| Disc lateral offset | Measured disc plane relative to wheel/fork/caliper datums. | Unverified |
| Pad sweep | Actual friction-material sweep and disc contact relationship; check overhang, ledges and interference. | Unverified |
| Wheel clearance | Wheel/rim/spoke clearance where applicable, with wheel rotation and the reviewed operating envelope. | Unverified |
| Fork clearance | Caliper, disc and associated hardware relative to fork surfaces. | Unverified |
| Bleed-screw orientation | Installed bleed orientation and a service strategy capable of removing trapped air. | Unverified |
| Banjo clearance | Geometry/orientation, fastener interface and clearance to surrounding parts. | Unverified |
| Hose routing | Topology, length, supports and routing throughout movement; no tension, crushing or unsafe bends. | Unverified |
| Full left/right steering lock | Hoses, reservoir, lever, switchgear and throttle clearance at both locks and throughout steering movement. | Unverified |
| Full relevant suspension travel | Reviewed safe method covering relevant travel and combined steering positions; no contact or hose tension. | Unverified |
| Reservoir and controls | Orientation/operating range, lever travel/reach, pivot and switchgear/throttle relationship. | Unverified |
| Sealing and service access | Washers, sealing faces, banjo/bleeder access, inspection and later replacement access. | Unverified |

## Service parts, hydraulic function and thermal evidence

- Identify the two repair kits and EBC pads exactly; verify applicability, condition and installation requirements from retained authoritative evidence before use.
- Establish fluid specification and compatibility with the verified system parts, including seals and hoses; no fluid type is selected here.
- Define hose specification/topology, banjo geometry/orientation, sealing washers/faces and bleed strategy without assuming interchangeability.
- Define reviewed pressure-retention, leak, application, release and residual-pressure methods and criteria. Record lever behavior and wheel release separately from hydraulic-pressure evidence.
- Define later thermal and dynamic evaluation, including repeated braking, fade/degradation and post-test condition, only after static gates pass and a separate method is reviewed.
- Evaluate inspection access, bleeding access, hose replacement, pad service, fastener access and reproducible assembly. Installation or rebuilding alone is not validation.

## Failure modes and hazards

The following are hazards to assess, not observed failures. No probability or severity numbers are assigned.

| Failure mode / hazard | Evidence or control required before progression |
| --- | --- |
| Incorrect hydraulic matching; master-cylinder bottoming or insufficient usable lever travel | Supported hydraulic inputs/calculation, reviewed lever-travel assessment and later static functional evidence. |
| Hose or banjo interference; hose tension at full steering/suspension movement | Routing and combined movement/clearance records. |
| Leakage; incorrect sealing washers or sealing surfaces | Part/service-source verification, surface inspection and pressure-hold/leak evidence. |
| Trapped air | Reviewed bleed orientation/method and retained final bleed condition. |
| Incorrect pad/disc sweep; caliper/disc misalignment | Measured interface/alignment and sweep evidence before hydraulic testing. |
| Seized or dragging pistons; residual hydraulic pressure | Condition inspection, application/release and residual-pressure investigation under a reviewed method. |
| Inappropriate repair parts | Exact pad/kit identity and authoritative applicability evidence before assembly. |
| Loose fasteners | Verified fastener interfaces, torque sources/values and assembly/inspection records. |
| Reduced braking force; wheel lock or unintended brake application | Static gates, reviewed dynamic method, stop conditions and retained braking observations. |
| Brake fade / thermal degradation | Separately reviewed higher-load/thermal criteria and post-test inspections. |
| Loss of control | No dynamic progression with incomplete gates; controlled environment and separately reviewed recovery arrangements. |

## Conclusion and decision impact

The candidate system is suitable for continued controlled evaluation only. No component-selection acceptance or road-use approval is established. The pairing, hose arrangement, hydraulic ratio and installation remain Unverified.

Use [TEST-PLAN-0003](../testing/TEST-PLAN-0003-front-brake-system-validation.md) for staged validation planning. No new ADR is required merely to create this research record. A future accepted material brake-system/component decision may require a decision record, depending on repository practice and design significance.

## Traceability and next evidence

- Requirements: [SYS-006](../requirements/system-requirements.md#sys-006), [SAF-004](../requirements/system-requirements.md#saf-004), [SAF-005](../requirements/system-requirements.md#saf-005), [REL-002](../requirements/system-requirements.md#rel-002), [SRV-001](../requirements/system-requirements.md#srv-001), [SRV-002](../requirements/system-requirements.md#srv-002), [DEV-002](../requirements/system-requirements.md#dev-002), [DEV-003](../requirements/system-requirements.md#dev-003), [DEV-005](../requirements/system-requirements.md#dev-005), [DEV-007](../requirements/system-requirements.md#dev-007), [DEV-008](../requirements/system-requirements.md#dev-008), [DOC-002](../requirements/system-requirements.md#doc-002), [DOC-006](../requirements/system-requirements.md#doc-006), [DOC-008](../requirements/system-requirements.md#doc-008).
- Roadmap context: [Stage 2](../implementation/roadmap.md#stage-2--requirements-and-measurement-capture) and [Stage 8](../implementation/roadmap.md#stage-8--reliability-and-safety-validation); no roadmap gate is passed here.
- Next evidence: physical identities/condition, service-part applicability, supported hydraulic inputs, mechanical measurements, service sources, configuration drawing and technical review. All remain open.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-15 | Created system-level front-brake integration research. | Connect acquired candidates to explicit evidence needs without accepting the combination or authorizing road use. |

## Navigation

[Research index](README.md) | [Validation plan](../testing/TEST-PLAN-0003-front-brake-system-validation.md) | [Documentation index](../INDEX.md)
