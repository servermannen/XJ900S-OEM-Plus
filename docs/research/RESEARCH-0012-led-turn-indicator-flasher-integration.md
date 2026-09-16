# RESEARCH-0012: XJ900S LED turn-indicator and flasher integration

**Purpose:** Preserve the current implementation evidence, observed gaps, and
validation requirements for the XJ900S LED turn-indicator and flasher relay
work without creating a final wiring diagram or acceptance record.

**Document status: Draft**

**Status: Unverified**

**Review: Technical Review Required**

## Research question

What evidence is currently retained for the purchased mini LED turn indicators,
replacement three-pin LED flasher relay, original flasher relay area, relay
connector work, instrument-cluster warning-lamp interaction, mechanical
indicator mounting, compliance status, and validation gates on the 1997 Yamaha
XJ900S?

## Scope

### Included

- Purchased/on-hand turn-indicator and flasher hardware.
- Owner-observed relay markings and motorcycle wiring observations.
- Proposed relay terminal-position changes.
- Connector and depinning evidence requirements.
- Instrument-cluster warning-lamp and possible crossfeed concerns.
- Load and flash behavior evidence requirements.
- Mechanical indicator mounting evidence requirements.
- Compliance, validation, and final acceptance boundaries.

### Excluded

- Final wiring diagram.
- Final relay pinout or OEM harness pinout.
- Final diode-isolation schematic.
- Diode or resistor component selection.
- Road-use acceptance.
- Creation of a separate connector record.
- Modification of Level 1 engine-management records.

No relay click, correct-looking flash, physical connector fit, successful
depinning, all-four illumination, one successful powered test, visible
E-mark-like marking, seller claim, or marketplace description is treated as
complete validation or legal compliance by this record.

## Current status

The repository retains acquisition evidence for mini LED turn indicators and a
generic three-pin LED flasher relay, plus project-reported observations and
implementation discussion supplied for this documentation gap. The record does
not establish the OEM flasher relay pinout, replacement relay pinout, vehicle
harness cavity functions, relay electrical compatibility, diode-isolation
design, legal compliance, validated flash behavior, or road-use acceptance.

**Status: Unverified**

**Review: Technical Review Required**

## Sources and evidence boundary

Repository records reviewed on 2026-09-17. This is not a purchase date,
measurement date, installation date, test date, or technical review date.

| Source | Type | Date accessed | Relevance | Reliability notes |
| --- | --- | --- | --- | --- |
| [Purchased / on-hand inventory](../components/PURCHASED-ON-HAND-INVENTORY.md) | Project inventory | 2026-09-17 | Records mini LED turn indicators and a three-pin LED flasher relay as purchased, delivered and on hand. | Acquisition and availability evidence only; exact manufacturer, model, electrical specifications, pinout, load range, flash-rate characteristic, connector type, E-mark status, homologation and acceptance remain unknown. |
| [Connector identification template](../templates/connector-identification-template.md) | Project template | 2026-09-17 | Defines connector, terminal, locking, cavity, depinning, crimping and compatibility evidence conventions. | Template only; does not identify the XJ relay connector. |
| [RESEARCH-0005: 1997-on electrical baseline extraction](RESEARCH-0005-1997-on-electrical-baseline.md) | Project research | 2026-09-17 | Provides electrical-baseline rules for source separation, wire-colour caution, grounds, relays, diodes and reviewed electrical execution. | Focuses on ignition, pickup, fuel-pump, starter and interlock baseline; it does not map the turn-signal flasher circuit. |
| [System requirements](../requirements/system-requirements.md) | Project requirements | 2026-09-17 | Defines staged validation, electrical protection, documentation, serviceability and technical-review obligations. | Requirements only; not component specification evidence. |
| [System architecture](../architecture/system-architecture.md) | Project architecture | 2026-09-17 | Places lighting and turn-signal functions in the Level 2/body-control domain while preserving Level 1 engine-management authority. | Architecture boundary only; no turn-signal implementation selected. |
| Project-reported observations supplied for this documentation gap | Project discussion input | 2026-09-17 | Preserves owner/project-reported relay markings, one reported frame/ground wire, proposed `E-`/`B+` relocation, possible cluster warning-lamp crossfeed concern, and mounting observations. | Not independently retained as photographs, measurements, wiring diagrams, datasheets or test records in the repository revision reviewed here. Treat as project-reported and Unverified unless later evidence is added. |

## Purchased and on-hand hardware

The following items are already recorded in the inventory. They are not
duplicated there by this record.

