# Purchased / On-Hand Component Inventory

**Purpose:** Record components reported as purchased, acquired, delivered, installed, or physically available to the XJ900S OEM+ / Diversion 2027 project.

**Document status: Draft**

**Status: Unverified**

This is an acquisition and availability record, not a compatibility or
acceptance register. Acquisition evidence is not compatibility evidence;
seller identification is not authoritative Yamaha application evidence; and
physical possession does not establish health or completeness. Successful
connector fit does not establish electrical or functional compatibility.

Safety-critical components require technical review and validation before road
use.

| Component | Part number | Source | Purchase date | Physical identity | Status | Evidence | Acceptance state |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [COMP-0001: MT-07 front brake master cylinder and lever](COMP-0001-2022-mt07-front-brake-master-cylinder.md) | `1XB-2580A-00-00` seller-reported | Owner-provided purchase identification | Not recorded | Owner-reported MT-07 2022 assembly; official application and physical identity Unverified | Acquired candidate | COMP-0001 owner-reported provenance | Unverified; not accepted |
| [COMP-0002: MT-07 clutch lever and perch](COMP-0002-2022-mt07-clutch-lever-perch.md) | Unknown | Owner-provided purchase identification | Not recorded | Owner-reported MT-07 2022 assembly; official application and physical identity Unverified | Acquired candidate | COMP-0002 owner-reported provenance | Unverified; not accepted |
| [COMP-0003: FZS600 handlebar](COMP-0003-2003-fzs600-handlebar.md) | `5RT2611001` supplied seller/product number; candidate normalized form `5RT-26110-01` Unverified | Owner-provided purchase identification | Not recorded | Owner-reported 2003 FZS600 handlebar; physical identity Unverified | Purchased candidate | COMP-0003 owner-reported provenance | Unverified; not accepted |
| [COMP-0004: Tracer 9 right switch and DBW grip](COMP-0004-2023-2024-tracer9-right-switch-dbw-grip.md) | `BAP-8291R-10` currently supplied project identification | Owner-provided purchase identification | Not recorded | Owner-reported Tracer 9 assembly; exact Yamaha application, variant, and physical identity Unverified | Purchased candidate | COMP-0004 project-reported provenance | Unverified; not accepted; DBW not accepted |
| [COMP-0005: MT-10 throttle-body assembly](COMP-0005-2022-mt10-throttle-body-assembly.md) | Unknown | Owner-reported purchase identification | Not recorded | Owner-reported MT-10 RN781/B5Y assembly; physical identity Unverified | Purchased candidate | COMP-0005 owner-reported provenance | Unverified; not accepted |
| [COMP-0006: MT-10 RN781/B5Y main wiring harness](COMP-0006-mt10-b5y-main-wiring-harness.md) | `B5Y-82590-00` supplied | Baboon.eu | 2026-08-19 | Seller/donor identified as MT-10 RN781/B5Y; physical identity not yet verified | Purchased, used; arrival/inspection not recorded | Owner-reported acquisition provenance and seller identification | Unverified; not accepted |
| [COMP-0007: Tracer 9 GT BAP/MTT890 front/sub-harness](COMP-0007-tracer9-b5u-front-sub-harness.md) | `B5U-82509-00` supplied | Baboon.eu | 2026-08-19 | Seller/donor identified as Tracer 9 GT BAP/MTT890; physical identity not yet verified | Purchased, used; arrival/inspection not recorded | Owner-reported acquisition provenance and seller identification | Unverified; not accepted |
| [COMP-0008: Tracer 900 GT left handlebar switch](COMP-0008-tracer-900-gt-left-handlebar-switch.md) | `B1J-83954-11-00` current project-supplied identification; conflicting historic `B5U-83954-01` | Owner-provided purchase identification | Not recorded | Exact Yamaha application, market/model-year coverage, supersession relationship, and physical identity Unverified | Purchased / on hand candidate | COMP-0008 project-reported provenance and retained historic conflict | Unverified; not accepted |
| [COMP-0009: R1 Blue Spot front brake calipers](COMP-0009-r1-blue-spot-front-brake-calipers.md) | Right `5JJ-2580U-00-00`; left `5JJ-25880T-00-00`, owner/project-reported | Owner-provided purchase identification | Not recorded | Yamaha OEM/R1/Blue Spot identity is owner/project-reported; exact physical identity, condition, donor application, and fitment Unverified | Purchased pair / on hand candidate | COMP-0009 owner/project-reported provenance | Unverified; not accepted; technical review required |
| [COMP-0010: B5Y inertial-module candidate](COMP-0010-owner-observed-yamaha-b5y-inertial-module-candidate.md) | Unknown | Source not recorded | Not recorded | Owner-observed on-hand module with visible label `B5Y0`, visible marking/serial `B5Y000M33S205A`, four mounting holes with metal bushings, integrated 4-position connector, and associated connector/harness wire colours observed as red/white, blue/black, blue/white, black/white from the wire-entry side in the project-shown orientation; exact Yamaha function, part number, source model, connector identity, pinout, protocol, and compatibility Unverified | Acquired / on hand candidate | COMP-0010 owner-observed physical evidence and project-reported on-hand context | Unverified; not accepted; technical review required |
| [COMP-0011: Yamaha 1WS-82380-00-00 pressure-sensor candidate](COMP-0011-yamaha-1ws-82380-00-00-pressure-sensor-candidate.md) | `1WS-82380-00-00` project-supplied identifier; `1WS-82380` short form | Source not recorded | Not recorded | Separate loose pressure-sensor candidate; exact Yamaha application, MT-07 association, exact function, electrical characteristics, pressure range, transfer function, calibration, connector identity, and uaEFI compatibility Unverified | Acquired / on hand spare/reference/test candidate | Project discussion and COMP-0011 project-supplied identifier | Unverified; not accepted; technical review required |
| Existing donor O2 / lambda sensor candidate(s) | Visible/project-observed markings reported as `2CR-10` and `270 0101722`; compact search form `2700101722` not separately established; candidate Yamaha identifier `2CR-8592A-20-00` project-supplied / Unverified | Source not recorded | Not recorded | One or more existing donor oxygen-sensor candidates reported physically/project-observed; exact count, donor model/application, manufacturer, DENSO identification, sensor technology, heater architecture, wire count, pinout, connector identity, signal type, controller requirements, and uaEFI WBO1/WBO2 compatibility Unverified | Acquired / on hand candidate(s) | Current project discussion and reported markings/identifier; no authoritative Yamaha application evidence retained here | Unverified; not accepted; technical review required |
| rusEFI uaEFI SUPER | Supplier SKU `SQ2035226`; order `#00012` | VERÉB ecu&more | 2026-08-25 | Delivered ECU physically on hand; observed board/revision marking consistent with Rev B / `mega-uaEFI 0.3`; optional IGBT positions `Q841`, `Q842`, `Q843`, `Q844`, `Q845`, and `Q846` observed unpopulated; exact hardware, schematic, BOM and build-option applicability remains Unverified | Delivered / physically on hand | Supplier/order provenance and later project physical observation recorded in RESEARCH-0007 | Unverified; not accepted; technical review required |
| Two brake-caliper repair kits associated with COMP-0009 | Unknown | Owner-provided purchase identification | Not recorded | Exact manufacturer, part numbers, contents, materials, and applicability Unknown | Purchased / on hand | Owner/project-reported acquisition and intended association | Unverified; not accepted |
| EBC brake pads intended for COMP-0009 | Unknown | Owner-provided purchase identification | Not recorded | Exact part number, compound, dimensions, homologation, and applicability Unknown | Purchased / on hand | Owner/project-reported acquisition, brand, and intended association | Unverified; not accepted |
| Original XJ900S passenger grab handles | Unknown | Owner-provided acquisition identification | Not recorded | Yamaha OEM/original XJ900S provenance owner-reported; exact part numbers and physical identity Unverified | Acquired / on hand | Owner-reported acquisition and provenance | Unverified; not accepted |
| Aftermarket mirrors | Unknown | Owner-provided purchase identification | Not recorded | Exact manufacturer, model, part number, specifications, and physical identity Unknown | Purchased / on hand | Owner-reported acquisition | Unverified; not accepted |
| T10/W5W instrument-cluster LED lamps | Unknown | Owner-provided installation status | Not recorded | Installed in the XJ900S instrument cluster; exact manufacturer, model, part number, and electrical specifications Unknown | Installed | Owner-reported installation status | Unverified; installation does not establish legal compliance, durability, or final acceptance |
| Mini LED turn indicators | Unknown | AliExpress | Not recorded | Exact manufacturer, model, part number, and electrical specifications Unknown | Purchased, delivered, on hand | Owner-reported acquisition and delivery status | Unverified; not accepted |
| Three-pin LED flasher relay | Unknown | AliExpress | Not recorded | Exact manufacturer and model Unknown; three electrical contacts reported; pinout and electrical specifications Unknown | Purchased, delivered, on hand | Owner-reported acquisition, delivery status, and physical description | Unverified; not accepted |

