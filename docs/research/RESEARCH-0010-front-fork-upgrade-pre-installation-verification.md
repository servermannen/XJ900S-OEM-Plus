# RESEARCH-0010: XJ900S front-fork upgrade and pre-installation verification

**Purpose:** Document the current front-fork upgrade intent, on-hand parts,
evidence gaps, measurement requirements, modification gates, brake-system
interaction, and validation gates required before installation or road use.

**Document status: Draft**

**Status: Unverified**

**Review: Technical Review Required**

## Research question

What evidence is required before the owner-reported on-hand YSS fork caps, YSS
PD Fork Valves, YSS fork springs, Wemoto Slinky Glide fork repair kit, and
front-fork damper-bolt sealing washers can be considered for installation in
the 1997 Yamaha XJ900S front fork without assuming compatibility or authorizing
permanent fork modification?

## Scope

### Included

- Front-fork upgrade intent and pre-installation evidence requirements.
- Owner-reported/on-hand YSS and Wemoto fork-related parts.
- Direct dimensional inspection requirements before assembly.
- Non-destructive dry-stack and fit-check requirements.
- Explicit modification gate for damper rods, fork caps, springs, spacers, and
  related fork components.
- Interaction with the front-brake upgrade documented in
  [RESEARCH-0008](RESEARCH-0008-front-brake-system-integration.md) and
  [TEST-PLAN-0003](../testing/TEST-PLAN-0003-front-brake-system-validation.md).
- Validation stages required before any road use is considered.

### Excluded

- Acceptance of any fork component, stack, spring rate, damping setting, oil
  specification, oil level, or installed configuration.
- Authorization for drilling, enlarging, welding, machining, shortening,
  spacer fabrication, spring cutting, fork-cap modification, or permanent
  damper-rod modification.
- Creation of separate component records for each YSS part.
- Use of specifications from another Yamaha model.

## Current status

The front-fork upgrade remains a pre-installation research and evidence gate.
No component compatibility, service specification, damping setup, installation
configuration, modification, test result, or road-use approval is established
by this record.

**Status: Unverified**

**Review: Technical Review Required**

## Sources and current evidence

Repository records reviewed on 2026-09-16. This is not a purchase, measurement,
installation, or test date.

| Source | Type | Relevance | Evidence boundary |
| --- | --- | --- | --- |
| [Purchased / on-hand component inventory](../components/PURCHASED-ON-HAND-INVENTORY.md) | Project inventory | Records acquisition/on-hand context for fork-related parts. | Availability record only; not compatibility or acceptance evidence. |
| [RESEARCH-0008](RESEARCH-0008-front-brake-system-integration.md) | Project research | Defines front-brake integration evidence needs involving the actual XJ900S fork, wheel, discs, hoses, and suspension movement. | Brake-system evidence gate only; does not validate fork upgrade components. |
| [TEST-PLAN-0003](../testing/TEST-PLAN-0003-front-brake-system-validation.md) | Project test plan | Defines staged front-brake validation and movement/clearance checks. | Not executed; does not authorize road use. |
| [System requirements](../requirements/system-requirements.md) | Project requirements | Defines safety, staged validation, documentation, and technical-review obligations. | Requirements and process basis only; not fork specification data. |

## On-hand parts and evidence boundary

The following entries preserve only owner-reported or directly observed project
evidence. Delivered/on-hand status is not compatibility, safety suitability, or
acceptance evidence.

| Item | Current retained evidence | Current status |
| --- | --- | --- |
| YSS fork cap | Marking/model `FCM38-41-001-50`; marking `M38x1.0`; marking `tube 41 mm`; delivered / physically on hand. | Unverified; no XJ900S fit or thread compatibility established. |
| YSS PD Fork Valve | Marking/model `PD335-D`; delivered / physically on hand. | Unverified; no XJ900S fit, valve size, seating, oil, setting, or damper-rod modification requirement established. |
| YSS fork spring pair | Delivered / physically on hand. Exact spring part number, rate, free length, and application are Unknown. | Unverified; no XJ900S fit, spring rate, preload, travel, or coil-bind suitability established. |
| Wemoto Slinky Glide front-fork repair kit | Supplied/order part number `PKAA9870`; delivered / on hand. | Unverified; exact contents, seal/bushing dimensions, application, and fit remain Unverified. |
| Wemoto copper sealing washers for front-fork damper retaining bolts | Supplied/order part number `AB7343`; quantity ordered 2; delivered / on hand. | Unverified; dimensions, material specification, sealing interface, and application remain Unverified. |