| Item | Retained acquisition state | Known technical data | Status and boundary |
| --- | --- | --- | --- |
| Mini LED turn indicators | Purchased, delivered, on hand; source recorded as AliExpress. | Exact manufacturer, model, part number and electrical specifications unknown. Threaded mounting reported by owner/project observation as M8. | Unverified; not accepted. Acquisition and owner-observed thread evidence do not establish electrical compatibility, mechanical suitability, E-mark validity, homologation, luminous intensity, viewing-angle compliance or road legality. |
| Three-pin LED flasher relay | Purchased, delivered, on hand; source recorded as AliExpress. | Exact manufacturer and model unknown; three electrical contacts reported; pinout, load range, polarity, ground requirement, current, voltage limits and flash-rate behavior unknown. | Unverified; not accepted. Physical possession and three-contact description do not establish relay pinout or vehicle compatibility. |

## Existing relay and motorcycle observations

These rows preserve owner/project-reported observations only. They are not a
complete OEM relay pinout or harness map.

| Observation | Evidence state | Boundary |
| --- | --- | --- |
| Existing/original flasher relay has three visible terminals. | Project-reported observation. | Does not establish internal relay architecture, OEM connector cavity numbering, or terminal functions. |
| One visible relay terminal marking is `L`. | Project-reported observation; described as lower terminal marked `L`. | The `L` marking belongs to the relay body observation only. It does not prove the vehicle harness terminal function at that visual position. |
| One visible relay terminal marking is `B`. | Project-reported observation. | The `B` marking is not enough to assign the harness-side switched battery feed without wiring-diagram and continuity evidence. |
| Third relay marking was not conclusively retained/read. | Project-reported observation. | Do not fill the gap from common relay conventions. |
| One associated wire reportedly goes directly to frame/ground. | Project-reported observation. | A frame/ground route must be verified by exact wire identification, continuity method and circuit state. Wire route or colour alone is not proof of relay ground function. |

## Replacement relay and proposed terminal relocation

Project-reported fitment work indicates the replacement relay's required
terminal arrangement did not directly match the existing connector layout. The
project identified a need to swap the positions corresponding to `E-` and
`B+`, while the `L` position was intended to remain unchanged.

**Status: Proposal / Unverified**

This record preserves that as a proposed or planned terminal-position change
only. No retained evidence reviewed here proves:

- the replacement relay's actual pinout;
- which XJ wire is switched battery feed to the relay;
- which XJ wire is flasher output to the indicator circuit;
- which XJ wire, if any, is relay ground;
- that the replacement relay requires a dedicated ground;
- that `E-` and `B+` relocation is electrically correct;
- that `L` on the relay body maps to the intended vehicle circuit;
- that the existing fuse architecture protects the modified circuit;
- that polarity is irrelevant or correctly handled;
- that any completed depinning or repinning was electrically validated.

No repository evidence reviewed for this record explicitly records the
depinning/repositioning as completed. If later evidence shows physical terminal
relocation was completed, record it separately from validated electrical
correctness.

## Connector and depinning evidence

Use the connector convention from the project instructions and connector
template before any connector-level acceptance. Unknown is preferred over
inference.

### Relay connector evidence register

| Evidence item | Current state | Required evidence before acceptance |
| --- | --- | --- |
| Connector side | Unknown. | Identify harness-side connector and relay/device-side interface separately. |
| Visible terminal markings | `L` and `B` owner/project-reported on relay body; third marking not conclusively retained. | Retained photographs or inspection notes of every visible marking with orientation. |
| Viewing orientation | Unknown. | Record wire-entry-side view and mating-side view separately. |
| Housing identity | Unknown. | Manufacturer/family and exact housing part number from authoritative source or retained markings. |
| Terminal family | Unknown. | Terminal family/type/size from authoritative source or confirmed physical evidence. |
| Cavity numbering | Unknown. | OEM numbering from service/connector documentation, or a clearly labelled temporary project locator. |
| Primary locking lance | Unknown. | Identify housing lance, terminal lance or other lock from documentation/inspection. |
| Secondary lock / TPA / retainer | Unknown. | Record presence, service position and correct term. |
| Removal/depinning tool | Unknown. | Exact tool manufacturer/part number or documented method. Successful depinning alone does not identify the correct tool. |
| Terminal reuse status | Unknown. | Manufacturer or service documentation, or record replacement requirement. |
| Wire colour | Unknown in retained evidence for this record. | Record actual wire colours with orientation and evidence. Wire colour alone is not function proof. |
| Circuit function | Unknown. | Establish by exact wiring diagram, continuity mapping and controlled electrical verification. |