## YSS front-fork upgrade parts

- Supplier: Not recorded
- Purchase/order date: Not recorded
- Delivery state: Delivered / physically on hand — owner-reported / directly
  observed markings as listed below
- Delivery date: Not recorded
- Evidence basis: Owner-reported delivery/on-hand state and retained visible
  markings. These entries are acquisition and marking evidence only.

The markings below do not establish XJ900S compatibility, cap thread
compatibility, spring suitability, valve suitability, required damper-rod
modification, oil recommendation, oil level, preload, fork setup, or road
acceptance.

| Supplied / observed item | Supplied or observed identifier | Source | Purchase date | Physical identity | Status | Evidence | Acceptance state |
| --- | --- | --- | --- | --- | --- | --- | --- |
| YSS fork cap | Marking/model `FCM38-41-001-50`; marking `M38x1.0`; marking `tube 41 mm` | Not recorded | Not recorded | Owner-observed markings only; XJ900S cap-thread compatibility and installed geometry Unverified | Delivered / physically on hand | Owner-reported/on-hand state and observed markings | Unverified; not accepted; technical review required |
| YSS PD Fork Valve | Marking/model `PD335-D` | Not recorded | Not recorded | Owner-observed marking only; exact valve dimensions, intended fork architecture, setup data and XJ900S compatibility Unverified | Delivered / physically on hand | Owner-reported/on-hand state and observed marking | Unverified; not accepted; technical review required |
| YSS fork spring pair | Unknown | Not recorded | Not recorded | Delivered spring pair; exact part number, rate, free length, dimensions, application and suitability Unknown | Delivered / physically on hand | Owner-reported/on-hand state | Unverified; not accepted; technical review required |