## Evidence classification rules

- Yamaha manual confirmed values shall be identified separately from owner
  measurements, vendor claims, YSS markings, and engineering assumptions.
- If exact XJ900S fork specifications are not retained in repository evidence,
  record them as evidence gaps rather than filling them from memory.
- Do not treat YSS markings `FCM38-41-001-50`, `M38x1.0`, or `tube 41 mm` as
  proof that the cap fits the XJ900S fork.
- Do not infer suitability of the spring pair from diameter, apparent fit, or
  delivered status.
- Do not infer PD335-D suitability from physical seating, valve appearance, or
  generic emulator-type installation practice.
- Do not infer Wemoto `PKAA9870` or `AB7343` applicability from ordering under
  a vehicle selection.

## Required XJ900S baseline evidence

The exact XJ900S fork variant and specifications remain evidence gaps unless
separately retained from an authoritative XJ900S source or direct measurement.
Do not use specifications from another Yamaha model.

Require verification and recorded evidence for at least:

- Exact XJ900S fork variant and year applicability.
- Stanchion/tube nominal diameter.
- Original fork-cap thread major diameter, pitch, thread form, and usable
  thread engagement.
- Original fork-cap shoulder and sealing arrangement.
- Original fork-cap O-ring or other sealing method.
- Original spring outside diameter.
- Original spring inside diameter where relevant.
- Original spring free length.
- Installed spring/preload stack.
- Spacer dimensions.
- Washer dimensions.
- Damper-rod outside diameter and inside diameter where relevant.
- Damper-rod top-seat geometry.
- PD-valve seating diameter.
- PD-valve centering and support.
- Available axial stack height.
- Available fork-cap thread engagement after any stack-height change.
- Full-compression clearance.
- Top-out clearance.
- Fork oil level / air-gap measurement method.
- Existing damper-rod compression-hole count, diameter, and location.
- Rebound path and orifice arrangement.
- Bottom retaining-bolt and copper-washer interface.
- Seal and bushing dimensions where replacement parts are considered.

## Fork-cap verification gate

Treat `FCM38-41-001-50`, `M38x1.0`, and `tube 41 mm` as markings or claimed
geometry only. Do not conclude the cap fits the XJ900S fork until direct
comparison against the actual XJ fork cap and fork tube is recorded and
technically reviewed.

Require direct comparison of:

- Thread outside diameter.
- Thread pitch.
- Thread engagement length.
- Shoulder geometry.
- Sealing interface.
- O-ring groove or sealing method.
- Cap underside geometry.
- Spring/preload interface.
- Wrench/tool clearance.
- Installed height.
- Steering and handlebar clearance.
- Full fork extension/compression effects where relevant.

A cap threading in by hand is not sufficient acceptance evidence.

## Spring verification gate

Before considering the YSS spring pair for assembly, require:

- Exact part number from retained label evidence.
- Spring rate from authoritative evidence.
- Free length.
- Outside diameter.
- Inside diameter where relevant.
- End treatment.
- Progressive versus linear identification.
- Pair matching.
- Manufacturer application data.
- Installed preload calculation.
- Available travel and coil-bind margin.
- Compatibility with the PD valve and cap stack.

Do not infer suitability from diameter alone.

## PD335-D verification gate

Before considering the YSS PD Fork Valve for assembly or modification planning,
require:

- Exact manufacturer identification.
- Authoritative installation instructions.
- Valve body diameter.
- Seating face.
- Spring/adjuster orientation.
- Preload setting method.
- Intended fork and damper-rod range.
- Required damper-rod modifications.
- Required oil recommendation.
- Initial setup recommendation.
- Service and inspection requirements.

If authoritative YSS documentation is not retained, keep these items
Unverified.

## Explicit modification gate

No drilling, enlarging, welding, machining, shortening, spacer fabrication,
spring cutting, fork-cap modification, or permanent damper-rod modification is
authorized by this research record.