Visual left/right/up/down position is not OEM cavity numbering. Relay body
marking alone does not prove vehicle harness terminal function. Physical fit
does not establish electrical compatibility. Successful depinning does not
establish correct depinning-tool identity or terminal reuse acceptability.

## Electrical architecture and required questions

Before final acceptance, answer the following with retained evidence:

- Which XJ wire is switched battery feed to the relay?
- Which XJ wire is flasher output to the indicator circuit?
- Which XJ wire, if any, is relay ground?
- Does the replacement relay require dedicated ground?
- Is relay polarity relevant?
- Is the replacement relay protected by the existing fuse architecture?
- What is the actual replacement relay pin assignment?
- What is the actual OEM relay or harness pin assignment?
- What connector, terminal and cavity identifiers apply to the relay circuit?
- How is the instrument-cluster warning lamp connected to the left and right
  indicator circuits, or otherwise?

Required failure-behavior analysis before road use:

- open indicator;
- short-to-ground;
- short-to-battery;
- reversed relay terminal assignment;
- lost relay ground;
- one failed front indicator;
- one failed rear indicator;
- warning-lamp / cluster crossfeed;
- connector terminal partially backed out.

Safe failure behavior should prioritize no overheated wiring, no unfused fault
path, no unintended all-four flashing caused by wiring error, no loss of
unrelated lighting or Level 1 functions, and practical rider fault detection
where possible. The lighting circuit must not have authority over Level 1
engine management.

## Instrument-cluster warning-lamp and diode isolation

The project has discussed the possibility that an original single/common turn
indicator warning lamp can provide a crossfeed path when low-current LED
indicators are installed. Diode isolation has been discussed/preferred over
load resistors.

**Status: Proposal / Unverified**

Backfeed is a testable concern, not an observed fault on this motorcycle in the
retained repository evidence reviewed here. This record does not authorize a
diode installation from a generic internet diagram.

Require all of the following before selecting or installing diode isolation:

1. Actual XJ wiring diagram for the exact relevant model/year.
2. Identification of how the cluster turn warning lamp connects between left
   and right circuits, or otherwise.
3. Confirmation whether incandescent bulb resistance originally limits
   cross-current.
4. Direct test with the installed or candidate LED indicators.
5. Measurement or observation of unintended opposite-side illumination if it
   occurs.
6. Reviewed diode-isolation schematic if diode isolation is required.
7. Diode electrical specification based on measured or specified circuit
   current and the motorcycle transient environment.
8. Polarity verification.
9. Failure-mode review.
10. Post-modification left/right/hazard behavior validation if hazards exist.

No diode part number, current rating, voltage rating, polarity, orientation,
resistor value, resistor wattage, relay load range, flash frequency, indicator
current or system current is established by this record.

## Load and flash behavior

The following remain Unknown until measured or specified by retained evidence:

- replacement relay load range;
- minimum and maximum LED indicator current;
- installed flash frequency;
- behavior with one failed indicator on either side;
- behavior with one front or one rear indicator disconnected;
- effect of instrument-cluster warning lamp current;
- behavior with low battery voltage and normal charging voltage;
- behavior after heat soak, vibration and repeated operation.

Do not treat relay clicking, lamps flashing, correct-looking flash rate, all
four lamps illuminating, or one successful test as complete validation.

## Mechanical indicator mounting

Project-reported observations include M8 threaded mini LED indicators and a
centering/reducer bushing discussion.

**Status: Unverified / Proposal**

Retained project discussion includes an approximately 12 mm opening at at
least one relevant mounting location, approximately 3 mm mounting thickness in
the mounting context, and approximately 8.3 mm bushing ID discussed as
suitable clearance for an M8 stud. The retained evidence used by this record
does not establish which front/rear location the 12 mm and 3 mm observations
apply to. These values shall not be propagated to another mounting position
without direct measurement.

The approximately 8.3 mm value is a proposed/design clearance dimension for an
M8 stud, not evidence that the same bushing design fits every mounting point.
Independent measurement is required for each actual mounting location before
fabrication or installation.