See [RESEARCH-0010](../research/RESEARCH-0010-front-fork-upgrade-pre-installation-verification.md)
for the front-fork pre-installation evidence and modification gates. Recording
these parts here does not authorize installation or modification.

## Wemoto order 1305414493

- Supplier: Wemoto
- Purchase/order date: 2026-09-01
- Delivery state: Delivered / on hand — owner-reported
- Delivery date: Not recorded
- Evidence basis: Owner-supplied order number, item numbers and descriptions, followed by the owner's report that all seven items have been delivered and are physically on hand. Detailed physical inspection is not recorded.

The item numbers and descriptions below are supplied/order provenance, not verified physical identities, OEM specifications or manufacturer application claims. Brand names, material descriptions and the rear-pad "HH" designation are retained only as supplied in the order description. Quantity ordered does not establish delivered completeness.

| Supplied/order description | Supplied/order part number | Source | Purchase date | Physical identity | Status | Evidence | Acceptance state |
| --- | --- | --- | --- | --- | --- | --- | --- |
| EBC sintered rear brake pads, HH | `AA5293` | Wemoto | 2026-09-01 | Unverified; supplied order description only | Purchased, delivered / on hand; detailed inspection not recorded | Owner-supplied order 1305414493 and owner-reported delivery/on-hand state | Unverified; not accepted |
| HEL rear hydraulic brake line | `SM-MVAA3733-BL-CA-61` | Wemoto | 2026-09-01 | Unverified; supplied order description only | Purchased, delivered / on hand; detailed inspection not recorded | Owner-supplied order 1305414493 and owner-reported delivery/on-hand state | Unverified; not accepted |
| Stainless double banjo bolt intended for the front master-cylinder / dual front brake-line arrangement | `PKAD5706` | Wemoto | 2026-09-01 | Unverified; supplied order description only | Purchased, delivered / on hand; detailed inspection not recorded | Owner-supplied order 1305414493 and owner-reported delivery/on-hand state | Unverified; not accepted |
| TRK stainless rear brake piston and seal kit | `PKAG7185` | Wemoto | 2026-09-01 | Unverified; supplied order description only | Purchased, delivered / on hand; detailed inspection not recorded | Owner-supplied order 1305414493 and owner-reported delivery/on-hand state | Unverified; not accepted |
| HEL front hydraulic brake lines, Race Set-Up | `SM-MVAB3633-BL-CA-61` | Wemoto | 2026-09-01 | Unverified; supplied order description only | Purchased, delivered / on hand; detailed inspection not recorded | Owner-supplied order 1305414493 and owner-reported delivery/on-hand state | Unverified; not accepted |
| Slinky Glide front-fork repair kit | `PKAA9870` | Wemoto | 2026-09-01 | Unverified; supplied order description only | Purchased, delivered / on hand; detailed inspection not recorded | Owner-supplied order 1305414493 and owner-reported delivery/on-hand state | Unverified; not accepted |
| Copper sealing washers for the front-fork damper retaining bolt; quantity ordered: 2 | `AB7343` | Wemoto | 2026-09-01 | Unverified; supplied order description only | Purchased, delivered / on hand; detailed inspection not recorded | Owner-supplied order 1305414493 and owner-reported delivery/on-hand state | Unverified; not accepted |

