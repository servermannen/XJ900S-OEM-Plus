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
- Use of 1995 Yamaha manual specifications as confirmed 1997 project
  motorcycle specifications before applicability is established.

## Current status

The front-fork upgrade remains a pre-installation research and evidence gate.
No component compatibility, service specification, damping setup, installation
configuration, modification, test result, or road-use approval is established
by this record.

**Status: Unverified**

**Review: Technical Review Required**

## Sources and current evidence

Repository records reviewed on 2026-09-16 and reconciled with supplied Yamaha
manual evidence on 2026-09-17. These dates are not purchase, measurement,
installation, or test dates.

| Source | Type | Relevance | Evidence boundary |
| --- | --- | --- | --- |
| Yamaha XJ900S(G) '95 Service Manual, manual number `4KM-28197-20`, chassis maintenance specifications, manual page 2-13, project PDF page 33 | Yamaha service manual evidence supplied to the project | Provides front-suspension maintenance specification values for the manual-stated XJ900S(G) '95 application. | Confirmed for the Yamaha 1995 manual application only. Use as confirmed 1997 Yamaha factory specifications requires authoritative Yamaha continuity evidence. Direct project-bike measurements can establish as-found geometry and dimensions, but not Yamaha 1997 factory specification continuity. |
| [Purchased / on-hand component inventory](../components/PURCHASED-ON-HAND-INVENTORY.md) | Project inventory | Records acquisition/on-hand context for fork-related parts. | Availability record only; not compatibility or acceptance evidence. |
| [RESEARCH-0008](RESEARCH-0008-front-brake-system-integration.md) | Project research | Defines front-brake integration evidence needs involving the actual XJ900S fork, wheel, discs, hoses, and suspension movement. | Brake-system evidence gate only; does not validate fork upgrade components. |
| [TEST-PLAN-0003](../testing/TEST-PLAN-0003-front-brake-system-validation.md) | Project test plan | Defines staged front-brake validation and movement/clearance checks. | Not executed; does not authorize road use. |
| [System requirements](../requirements/system-requirements.md) | Project requirements | Defines safety, staged validation, documentation, and technical-review obligations. | Requirements and process basis only; not fork specification data. |

## Yamaha 1995 baseline evidence

The following values are retained from the Yamaha XJ900S(G) '95 Service Manual,
manual number `4KM-28197-20`, chassis maintenance specifications, manual page
2-13, project PDF page 33.

**Status: Confirmed** for the Yamaha 1995 manual application.

**Status: Unverified** for the project-recorded 1997 XJ900S until
authoritative Yamaha evidence establishes no relevant fork specification change
for 1997. Direct physical measurements may establish as-found geometry,
dimensions, interfaces, stack height, spring dimensions, damper-rod
architecture, and other directly measurable characteristics of the actual
project fork, but do not by themselves confirm Yamaha's 1997 factory
specification for oil grade, oil capacity, oil level, spring rate, spring-rate
transition/stroke, or model-year specification continuity.

| Front-suspension item | Yamaha 1995 manual value | Evidence status | 1997 project applicability |
| --- | --- | --- | --- |
| Front fork travel | 140 mm | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Front spring free length | 505 mm | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Spring rate K1 | 5.0 N/mm (0.5 kg/mm) | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Spring rate K2 | 9.0 N/mm (0.9 kg/mm) | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Stroke K1 | 0-80 mm | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Stroke K2 | 80-140 mm | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Optional spring | No | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Oil capacity | 444 cm3 | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Oil level | 133 mm | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |
| Oil grade | Fork oil 5W or equivalent | Confirmed for Yamaha XJ900S(G) '95 manual application | Unverified |

This baseline does not establish fork-cap thread specification, damper-rod
dimensions, compression-hole count or diameter, fork-cap sealing geometry,
41 mm fork-tube applicability to the 1997 motorcycle, PD335-D compatibility,
YSS spring compatibility, or any requirement to drill the damper rod.

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

## Required 1997 XJ900S baseline evidence

The exact 1997 XJ900S fork variant and project-motorcycle specifications
remain evidence gaps unless separately retained from an authoritative 1997
XJ900S source or established by authoritative Yamaha continuity evidence.
Direct measurement of the actual project motorcycle may establish as-found
physical geometry and dimensions, but not Yamaha factory specification
continuity. The 1995 Yamaha manual values above may be used as bounded
comparison evidence only until 1997 specification applicability is established
by authoritative Yamaha evidence.

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

## 1997 applicability gate

Before using any 1995 Yamaha value as a confirmed 1997 Yamaha factory
specification, establish authoritative Yamaha specification continuity for that
value. Direct project-bike measurement remains useful for physical
compatibility work, but it does not confirm Yamaha's factory specification
continuity.

Evidence paths are separated as follows:

- OEM part-number/specification continuity: requires authoritative Yamaha
  evidence.
- Actual physical geometry: may be established by direct measurement of the
  actual project fork.
- Spring rate: requires authoritative Yamaha evidence or controlled
  spring-rate measurement; dimensional inspection alone is insufficient.
- Oil grade, oil capacity, and oil level as Yamaha factory specifications:
  require authoritative Yamaha evidence.