| Mounting item | Front locations | Rear locations |
| --- | --- | --- |
| Actual hole diameter at each location | Required; measure directly. | Required; measure directly. |
| Mounting plate/tab thickness | Required; measure directly. | Required; measure directly. |
| Indicator M8 thread verification | Owner/project-reported for the mini LED indicators; verify exact thread pitch and usable thread length. | Owner/project-reported for the mini LED indicators; verify exact thread pitch and usable thread length. |
| Available nut/washer engagement | Required; unknown. | Required; unknown. |
| Bushing ID | Required for final design; approximately 8.3 mm is a project-discussed candidate clearance only. | Required for final design; approximately 8.3 mm is a project-discussed candidate clearance only. |
| Bushing OD | Required from actual measured opening. | Required from actual measured opening. |
| Bushing thickness | Required from actual mounting geometry. | Required from actual mounting geometry. |
| Flange requirement | Required; unknown. | Required; unknown. |
| Anti-rotation method | Required; unknown. | Required; unknown. |
| Wire pass-through clearance | Required; unknown. | Required; unknown. |
| Strain relief | Required; unknown. | Required; unknown. |
| Weather sealing | Required; unknown. | Required; unknown. |
| Clearance to bodywork | Required; unknown. | Required; unknown. |
| Movement and heat clearance | Steering movement clearance required. | Exhaust, wheel, luggage and bodywork clearance required where applicable. |

Physical mounting does not establish electrical suitability, visibility
compliance, durability, homologation, or road-use acceptance.

## Compliance and legal evidence

Legal and homologation status is Unverified. This record does not assert
Swedish, EU, ECE or any other road-legality compliance.

Visible E-mark-like markings, seller claims, marketplace descriptions, physical
fit, or apparently bright flashing do not alone establish legal compliance for
the installed configuration. Before road-use acceptance, retain authoritative
current evidence for the exact indicators and installed configuration,
including marking validity, application scope, luminous intensity, flash
visibility, viewing angles, mounting position and any applicable national
requirements.

## Validation stages

No stage below is recorded as executed by this research record.

| Stage | Validation stage | Current execution status | Entry evidence required |
| --- | --- | --- | --- |
| A | Component and marking identification | Not started. | Retained photos/inspection of indicators, relay markings, labels and supplied documentation. |
| B | Exact XJ wiring-diagram mapping | Not started. | Exact model/year diagram and applicability evidence. |
| C | Connector / terminal / depinning identification | Not started. | Relay connector record data, terminal family, locks, tool and reuse status. |
| D | Non-powered continuity and polarity mapping | Not started. | Defined method, disconnected/isolated circuit state and retained results. |
| E | Current-limited bench or motorcycle electrical verification | Not started. | Fuse protection, known polarity, defined current limitation where practical, known relay pin assignment, insulated terminals and stop conditions. |
| F | Left/right functional test | Not started. | Controlled configuration and pass/fail criteria. |
| G | Instrument-cluster/backfeed test | Not started. | Cluster topology evidence, LED configuration and observation/measurement plan. |
| H | Fault-condition checks | Not started. | Reviewed fault-injection scope for open, short, reversed terminal, lost ground and backed-out terminal cases. |
| I | Mechanical mounting and movement-clearance checks | Not started. | Front and rear location measurements, bushing data, strain relief, sealing and clearance envelopes. |
| J | Final system check / road-use acceptance | Blocked. | Completion of evidence stages, technical review and compliance evidence. |

Electrical energization requires fuse protection, known supply polarity,
defined current limitation where practical, known relay pin assignment, no
loose or uninsulated terminals, and stop conditions for heat, smoke, abnormal
current, chatter or unintended illumination.

## Final acceptance boundary

The turn-signal system is not accepted by this record. Before acceptance,
retain source evidence, direct observations, measurements, completed validation
results, compliance evidence where required, and technical review.

## Decision impact

- Related requirements: SYS-010, SAF-006, SAF-007, REL-002, REL-006, SRV-003,
  SRV-007, ARC-002, ARC-003, ARC-008, DEV-001 through DEV-008, DOC-001 through
  DOC-009.
- Related components: Mini LED turn indicators and three-pin LED flasher relay
  in the purchased/on-hand inventory.
- ADR required: Undetermined; no architecture or acceptance decision is made
  here.
- Recommended next action: Capture retained photographs and inspection notes
  for the relay, relay connector, wire-entry side, mating side, indicator
  mounting locations and indicator markings; then map the exact wiring diagram
  and define a reviewed, current-limited electrical test method.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-17 | Created LED turn-indicator and flasher integration evidence record. | Close documentation gap while preserving uncertainty, technical-review gates, and no road-use acceptance. |

## Navigation

[Research index](README.md) | [Purchased / on-hand inventory](../components/PURCHASED-ON-HAND-INVENTORY.md) | [Connector template](../templates/connector-identification-template.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Documentation index](../INDEX.md)