Before any damper rod is drilled or modified, require all of the following:

1. Exact PD335-D manufacturer installation documentation for the relevant
   valve.
2. Confirmation that the valve is intended for a damper-rod fork architecture
   compatible with the XJ fork.
3. Direct XJ damper-rod measurements.
4. Current compression-hole geometry recorded.
5. Required hole modification from authoritative YSS documentation.
6. Wall-thickness / structural review.
7. Burr-removal and cleaning method.
8. Confirmation that rebound control is not unintentionally bypassed.
9. Defined reassembly and inspection procedure.
10. Technical review.

If any item is missing, status remains **BLOCKED FOR MODIFICATION**.

## Brake-system interaction

The front suspension upgrade interacts with the front-brake upgrade documented
in [RESEARCH-0008](RESEARCH-0008-front-brake-system-integration.md) and
[TEST-PLAN-0003](../testing/TEST-PLAN-0003-front-brake-system-validation.md).

Evaluate and retain evidence for:

- Brake dive.
- Fork stroke usage.
- Brake-hose routing.
- Caliper clearance.
- Wheel/fender clearance.
- Front-end geometry.
- Rider/load case.
- Braking stability.

Do not state that stiffer springs or emulator valves automatically improve
braking safety. The Blue Spot/front master-cylinder upgrade and fork upgrade
must be validated as a system before road acceptance. Successful fork assembly,
cap installation, or bounce testing is not road validation.

Design rider/load case: not yet formally documented in repository evidence.

## Hazards requiring review

The following are hazards to assess, not observed failures. No probability,
severity, or numerical acceptance criteria are assigned here.

| Hazard | Required control before progression |
| --- | --- |
| Wrong cap thread / thread pullout | Direct thread and engagement comparison, sealing/interface evidence, and technical review. |
| Insufficient cap engagement | Recorded original and candidate engagement, stack-height impact, and review. |
| Cap seal leakage | Verified sealing method, seal condition, and controlled leak inspection. |
| Incorrect spring preload | Exact spring and stack evidence plus reviewed preload calculation. |
| Coil bind | Free length, compressed length/coil-bind evidence, available travel, and stack review. |
| Reduced available travel | Full-compression and top-out clearance evidence. |
| Bottoming | Travel, oil level / air-gap method, spring, damping, and static/dynamic evidence under reviewed gates. |
| Top-out | Top-out clearance, spring/stack effect, and rebound behavior review. |
| Excessive fork stiffness | Spring/rate evidence, preload calculation, sag measurement, and controlled functional checks. |
| Insufficient damping | PD-valve documentation, oil recommendation, setup evidence, and functional checks. |
| Excessive damping | Setup evidence, oil recommendation, rebound behavior, and controlled functional checks. |
| Rebound packing | Rebound path/orifice evidence and controlled functional checks. |
| Cavitation/aeration | Oil level / air-gap method, filling/bleeding method, and damping behavior review. |
| Incorrect oil level | Defined measurement method and authoritative setup evidence before filling. |
| Blocked hydraulic path | Damper-rod/valve path inspection and cleaning evidence. |
| Damper rod weakened by drilling | Modification gate, authoritative documentation, structural review, and technical review. |
| Burr/debris contamination | Burr-removal, cleaning, inspection, and reassembly procedure. |
| Seal damage | Seal/bushing identity, tool/method evidence, and inspection. |
| Bushing damage | Bushing identity, condition, installation method, and inspection. |
| Fork misalignment | Controlled assembly, axle/fork alignment method, and static checks. |
| Unequal left/right assembly | Left/right measurement symmetry, matched parts, and recorded settings. |
| Brake-hose interference | Combined steering/suspension movement checks with the brake configuration. |
| Steering interference | Full lock-to-lock checks with installed caps, bars, hoses, and controls. |
| Wheel/fender contact | Full-compression and steering-envelope checks. |
| Fastener/retaining-bolt sealing failure | Bottom-bolt and copper-washer interface evidence, sealing inspection, and reviewed service data. |

## Validation stages

No validation stage is executed or passed by this record. Each stage requires
recorded left/right symmetry and measurements.