Until authoritative continuity evidence is retained for a given factory
specification, the corresponding 1995 value remains confirmed only for the
manual-stated 1995 application and Unverified for the project-recorded 1997
motorcycle.

## Direct-measurement gate

Before any irreversible fork or damper-rod modification, record the following
minimum measurements from the actual project motorcycle and on-hand parts.

### Fork / original cap

- Fork tube outside diameter.
- Original cap male-thread major diameter.
- Thread pitch.
- Usable thread engagement length.
- Original cap shoulder/seating geometry.
- Sealing/O-ring arrangement.
- Internal depth from tube top to spring/spacer stack.

### Original spring/stack

- Spring free length.
- Spring outside diameter and inside diameter.
- Wire diameter.
- End geometry.
- Spacer length.
- Washer thickness, outside diameter, and inside diameter.
- Existing static preload derived from measured stack dimensions.

### YSS cap

- Measured thread major diameter.
- Measured pitch.
- Threaded length.
- Shoulder/seating geometry.
- O-ring/seal geometry.
- Adjuster travel.
- Protrusion above fork tube / possible handlebar or upper-yoke interference.

### YSS spring

- Exact visible part number or label.
- Free length.
- Outside diameter.
- Inside diameter.
- Wire diameter.
- End geometry.
- Spring-rate evidence if present on label or documentation.

### PD335-D

- Outside diameter.
- Total height.
- Lower seating diameter/profile.
- Top spring-contact geometry.

### Damper rod

Only after normal reversible disassembly, record:

- Top outside diameter.
- Central bore inside diameter.
- Seating-face geometry available for the PD valve.
- Existing compression-hole count.
- Existing hole diameters.
- Axial positions of holes.
- Wall thickness where modification might otherwise be proposed.

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

No drilling, enlargement, welding, machining, shortening, spacer fabrication,
spring cutting, fork-cap modification, or permanent damper-rod alteration is
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

## Decision gates

No gate is executed or passed by this record. Each gate requires recorded
left/right symmetry and measurements where applicable.

| Gate | Initial state | Gate intent |
| --- | --- | --- |
| A. Documentation baseline | Not started | Applicability status of relevant Yamaha specifications explicitly known, and unresolved model-year differences identified. Authoritative continuity evidence is required wherever a 1995 Yamaha value is to be used as a confirmed 1997 factory specification. |
| B. Dimensional | Not started | YSS cap/spring/PD valve and actual fork dimensions recorded as as-found physical evidence; this can proceed without resolving every Yamaha factory-specification continuity question. |
| C. Dry compatibility | Not started | Thread engagement, sealing seat, centering, stack height, and mechanical clearances demonstrated without permanent modification. |
| D. Reversible assembly | Blocked | Only after Gates A-C pass and oil/stack/preload requirements are defined. |
| E. Permanent modification | Blocked | Requires separate technical review and explicit evidence for the exact PD335-D installation requirements on this fork architecture. |
| F. Road validation | Blocked | Remains blocked until assembly, sag, travel, damping behavior, clearance, and safety validation are completed. |

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
- Recommended next action: document the 1997 applicability status of the
  retained 1995 Yamaha baseline, retain part-label photographs, obtain
  authoritative YSS PD335-D and cap/spring documentation, measure the actual XJ
  fork and original parts, then complete a technical review before any
  installation or modification.

## Open questions

- What exact XJ900S fork variant is installed on the project motorcycle?
- Do authoritative Yamaha records show the 1997 fork assembly / OEM
  part-number family, tube/top-thread geometry, spring specification,
  damper-rod architecture, and oil specification are materially unchanged from
  the 1995 manual application?
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
accepted for installation or road use by this record. The recovered Yamaha
front-suspension values are confirmed only for the manual-stated 1995
application and remain Unverified for the project-recorded 1997 motorcycle.
Direct project-bike measurements may establish as-found physical compatibility
evidence but do not confirm Yamaha factory specification continuity. Permanent
modification is blocked until required documentation status, direct project
measurements, authoritative PD335-D documentation, structural review,
cleaning/reassembly procedure, and technical review are complete.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-18 | Clarified that direct measurement can establish as-found physical evidence but not Yamaha factory specification continuity, and that dimensional evidence may proceed independently of unresolved factory-specification continuity. | Prevent direct project-bike measurement from being read as confirming complete 1995-to-1997 Yamaha specification applicability. |
| 2026-09-17 | Reconciled recovered Yamaha XJ900S(G) '95 front-suspension service-manual evidence, added 1997 applicability and direct-measurement gates, and restated permanent-modification blocking. | Preserve confirmed 1995 Yamaha baseline values without converting them into confirmed 1997 project specifications or authorizing YSS installation/drilling. |
| 2026-09-16 | Created front-fork upgrade and pre-installation verification record. | Preserve on-hand part evidence while defining safety-critical evidence, modification, and validation gates. |

## Navigation

[Research index](README.md) | [Front brake research](RESEARCH-0008-front-brake-system-integration.md) | [Front brake validation plan](../testing/TEST-PLAN-0003-front-brake-system-validation.md) | [Documentation index](../INDEX.md)