### Order evidence limitations

Delivery/on-hand status establishes owner-reported acquisition/delivery provenance only. It does not establish exact physical identity, completeness, condition, seller-description accuracy, manufacturer authenticity beyond the supplied description, Yamaha application, mechanical/physical fit, hydraulic, suspension, functional or electrical compatibility, service or safety suitability, successful installation, validation, completed technical review, component selection or final acceptance.

- The double banjo bolt's intended use does not establish fit with the MT-07 master cylinder, HEL hoses, Blue Spot calipers or XJ900S.
- The rear piston/seal kit is not established as applicable to the installed/original rear caliper. The rear pads' description and HH designation do not confirm compound or application beyond the supplied order provenance.
- The HEL line descriptions establish no hose dimensions, banjo angles, fitting specifications, homologation, routing suitability or installed compatibility.
- The fork kit and damper-bolt washers have no verified exact fork application, seal/washer dimensions or suitability. Material wording is only the supplied description; ordering under a vehicle selection does not establish compatibility with the 1997 XJ900S.
- These rear-brake items do not identify or resolve the separate front-caliper repair kits and EBC pads already recorded for COMP-0009.
- Recording the brake-related items closes no open requirement or validation gate in [RESEARCH-0008](../research/RESEARCH-0008-front-brake-system-integration.md) or [TEST-PLAN-0003](../testing/TEST-PLAN-0003-front-brake-system-validation.md).

**Review: Technical Review Required**

This label preserves the safety-review requirement; it records no completed technical review or permission to install or test the items.

## Inventory use and evidence boundary

The listed status records only the reported acquisition or availability state.
It does not verify seller/donor identification, Yamaha application, part-number
application, component completeness, condition, connector identity, electrical
function, physical fit, functional fit, safety suitability, or final
acceptance. Each of those matters requires its own evidence and review.

No voltage, power, current, polarity, connector type, homologation, E-mark
status, relay pin assignment, load range, or flash-rate characteristic is
recorded for the unmarked LED items because no evidence is retained here.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-09-17 | Added existing donor O2 / lambda sensor candidate inventory entry with reported `2CR-10`, `270 0101722`, search form `2700101722`, and project-supplied candidate `2CR-8592A-20-00` identifiers. | Preserve acquisition/observation evidence without accepting identity, Yamaha application, DENSO manufacturer identity, sensor technology, heater, pinout, signal type, uaEFI WBO compatibility, or final selection. |

## Navigation

[Component index](README.md) | [Documentation index](../INDEX.md)