| Stage | Initial state | Gate intent |
| --- | --- | --- |
| A. Evidence and parts identification | Not started | Exact parts, markings, labels, source documentation, and evidence class retained. |
| B. Direct dimensional inspection | Not started | Actual XJ fork, original parts, and candidate parts measured at defined datums. |
| C. Dry stack / non-destructive fit check | Not started | Stack height, seating, cap engagement, clearances, and left/right symmetry checked without permanent change. |
| D. Modification review gate | Blocked | Permanent fork or damper-rod modification remains blocked unless the explicit modification gate is satisfied. |
| E. Controlled fork assembly | Blocked | Assembly only after evidence, measurements, service method, oil data, and technical review support it. |
| F. Static motorcycle checks | Blocked | Steering, suspension movement, leaks, sag, hose routing, brake clearance, and left/right behavior checked under reviewed methods. |
| G. Low-risk functional checks | Blocked | Controlled non-road or low-risk checks only after static gates pass and review authorizes the exact scope. |
| H. Road validation only after technical review | Blocked | Road validation requires completed prerequisite evidence, system-level brake/fork review, defined criteria, and separate authorization. |

Successful assembly, threading, or bounce testing does not equal road
validation.

## Decision impact

- Related requirements:
  [SYS-006](../requirements/system-requirements.md#sys-006),
  [SAF-004](../requirements/system-requirements.md#saf-004),
  [SAF-005](../requirements/system-requirements.md#saf-005),
  [REL-002](../requirements/system-requirements.md#rel-002),
  [SRV-001](../requirements/system-requirements.md#srv-001),
  [SRV-002](../requirements/system-requirements.md#srv-002),
  [DEV-002](../requirements/system-requirements.md#dev-002),
  [DEV-003](../requirements/system-requirements.md#dev-003),
  [DEV-005](../requirements/system-requirements.md#dev-005),
  [DEV-007](../requirements/system-requirements.md#dev-007),
  [DEV-008](../requirements/system-requirements.md#dev-008),
  [DOC-002](../requirements/system-requirements.md#doc-002),
  [DOC-003](../requirements/system-requirements.md#doc-003),
  [DOC-006](../requirements/system-requirements.md#doc-006),
  [DOC-008](../requirements/system-requirements.md#doc-008).
- Related research:
  [RESEARCH-0008](RESEARCH-0008-front-brake-system-integration.md).
- Related tests:
  [TEST-PLAN-0003](../testing/TEST-PLAN-0003-front-brake-system-validation.md).
- ADR required: Undetermined; a future accepted fork-upgrade configuration or
  permanent modification may require a decision record.
- Recommended next action: retain part-label photographs, obtain authoritative
  YSS PD335-D and cap/spring documentation, measure the actual XJ fork and
  original parts, then complete a technical review before any installation or
  modification.

## Open questions

- What exact XJ900S fork variant is installed on the project motorcycle?
- What Yamaha manual or parts data applies directly to that exact fork?
- What are the original fork-cap thread, sealing, shoulder, and engagement
  dimensions?
- What is the exact YSS spring part number, rate, free length, end treatment,
  and application?
- What are the authoritative YSS instructions for `PD335-D`?
- What oil recommendation, oil level / air-gap method, and setup data apply to
  the exact valve/spring/fork combination?
- What non-destructive stack height, cap engagement, full-compression, and
  top-out margins exist with all candidate parts?
- What brake-hose, caliper, wheel, fender, steering, and fork-motion clearances
  exist after the brake and fork upgrades are considered together?

## Conclusion

The front-fork upgrade may continue as controlled research and
pre-installation verification only. The on-hand YSS and Wemoto parts are not
accepted for installation or road use by this record. Permanent modification is
blocked until authoritative documentation, direct XJ measurements, structural
review, cleaning/reassembly procedure, and technical review are complete.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-16 | Created front-fork upgrade and pre-installation verification record. | Preserve on-hand part evidence while defining safety-critical evidence, modification, and validation gates. |

## Navigation

[Research index](README.md) | [Front brake research](RESEARCH-0008-front-brake-system-integration.md) | [Front brake validation plan](../testing/TEST-PLAN-0003-front-brake-system-validation.md) | [Documentation index](../INDEX.md)
