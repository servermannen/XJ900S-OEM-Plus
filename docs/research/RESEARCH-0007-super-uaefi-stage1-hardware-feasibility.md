# RESEARCH-0007: Super uaEFI Stage 1 Hardware Feasibility

**Purpose:** Record the evidence-bounded static hardware and physical-I/O
feasibility of the purchased rusEFI uaEFI SUPER as the primary Level 1 ECU
candidate for the proposed XJ900S Stage 1 allocation.

**Document status: Review**

**Status: Proposal**

**Review: Technical Review Required**

Reason for `Status: Proposal`: upstream Super uaEFI hardware capability and pin
definitions may be Confirmed individually at the pinned source revisions, but
the XJ900S Stage 1 allocation and hardware suitability remain project
proposals until the physical ECU revision and Yamaha-side electrical
interfaces are validated.

In this record, `PASS` means that a static allocation fits the reviewed
physical pin definition without an identified Stage 1 cavity conflict. It does
not mean electrical compatibility, functional validation, technical
acceptance, or permission to energize or install hardware.

## 1. Purpose

This record maps the proposed initial XJ900S Level 1 engine-management
functions to the physical 120-cavity Super uaEFI connector set. It preserves
the source revision, connector naming conflicts, reserved resources, safety
boundaries, and evidence gates that must be closed before hardware acceptance.

## 2. Scope and boundaries

### Included

- Static review of the Super uaEFI connector YAML, generated metadata, board
  defaults, and schematic-extraction notes at a pinned rusEFI revision.
- Proposed Stage 1 allocation for crank-only synchronization, semi-sequential
  injection, wasted-spark ignition, open-loop fueling, DBW, required engine
  sensors, safety inputs, relays, power, ground, diagnostics, and Level 2 CAN.
- A complete map of physical cavities A1-A34, B1-B26, C1-C34, and D1-D26.
- Static resource-conflict analysis and seven remaining hardware/safety gates.

### Excluded

- Acceptance of the ECU, its physical revision, the MT-10 throttle body, the
  Tracer 9 grip, DBW, injectors, ignition hardware, Yamaha sensors, tip-over
  implementation, wiring, protection, calibration, or road use.
- Electrical limits not stated by the pinned upstream sources or established
  by direct measurement.
- Firmware configuration release, harness design, powered testing, fault
  injection, motorcycle installation, an ADR, or modification of older
  research and accepted decisions.

## 3. Project status and procurement context

The following is procurement evidence only. Purchase does not establish
technical suitability or acceptance.

| Field | Recorded procurement evidence |
| --- | --- |
| Component | rusEFI uaEFI SUPER |
| Supplier | VERÉB ecu&more |
| Supplier SKU | `SQ2035226` |
| Order | `#00012` |
| Order date | 2026-08-25 |
| Quantity | 1 |
| Procurement status | Purchased / On order |
| Intended project role | Primary Level 1 ECU candidate |
| Technical acceptance | Not accepted |

The exact hardware revision, build options, populated ignition drivers,
condition, and correspondence to the reviewed pinout remain Unverified until
the delivered unit is inspected.

## 4. Evidence baseline and pinned revisions

### rusEFI firmware and pinout

The allocation was reviewed at immutable rusEFI revision
[`bcf8b7e166f6a05ede58e9e1763407d15e2d4333`](https://github.com/rusefi/rusefi/commit/bcf8b7e166f6a05ede58e9e1763407d15e2d4333).

| Evidence ID | Pinned upstream source | Use in this record |
| --- | --- | --- |
| UAEFI-SRC-001 | [`connectors/60pin.yaml`](https://github.com/rusefi/rusefi/blob/bcf8b7e166f6a05ede58e9e1763407d15e2d4333/firmware/config/boards/hellen/super-uaefi/connectors/60pin.yaml) | Physical A/B connector functions, types, and firmware metadata. |
| UAEFI-SRC-002 | [`connectors/C-34pins-4k.yaml`](https://github.com/rusefi/rusefi/blob/bcf8b7e166f6a05ede58e9e1763407d15e2d4333/firmware/config/boards/hellen/super-uaefi/connectors/C-34pins-4k.yaml) | Physical C connector functions, power, USB, and low-side outputs. |
| UAEFI-SRC-003 | [`connectors/26pin_4k.yaml`](https://github.com/rusefi/rusefi/blob/bcf8b7e166f6a05ede58e9e1763407d15e2d4333/firmware/config/boards/hellen/super-uaefi/connectors/26pin_4k.yaml) | Physical D connector functions, ETB, VR, CAN, grounds, and buttons. |
| UAEFI-SRC-004 | [`connectors/generated_board_pin_names.h`](https://github.com/rusefi/rusefi/blob/bcf8b7e166f6a05ede58e9e1763407d15e2d4333/firmware/config/boards/hellen/super-uaefi/connectors/generated_board_pin_names.h) | Generated connector-to-platform-symbol associations, including D24-D26. |
| UAEFI-SRC-005 | [`board_configuration.cpp`](https://github.com/rusefi/rusefi/blob/bcf8b7e166f6a05ede58e9e1763407d15e2d4333/firmware/config/boards/hellen/super-uaefi/board_configuration.cpp) | Default sensor, trigger, ETB, main-relay, and fuel-pump assignments. |
| UAEFI-SRC-006 | [`hellen_mm100_meta.h`](https://github.com/rusefi/rusefi/blob/bcf8b7e166f6a05ede58e9e1763407d15e2d4333/firmware/config/boards/hellen_mm100_meta.h) | Platform-symbol resolution to MCU pins and ADC channels. |
| UAEFI-SRC-007 | [`docs/schematic-notes.md`](https://github.com/rusefi/rusefi/blob/bcf8b7e166f6a05ede58e9e1763407d15e2d4333/firmware/config/boards/hellen/super-uaefi/docs/schematic-notes.md) | Rev C schematic extraction, cross-check notes, driver options, C32 discrepancy, and A6/A15 summary inconsistency. |

UAEFI-SRC-007 records `docs/super-uaefi-c-schematic.pdf` as a 28-page,
KiCad-generated schematic, Rev C, dated 2026-04-29. It states that the
connector mapping was cross-checked against the YAML and firmware sources.

### Public hardware documentation

| Evidence ID | Pinned upstream source | Use and limitation |
| --- | --- | --- |
| UAEFI-SRC-008 | [`super-uaEFI.md`](https://github.com/rusefi/rusefi_documentation/blob/a7c3e7116502c70f1a69faae09e204c34fe04b3c/super-uaEFI.md) at [`a7c3e7116502c70f1a69faae09e204c34fe04b3c`](https://github.com/rusefi/rusefi_documentation/commit/a7c3e7116502c70f1a69faae09e204c34fe04b3c) | Public capability summary and hardware-documentation context. It links schematic Rev B and does not identify the project unit's revision. |

Sources were accessed on 2026-08-26. The firmware/pinout revision is the
controlling static source for this allocation. Public feature summaries do not
override cavity-level YAML or firmware evidence.

## 5. Hardware-revision discrepancy

**Status: Unverified**

The firmware repository's pinned schematic notes describe Super uaEFI
schematic Rev C, dated 2026-04-29, with 28 pages and a connector/pin mapping
cross-check. The pinned public hardware document still links a schematic
identified as Rev B. This is an evidence discrepancy, not proof that one
revision supersedes or applies to the ordered unit.

The delivered uaEFI SUPER must be inspected for PCB and revision markings and
matched positively to an applicable schematic and pinout. Until then, Rev B
versus Rev C applicability and any build-option differences remain
Unverified. This discrepancy is HG-01 and blocks hardware acceptance.

### A6/A15 platform-symbol and summary inconsistency

**Status: Confirmed**

Classification: Upstream documentation inconsistency.

The pinned sources preserve the following distinct definitions:

- `connectors/60pin.yaml` defines A6 as
  `MM100_IN_O2S2_ANALOG` and A15 as `MM100_IN_AUX1_ANALOG` / TPS2.
- `hellen_mm100_meta.h` defines `MM100_IN_O2S2` as PA1,
  `MM100_IN_O2S2_ANALOG` as `EFI_ADC_1`, `MM100_IN_AUX1` as PB0, and
  `MM100_IN_AUX1_ANALOG` as `EFI_ADC_8`.
- `board_configuration.cpp` assigns TPS2 using
  `MM100_IN_AUX1_ANALOG`.

The summary table in pinned `schematic-notes.md` is inconsistent with that
chain: it shows A15/TPS2 as PA1 while also showing A6 as PA1 and notes shared
metadata history. Later in the same file, the input mapping records `IN_O2S2`
as PA1 and `IN_AUX1` as PB0.

This is classified as an upstream documentation inconsistency, not a physical
Stage 1 allocation conflict. The project allocation follows the pinned
connector YAML, `hellen_mm100_meta.h`, and board firmware:

- A6 = independent auxiliary analog path / `MM100_IN_O2S2_ANALOG`;
- A15 = TPS2 / `MM100_IN_AUX1_ANALOG`.

The proposed simultaneous use of A6 and A15 therefore does not currently
create an identified static resource conflict. Because A15 is a DBW feedback
channel and A6 is proposed for a safety input, the physical delivered ECU must
still be checked under HG-01 before either channel is accepted. Neither cavity
is assigned `CONFLICT`; C32 remains the only cavity explicitly marked
`CONFLICT` / `DO NOT USE`.

## 6. Stage 1 working definition

The accepted later project direction used by this feasibility record requires:

- DBW from the first engine-control implementation;
- crank-only synchronization initially;
- semi-sequential injection initially;
- wasted-spark ignition initially;
- open-loop fueling initially;
- no dependency on cam synchronization;
- no dependency on closed-loop lambda; and
- no dependency on knock control.

The owner-reported 2022 MT-10 throttle-body assembly remains the working
baseline and primary integration candidate, so Stage 1 must provide APS1,
APS2, TPS1, TPS2, ETB motor positive/negative control, DBW plausibility, and a
defined safe-state path. [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md)
remains `Status: Unverified`; this record does not accept it or DBW.

### Historical traceability

[RESEARCH-0001](RESEARCH-0001-engine-management-platform.md) and
[RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) contain
historical text that permits cable throttle initially or treats DBW as a
future option. This record does not rewrite that history. The later project
direction used here requires DBW in Stage 1 because the MT-10 electronic
throttle-body assembly is the working integration baseline. A future focused
update or superseding decision may reconcile those records.

## 7. Super uaEFI connector architecture

The reviewed connector definition exposes 120 physical cavities:

| Connector | Physical range | Count | Principal reviewed roles |
| --- | --- | ---: | --- |
| A | A1-A34 | 34 | Analog/event inputs, +5 V references, and GNDA returns. |
| B | B1-B26 | 26 | Ignition, injector and low-side outputs, +5 V, GNDA, power ground, digital/FLEX, and MAP. |
| C | C1-C34 | 34 | Key-voltage sense, switched/permanent power, WBO2, USB, EGT, grounds, hot low-sides, blanks, and C32 discrepancy. |
| D | D1-D26 | 26 | WBO1, two DC bridges, knock, two VR paths, grounds, CAN, high side, switched power, and buttons. |
| **Total** | **A-D** | **120** | **Complete physical connector set reviewed in this record.** |

`Allocation status: PASS` below means only that the proposed use occupies a
reviewed physical cavity with no identified static Stage 1 collision.

## 8. Stage 1 functional I/O allocation

Expected electrical values remain Unverified unless the upstream physical
function itself states a supply category. Safe states in this table are
proposals requiring technical review and fault-injection evidence.

| Function | Source component | Signal type | Expected voltage/current | Safe state | Super uaEFI connector | Physical cavity | Firmware/hardware name | Required pull-up/pull-down/conditioning | Failure behavior | Stage 1 required / future reserved | Allocation status | Evidence status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CKP | XJ900S original pickup | Passive VR candidate | Yamaha waveform, polarity and amplitude Unverified | Stop injection and ignition; de-energize pump after validated timeout | D | D10/D11 | `VR_9924-` / `VR_9924+`; positive path to `MM100_UART8_TX` | MAX9924 conditioning; polarity and any optional damping Unverified | Loss/invalid sequence must not command fuel or ignition | Stage 1 Required | PASS | Upstream path Confirmed; Yamaha compatibility Unverified; allocation Proposal |
| APS1 | Tracer 9 DBW grip candidate | Analog position | Candidate transfer curve and electrical limits Unverified | Remove ETB drive for implausible/invalid redundant demand | A | A13 | `MM100_IN_PPS_ANALOG` / PPS1 | Candidate-specific interface Unverified | Redundant-pair plausibility and fault response required | Stage 1 Required | PASS | Upstream pin Confirmed; candidate interface Unverified; allocation Proposal |
| APS2 | Tracer 9 DBW grip candidate | Analog position | Candidate transfer curve and electrical limits Unverified | Remove ETB drive for implausible/invalid redundant demand | A | A7 | `MM100_IN_AUX2_ANALOG` / PPS2 | Candidate-specific interface Unverified | Redundant-pair plausibility and fault response required | Stage 1 Required | PASS | Upstream pin Confirmed; candidate interface Unverified; allocation Proposal |
| TPS1 | 2022 MT-10 throttle-body candidate | Analog position | Candidate transfer curve and electrical limits Unverified | Remove ETB drive for implausible/invalid redundant feedback | A | A5 | `MM100_IN_TPS_ANALOG` / TPS1 | Candidate-specific interface Unverified | Redundant-pair plausibility and fault response required | Stage 1 Required | PASS | Upstream pin Confirmed; candidate interface Unverified; allocation Proposal |
| TPS2 | 2022 MT-10 throttle-body candidate | Analog position | Candidate transfer curve and electrical limits Unverified | Remove ETB drive for implausible/invalid redundant feedback | A | A15 | `MM100_IN_AUX1_ANALOG` / TPS2 | Candidate-specific interface Unverified | Redundant-pair plausibility and fault response required | Stage 1 Required | PASS | Upstream pin Confirmed; candidate interface Unverified; allocation Proposal |
| ETB | 2022 MT-10 throttle-body servo candidate | Bidirectional DC motor | Motor running, transient and stall current Unverified | De-energize bridge; throttle returns to validated mechanical safe position | D | D6/D7 | `DC1-` / `DC1+`; TLE9201SG H-bridge; default `etbFunctions[0] = DC_Throttle1` | H-bridge is upstream-conditioned; fuse/current/thermal strategy open | Fault must remove unsafe drive and enter defined DBW safe state | Stage 1 Required | PASS | Upstream bridge/default Confirmed; motor/thermal suitability Unverified; allocation Proposal |
| MAP | Purchased Yamaha MAP candidate | Analog pressure | Identity and transfer function Unverified | Defined degraded response; no value invented | B | B26 | `MM100_IN_MAP1_ANALOG` / MAP | B16 +5 V and B23 GNDA proposed | Missing/invalid response and substitution policy Unverified | Stage 1 Required | PASS | Upstream pin/supply/return Confirmed; sensor interface Unverified; allocation Proposal |
| IAT | Purchased Yamaha B5Y temperature-sensor candidate | Resistive/analog temperature candidate | Exact identity and calibration Unverified | Defined bounded fault response; no value invented | A | A12 | `MM100_IN_IAT_ANALOG` / IAT | Upstream default analog-temperature pull-up path; candidate calibration Unverified | Open/short/plausibility handling required | Stage 1 Required | PASS | Upstream pin Confirmed; sensor identity/calibration Unverified; allocation Proposal |
| Engine temperature | Sensor not selected | Analog temperature candidate | Sensor and range Unverified | Defined bounded fault response; no value invented | A | A11 | `MM100_IN_CLT_ANALOG` / CLT-labelled input | Upstream default analog-temperature pull-up path; air-cooled sensor/location open | Open/short/plausibility handling required | Stage 1 Required | PASS | Upstream pin Confirmed; sensor/location Proposal and Unverified |
| Injector 1 | Injector not selected | Low-side injector output | Impedance, current and dead time Unverified | Command disabled for shutdown/critical fault | B | B13 | `MM100_INJ1` | Driver compatibility, flyback, fuse and power architecture Unverified | No unintended fuel command; diagnostic response required | Stage 1 Required | PASS | Upstream output Confirmed; injector compatibility Unverified; allocation Proposal |
| Injector 2 | Injector not selected | Low-side injector output | Impedance, current and dead time Unverified | Command disabled for shutdown/critical fault | B | B12 | `MM100_INJ2` | Driver compatibility, flyback, fuse and power architecture Unverified | No unintended fuel command; diagnostic response required | Stage 1 Required | PASS | Upstream output Confirmed; injector compatibility Unverified; allocation Proposal |
| Injector 3 | Injector not selected | Low-side injector output | Impedance, current and dead time Unverified | Command disabled for shutdown/critical fault | B | B11 | `MM100_INJ3` | Driver compatibility, flyback, fuse and power architecture Unverified | No unintended fuel command; diagnostic response required | Stage 1 Required | PASS | Upstream output Confirmed; injector compatibility Unverified; allocation Proposal |
| Injector 4 | Injector not selected | Low-side injector output | Impedance, current and dead time Unverified | Command disabled for shutdown/critical fault | B | B10 | `MM100_INJ4` | Driver compatibility, flyback, fuse and power architecture Unverified | No unintended fuel command; diagnostic response required | Stage 1 Required | PASS | Upstream output Confirmed; injector compatibility Unverified; allocation Proposal |
| Wasted-spark bank 1 | Ignition architecture not selected | Logic/smart-coil output by default | Coil/igniter current and dwell Unverified | No-spark command state | B | B2 | `MM100_IGN1` | Default logic output; onboard IGBT option or external igniter remains open | No unintended spark; loss and driver fault handling required | Stage 1 Required | PASS | Upstream default Confirmed; XJ coil compatibility Unverified; allocation Proposal |
| Wasted-spark bank 2 | Ignition architecture not selected | Logic/smart-coil output by default | Coil/igniter current and dwell Unverified | No-spark command state | B | B3 | `MM100_IGN2` | Default logic output; onboard IGBT option or external igniter remains open | No unintended spark; loss and driver fault handling required | Stage 1 Required | PASS | Upstream default Confirmed; XJ coil compatibility Unverified; allocation Proposal |
| Fuel-pump relay | Relay/interface not selected | Low-side relay control | Relay current/interface Unverified | Relay de-energized where shutdown is required | C | C31 | `MM100_OUT_PWM2` / LS4; default `fuelPumpPin` | External relay, flyback, protection and fuse design Unverified | Prime/run/stall/fault timeout behavior requires validation | Stage 1 Required | PASS | Upstream pin/default Confirmed; vehicle interface Unverified; allocation Proposal |
| Main-relay control | Relay/interface not selected | Always-hot-capable low-side relay control | Relay current/interface Unverified | Defined power-down sequence; no unintended maintained actuation | C | C30 | `MM100_IGN7` / LS5_HOT; default `mainRelayPin` | External relay, flyback, protection and fuse design Unverified | Startup, shutdown and controller-reset behavior requires validation | Stage 1 Required | PASS | Upstream pin/default Confirmed; vehicle interface Unverified; allocation Proposal |
| Ignition/key voltage sense | XJ900S key circuit | Analog battery-voltage sense | Upstream 12 V input category; XJ circuit behavior Unverified | Defined key-off shutdown and brownout handling | C | C1 | `MM100_IN_VBATT` | Board input conditioning upstream-defined; XJ interface/protection requires validation | Missing/implausible state must not create unsafe output | Stage 1 Required | PASS | Upstream input Confirmed; XJ interface Unverified; allocation Proposal |
| Permanent battery supply | Protected battery feed not designed | Permanent +12 V supply | Upstream `+12v Bat+`; load and transients Unverified | External protection isolates foreseeable faults | C | C26 | `+12v Bat+ (Hot all times)` | External fusing, reverse-polarity/transient protection and wiring design open | Loss/brownout/recovery behavior requires validation | Stage 1 Required | PASS | Upstream cavity Confirmed; protection design Proposal/Unverified |
| ETB/H-bridge switched supply | Main-relay-fed supply not designed | Switched +12 V input | Upstream switched +12 V category; current/thermal demand Unverified | Supply removed on critical shutdown | C | C10 | `+12v from main relay (ecu input to feed h-bridges)` | Fuse, conductor, relay and current strategy open | Loss or fault must remove unsafe ETB drive | Stage 1 Required | PASS | Upstream cavity Confirmed; fuse/current strategy Proposal/Unverified |
| Engine stop | XJ900S engine-stop switch | Switched input candidate | Switch voltage/interface Unverified | Stop or inhibit engine operation under validated logic | D | D24 | `BUTTON1`; metadata `MM100_IN_CRANK` | External interface, active state, pull and protection Unverified | Open/short/stuck and startup-state behavior required | Stage 1 Required | PASS | Physical BUTTON1 Confirmed; project use Proposal; XJ interface Unverified |
| Sidestand | XJ900S sidestand switch | Switched input candidate | Electrical interface Unverified | Defined safety response under accepted interlock logic | D | D25 | `BUTTON2`; metadata `MM100_IN_CAM` | External interface, active state, pull and protection Unverified | Open/short/stuck behavior and running/start distinction required | Stage 1 Required | PASS | Physical BUTTON2 Confirmed; project use Proposal; XJ interface Unverified |
| Neutral | XJ900S neutral switch | Switched input candidate | Electrical interface Unverified | Defined state/diagnostic response | D | D26 | `BUTTON3` / `MM100_IN_D4` | External interface, active state, pull and protection Unverified | Open/short/stuck behavior and interlock interaction required | Stage 1 Required | PASS | Physical BUTTON3 Confirmed; project use Proposal; XJ interface Unverified |
| Clutch | XJ900S clutch switch | Analog/digital input candidate | Electrical interface Unverified | Defined state/diagnostic response | A | A16 | `MM100_IN_AUX3`; analog/digital, no pull | External pull/conditioning and protection open | Open/short/stuck behavior and interlock interaction required | Stage 1 Required | PASS | Upstream no-pull input Confirmed; project use Proposal; XJ interface Unverified |
| Tip-over | Sensor not selected | Independent direct analog safety input candidate | Sensor voltage/interface Unverified | Level 1 shutdown of ETB, injectors, ignition and fuel pump; deliberate recovery | A | A6 | `MM100_IN_O2S2_ANALOG`; AIN2 with 500K pulldown | Sensor selection, interface, thresholds and diagnostics open | Disconnected/short/stuck/frozen behavior must be validated | Stage 1 Required safety function | PASS | Upstream input/pulldown Confirmed; sensor and project implementation Proposal/Unverified |
| CAN to Level 2 | Level 2 not selected | Differential CAN | Physical layer is upstream-defined; project network details Unverified | Level 1 remains autonomous if CAN is lost | D | D18/D19 | CAN Low / CAN High | Termination, topology, protection, protocol and timeouts open | Loss/invalid/stale data must not transfer Level 1 authority | Stage 1 interface | PASS | Upstream CAN cavities Confirmed; project interface Proposal |

The purchased B5Y IMU gains no Level 1 shutdown authority in this record. Its
interface, protocol, startup diagnostics, stale-data behavior, failure
handling, and functional suitability have not been validated.

## 9. Full 120-pin cavity map

Every row below is one physical cavity. Blank cavities remain blank; no
function is invented. `RESERVED` preserves a resource without accepting a
future use.

### Connector A — 34 cavities

| Cavity | Upstream physical function | Current XJ900S project allocation | Allocation state |
| --- | --- | --- | --- |
| A1 | +5 V HALL1 sensor | Future active-sensor supply reserve | RESERVED |
| A2 | +5 V HALL2 sensor | Future cam sensor supply reserve | RESERVED |
| A3 | +5 V HALL3 sensor | Future active-sensor supply reserve | RESERVED |
| A4 | +5 V DIN sensor | Candidate direct safety-sensor supply | PASS |
| A5 | Universal analog input; suggested TPS1 | MT-10 TPS1 | PASS |
| A6 | Auxiliary analog input 2; 500K pulldown | Proposed independent direct tip-over input | PASS |
| A7 | Universal analog input; suggested PPS2 | APS2 | PASS |
| A8 | VSS / HALL1 sensor | Future event-input reserve | RESERVED |
| A9 | CAM sensor exhaust / HALL3 | Future event/SENT reserve | RESERVED |
| A10 | +5 V | TPS/reference supply | PASS |
| A11 | ECT/CLT temperature input | Proposed air-cooled-engine temperature input | PASS |
| A12 | IAT sensor input | IAT candidate | PASS |
| A13 | Universal analog input; suggested PPS1 | APS1 | PASS |
| A14 | Auxiliary analog input 1; 500K pulldown | Future analog-input reserve | RESERVED |
| A15 | Universal analog input; suggested TPS2 | MT-10 TPS2 | PASS |
| A16 | Analog/digital input; no pull | Proposed clutch input | PASS |
| A17 | CAM sensor intake / HALL2 | Future cam input reserve | RESERVED |
| A18 | +5 V | APS/reference supply | PASS |
| A19 | +5 V | Future sensor-supply reserve | RESERVED |
| A20 | +5 V | Future sensor-supply reserve | RESERVED |
| A21 | +5 V | Future sensor-supply reserve | RESERVED |
| A22 | +5 V | Future sensor-supply reserve | RESERVED |
| A23 | GNDA analog/sensor ground | TPS return | PASS |
| A24 | GNDA analog/sensor ground | APS return | PASS |
| A25 | GNDA analog/sensor ground | Engine-temperature return | PASS |
| A26 | GNDA analog/sensor ground | IAT return | PASS |
| A27 | GNDA analog/sensor ground | Tip-over return | PASS |
| A28 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| A29 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| A30 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| A31 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| A32 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| A33 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| A34 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |

### Connector B — 26 cavities

| Cavity | Upstream physical function | Current XJ900S project allocation | Allocation state |
| --- | --- | --- | --- |
| B1 | Coil 7 unused | None | UNALLOCATED |
| B2 | Smart ignition coil 1 / IGN1 | Wasted-spark ignition bank 1 | PASS |
| B3 | Smart ignition coil 2 / IGN2 | Wasted-spark ignition bank 2 | PASS |
| B4 | Smart ignition coil 3 / IGN3 | Future sequential-ignition reserve | RESERVED |
| B5 | Smart ignition coil 4 / IGN4 | Future sequential-ignition reserve | RESERVED |
| B6 | Smart ignition coil 5 / IGN5 | Future sequential-ignition reserve | RESERVED |
| B7 | Smart ignition coil 6 / IGN6 | Future sequential-ignition reserve | RESERVED |
| B8 | Injector 6 / INJ6 | Future injector-output reserve | RESERVED |
| B9 | Injector 5 / INJ5 | Future injector-output reserve | RESERVED |
| B10 | Injector 4 / INJ4 | Injector 4 | PASS |
| B11 | Injector 3 / INJ3 | Injector 3 | PASS |
| B12 | Injector 2 / INJ2 | Injector 2 | PASS |
| B13 | Injector 1 / INJ1 | Injector 1 | PASS |
| B14 | Coil 8 unused | None | UNALLOCATED |
| B15 | Power/chassis ground | ECU power/chassis ground | PASS |
| B16 | +5 V | MAP supply candidate | PASS |
| B17 | +5 V | Future sensor-supply reserve | RESERVED |
| B18 | Injector 8 / SPI2_SCK-backed output | Future injector-output reserve | RESERVED |
| B19 | Injector 7 / SPI2_CS-backed output | Future injector-output reserve | RESERVED |
| B20 | Low-Side 1 output | Future low-side reserve | RESERVED |
| B21 | Low-Side 2 output | Future low-side reserve | RESERVED |
| B22 | Low-Side 3 output | Future low-side reserve | RESERVED |
| B23 | GNDA analog/sensor ground | MAP return | PASS |
| B24 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| B25 | Digital input / FLEX fuel sensor | Future digital/event-input reserve | RESERVED |
| B26 | MAP signal / MAP1 analog | MAP candidate signal | PASS |

### Connector C — 34 cavities

| Cavity | Upstream physical function | Current XJ900S project allocation | Allocation state |
| --- | --- | --- | --- |
| C1 | Ignition switch / battery-voltage analog input | Ignition/key voltage sense | PASS |
| C2 | +12 V from main-relay output | Future switched-supply reserve | RESERVED |
| C3 | WBO2 SWD programming access | WBO2 reserve | RESERVED |
| C4 | WBO2 SWC programming access | WBO2 reserve | RESERVED |
| C5 | WBO2 Vs (Un) | WBO2 reserve | RESERVED |
| C6 | WBO2 CalR | WBO2 reserve | RESERVED |
| C7 | WBO2 Ip | WBO2 reserve | RESERVED |
| C8 | WBO2 Vs/Ip (Vm) | WBO2 reserve | RESERVED |
| C9 | WBO2 heater negative | WBO2 reserve | RESERVED |
| C10 | +12 V from main relay; H-bridge feed input | ETB/H-bridge switched supply | PASS |
| C11 | Fused +12 V from main-relay output / auxiliary daisy chain | Future switched-supply reserve | RESERVED |
| C12 | USB VBUS | Service/diagnostics | PASS |
| C13 | USB D- | Service/diagnostics | PASS |
| C14 | USB D+ | Service/diagnostics | PASS |
| C15 | PROG button | Programming/service reserve | RESERVED |
| C16 | Blank; no YAML function | None | UNALLOCATED |
| C17 | Blank; no YAML function | None | UNALLOCATED |
| C18 | Fused +12 V from main-relay output / auxiliary daisy chain | Future switched-supply reserve | RESERVED |
| C19 | Blank; no YAML function | None | UNALLOCATED |
| C20 | Blank; no YAML function | None | UNALLOCATED |
| C21 | Power/chassis ground | ECU power/chassis ground | PASS |
| C22 | Power/chassis ground | ECU power/chassis ground | PASS |
| C23 | Blank; no YAML function | None | UNALLOCATED |
| C24 | Blank; no YAML function | None | UNALLOCATED |
| C25 | Blank; no YAML function | None | UNALLOCATED |
| C26 | +12 V Bat+, hot at all times | Permanent protected battery supply | PASS |
| C27 | EGT positive input | Future EGT reserve | RESERVED |
| C28 | EGT negative input | Future EGT reserve | RESERVED |
| C29 | Low-Side 6 HOT / IGN8; YAML describes fuel-relay-capable output | Future hot low-side reserve | RESERVED |
| C30 | Low-Side 5 HOT / IGN7; main-relay control output | Main-relay control | PASS |
| C31 | Low-Side 4 / PWM2; firmware default fuel-pump pin | Fuel-pump relay control | PASS |
| C32 | No YAML function; schematic extraction reports `IN_KNOCK2` | DO NOT USE until upstream discrepancy is resolved | CONFLICT |
| C33 | Blank; no YAML function | None | UNALLOCATED |
| C34 | Blank; no YAML function | None | UNALLOCATED |

### Connector D — 26 cavities

| Cavity | Upstream physical function | Current XJ900S project allocation | Allocation state |
| --- | --- | --- | --- |
| D1 | WBO1 Vs (Un) | WBO1 reserve | RESERVED |
| D2 | WBO1 Vs/Ip (Vm) | WBO1 reserve | RESERVED |
| D3 | WBO1 heater negative | WBO1 reserve | RESERVED |
| D4 | DC2- output | Future DC2 reserve | RESERVED |
| D5 | DC2+ output | Future DC2 reserve | RESERVED |
| D6 | DC1- output | MT-10 ETB motor negative | PASS |
| D7 | DC1+ output | MT-10 ETB motor positive | PASS |
| D8 | WBO1 CalR | WBO1 reserve | RESERVED |
| D9 | Knock-sensor input | Future knock reserve | RESERVED |
| D10 | VR_9924 negative input | XJ CKP negative candidate | PASS |
| D11 | VR_9924 positive input / `MM100_UART8_TX` | XJ CKP positive candidate | PASS |
| D12 | VR_DISCRETE negative input | Future trigger/phase reserve | RESERVED |
| D13 | VR_DISCRETE positive input / `MM100_UART8_RX` | Future trigger/phase reserve | RESERVED |
| D14 | WBO1 SWC programming access | WBO1 reserve | RESERVED |
| D15 | WBO1 Ip | WBO1 reserve | RESERVED |
| D16 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| D17 | Power/chassis ground | ECU power/chassis ground | PASS |
| D18 | CAN bus Low | Level 2 CAN Low | PASS |
| D19 | CAN bus High | Level 2 CAN High | PASS |
| D20 | High-side high-current output | Future high-side reserve | RESERVED |
| D21 | WBO1 SWD programming access | WBO1 service reserve | RESERVED |
| D22 | +12 V from main-relay output | Future switched-supply reserve | RESERVED |
| D23 | GNDA analog/sensor ground | Future sensor-return reserve | RESERVED |
| D24 | BUTTON1 sensor; metadata `MM100_IN_CRANK` | Proposed engine-stop input | PASS |
| D25 | BUTTON2 sensor; metadata `MM100_IN_CAM` | Proposed sidestand input | PASS |
| D26 | BUTTON3 input / `MM100_IN_D4` | Proposed neutral input | PASS |

## 10. Power, ground and 5 V reference allocation

**Status: Proposal**

| Class | Proposed Stage 1 cavities | Boundary |
| --- | --- | --- |
| Permanent battery supply | C26 | Upstream function is hot-at-all-times +12 V. External fusing, wire sizing, transient/reverse-polarity protection, and isolation are not designed or accepted. |
| Key/ignition sense | C1 | Upstream function is an ignition-switch/battery-voltage analog input. The XJ interface remains Unverified. |
| ETB/H-bridge switched supply | C10 | Upstream function feeds the H-bridges from main-relay +12 V. Fuse, relay, current and thermal strategy remain open. |
| +5 V references | A4 direct safety-sensor candidate; A10 TPS; A18 APS; B16 MAP | Each named cavity is identified as +5 V in the pinned YAML. This does not establish sensor compatibility, supply grouping, current budget, independence, or fault containment. |
| GNDA sensor returns | A23 TPS; A24 APS; A25 engine temperature; A26 IAT; A27 tip-over; B23 MAP | Each named cavity is identified as GNDA in the pinned YAML. Final reference routing, shared-fault analysis, and shielding remain open. |
| Power/chassis grounds | B15, C21, C22, D17 | These are upstream power/chassis grounds and are not relabelled as sensor grounds. Final conductor sizing, topology, bonding, and voltage-drop criteria remain open. |

The static mapping separates GNDA from power/chassis ground. It does not
accept a grounding, protection, or harness architecture.

## 11. DBW allocation

**Status: Proposal**

APS1/APS2 use A13/A7, TPS1/TPS2 use A5/A15, and DC1 uses D6/D7. The board
default assigns the same four analog functions and
`etbFunctions[0] = DC_Throttle1`. The pinned schematic notes identify two
TLE9201SG H-bridges and logic/PWM control.

Static pin availability does not establish candidate pinout, reference
voltage, channel independence, transfer direction, correlation, plausibility
thresholds, servo current, fuse margin, PCB thermal margin, mechanical safe
position, or safe-state behavior. HG-02 and HG-03 remain OPEN. Direct throttle
authority remains Level 1; Level 2 CAN cannot command or become required for
basic DBW operation.

## 12. Trigger allocation

**Status: Proposal**

D24 is **not** the Stage 1 physical crank VR input. The generated metadata
associates D24 with the platform symbol `MM100_IN_CRANK`, but the physical
connector definition identifies D24 as `BUTTON1`. That naming discrepancy is
preserved rather than silently normalized.

The Super uaEFI default crank path is the MAX9924-conditioned input:

- D10 = `VR_9924-`;
- D11 = `VR_9924+`, mapped to `MM100_UART8_TX`; and
- `board_configuration.cpp` assigns
  `triggerInputPins[0] = Gpio::MM100_UART8_TX` with the source comment
  `VR2 max9924 is the safer default`.

D10/D11 are therefore the current physical Stage 1 CKP candidate for the
original XJ900S pickup. This is a proposed allocation, not evidence that the
pickup is a compatible VR source. Yamaha waveform, polarity, amplitude, air
gap, noise, decoder stability, and loss-of-sync behavior remain Unverified
under HG-04. D12/D13 and the HALL resources remain reserved for later trigger
or phase evaluation.

## 13. Injection and ignition allocation

**Status: Proposal**

B13/B12/B11/B10 provide four separate injector outputs for the proposed
semi-sequential Stage 1 configuration. Static output count is sufficient, but
injector identity, impedance, current, flow, pressure, dead time, power,
fusing, flyback and thermal compatibility remain Unverified under HG-06.

B2/B3 provide two ignition commands for the proposed wasted-spark Stage 1
configuration. The pinned schematic notes state that the outputs are
logic-level/smart-coil outputs by default, with an onboard IGBT populate option.
Direct drive of the original XJ coils is not confirmed. Onboard IGBTs,
external igniters, and smart coils remain open alternatives under HG-05.
B4-B7 remain reserved for later sequential-ignition capability.

## 14. Safety and supervisory inputs

**Status: Proposal**

- D24/BUTTON1 is proposed for engine stop, D25/BUTTON2 for sidestand,
  D26/BUTTON3 for neutral, and A16/no-pull analog/digital input for clutch.
- A6/AIN2 with its documented 500K pulldown is proposed for an independent
  direct Level 1 tip-over input.
- Actual XJ switch voltage, active states, contacts, shared circuitry, pulls,
  protection, failure states, and running-engine versus starter-permission
  behavior remain Unverified.
- A valid fall event must retain Level 1 authority over ETB, injectors,
  ignition, and fuel pump and require deliberate recovery. The direct sensor
  strategy remains open under HG-07.
- The purchased B5Y IMU has no shutdown authority in this allocation.

## 15. Future reserved resources

The static allocation preserves:

- HALL/event resources and +5 V supply for future cam/phase sensing;
- B4-B7 for future sequential ignition;
- B8/B9 and B18/B19 as additional injector-capable outputs;
- both WBO interfaces;
- D9 knock input;
- A14 and other unused/reserved analog/digital resources;
- B20-B22 additional low-side outputs;
- D4/D5 DC2;
- D20 high-side output;
- EGT, switched-supply and service resources; and
- D18/D19 CAN for the Level 2 interface without transferring Level 1
  authority.

Reservation is not acceptance of a future feature or evidence that all
simultaneous electrical, thermal, firmware, or fault-containment constraints
can be satisfied.

## 16. Resource-conflict analysis

**Status: Confirmed for the static allocation only**

- No Stage 1 cavity shortage was identified.
- No Stage 1 project function is intentionally double-allocated. Differential
  pairs, motor pairs, and CAN pairs intentionally consume their two distinct
  complementary cavities.
- Sufficient physical resources remain reserved for future cam/phase.
- Sufficient ignition outputs remain reserved for future sequential ignition.
- Both WBO interfaces and the knock input remain reserved.
- Additional analog/digital inputs, low-side outputs, DC2, and a high-side
  output remain physically available or reserved.
- CAN remains available and allocated for Level 2, while Level 1 remains
  autonomous if CAN is lost.
- The A6/A15 upstream documentation inconsistency does not currently create a
  static resource conflict: the pinned YAML, platform metadata, and board
  default resolve A6 and A15 to distinct analog paths.
- C32 is an isolated upstream documentation conflict and is not used by Stage
  1. It remains `CONFLICT` / `DO NOT USE`.

| Classification | Result | Boundary |
| --- | --- | --- |
| I/O capacity | PASS | Static physical capacity only. |
| Physical pin allocation feasibility | PASS | Static cavity assignment only. |
| Resource-conflict check | PASS except unresolved upstream C32 discrepancy | C32 is excluded from project use. |
| Hardware acceptance | NOT PASSED | HG-01 through HG-07 and subsequent bench validation remain required. |

## 17. Seven remaining hardware/safety gates

All gates are `Status: OPEN`. Documentation review may establish a starting
point but cannot pass a gate whose criterion requires physical measurement,
controlled energization, fault injection, or bench validation.

| Gate | Safety relevance | Current evidence | Missing evidence | Required test/document | Pass criterion | Current result | Next action |
| --- | --- | --- | --- | --- | --- | --- | --- |
| HG-01 — Physical uaEFI SUPER hardware revision | Pinout, driver, protection and build-option applicability, including safety-relevant A6 and DBW-feedback A15 | Pinned Rev C firmware/schematic notes, connector YAML, platform metadata, board defaults, and public Rev B documentation; the A6/A15 summary inconsistency is recorded | Delivered-unit PCB/revision markings, build population, and physical confirmation that the applicable A6/A15 paths match the pinned allocation | Inspect delivered ECU; photograph/transcribe PCB and revision markings; compare with pinned schematic and pinout; resolve Rev B/Rev C applicability; check A6 and A15 before either is accepted | Physical unit revision and applicable schematic/pinout are positively matched, including the A6/A15 paths used by this allocation | OPEN | Quarantine the allocation from harness release and do not accept A6 or A15 until physical identity and applicable paths are recorded |
| HG-02 — MT-10 ETB electrical and thermal compatibility | Direct throttle actuation and uncontrolled-motion risk | D6/D7 DC1 and TLE9201SG path exist upstream; donor assembly is a candidate only | Exact motor connector/pinout, meaningful resistance, running/transient/stall current, bridge/PCB/fuse/thermal margins, spring-return safe position | Create a technically reviewed, current-limited ETB characterization method; record running, transient and safe stall characterization plus thermal-margin analysis | Validated current and thermal margins plus defined safe de-energized behavior | OPEN | Positively identify servo terminals and define the reviewed method before energization |
| HG-03 — APS/TPS redundant DBW sensor interfaces | Incorrect demand/feedback could command unsafe throttle | Four upstream analog cavities and firmware defaults are statically available; donor manuals describe redundant reference architectures | Candidate APS1/APS2 and TPS1/TPS2 pinouts, references, returns, full-travel curves, directions/correlation, normal ranges, thresholds, and electrical-fault behavior | Characterize both pairs independently; test disconnected, short-to-ground and short-to-reference conditions under a reviewed method; define DBW safe-state logic | Both redundant pairs can be independently acquired and reliably checked for plausibility with defined DBW safe-state behavior | OPEN | Complete positive connector identification before defining powered tests |
| HG-04 — XJ900S CKP electrical compatibility | Loss/false synchronization can cause mistimed fuel or ignition | D10/D11 MAX9924 path and firmware default are confirmed upstream; original pickup remains an Unverified passive-VR candidate | Direct 1997 resistance, polarity, cranking waveform, amplitude versus RPM where practical, air gap, noise, conditioner behavior and decoder stability | Use the reviewed pickup-characterization and later decoder-validation plans; validate D10/D11 conditioning, cranking/run synchronization and loss-of-sync response | Reliable crank synchronization over cranking and operating range with defined loss-of-sync behavior | OPEN | Satisfy TEST-PLAN-0001 safety prerequisites before waveform work |
| HG-05 — Ignition-driver compatibility | Incorrect dwell/driver selection can damage hardware or create unintended/no spark | B2/B3 exist; upstream outputs are logic/smart-coil by default with optional onboard IGBTs | XJ coil primary resistance, inductance, current and dwell; physical ECU IGBT population; comparison of onboard IGBT, external igniter and smart-coil alternatives | Inspect ECU population; collect coil evidence; analyze alternatives; use bench-safe loads before any coil energization | Selected ignition architecture has adequate electrical/thermal margin and a defined no-spark safe state | OPEN | Identify physical ECU build and retain all three driver alternatives until evidence supports selection |
| HG-06 — Injector electrical compatibility | Incorrect driver/load/fuel delivery can cause overheating, leakage or uncontrolled fueling | Four required low-side outputs are statically available | Selected injector identity, impedance, current, flow, pressure, dead time versus voltage, driver/thermal margin, fuse and power architecture | Establish authoritative injector data and a technically reviewed safe-load/driver validation plan before fuel testing | Selected injectors are electrically compatible and have sufficient controlled operating margin | OPEN | Identify injectors and obtain authoritative electrical/fuel data before sizing or energization |
| HG-07 — Tip-over / fall-event Level 1 safety path | A failed fall path can leave throttle, fuel or ignition active | A6 is statically available as a direct Level 1 input; accepted requirements retain Level 1 shutdown authority | Direct sensor strategy, interface, orientation, threshold, transient behavior, disconnected/short/stuck/frozen behavior, complete shutdown and deliberate restart behavior | Select only a test candidate; define reviewed bench and fault-injection tests covering ETB, injectors, ignition, pump, reset and Level 2 independence | A validated Level 1 fall-event path produces the defined safe state without Level 2 or an unvalidated B5Y IMU communication path | OPEN | Develop a dedicated direct-sensor safety requirement and test method; do not grant the B5Y IMU authority |

## 18. Safe-state proposal

**Status: Proposal**

**Review: Technical Review Required**

For critical loss or fault events where engine shutdown is required, the
current Stage 1 safe-state proposal is:

- remove ETB drive and require the throttle to return to its validated
  mechanical safe position;
- disable injector commands;
- disable ignition commands;
- de-energize the fuel-pump relay;
- retain Level 1 shutdown authority independently of Level 2; and
- require a deliberate, validated recovery/reset condition before restart
  after a fall or shutdown event.

This is not an Accepted safety strategy. Exact detection, timing, sequencing,
diagnostics, power behavior, reset conditions, and handling of every credible
fault remain Unverified and require technical review and physical validation.

## 19. Confirmed findings

**Status: Confirmed**

Confirmed here is limited to the reviewed upstream sources and the static
allocation calculation:

- The pinned connector sources define 34 A, 26 B, 34 C, and 26 D physical
  cavities, totalling 120.
- A5/A15 and A13/A7 provide the upstream TPS1/TPS2 and PPS1/PPS2 analog paths;
  D6/D7 provide DC1 through an upstream TLE9201SG H-bridge path.
- D10/D11 are the physical MAX9924 VR input pair, and the firmware default uses
  `MM100_UART8_TX` from D11 as its first trigger input.
- D24 is physically BUTTON1 even though generated metadata associates it with
  the platform symbol `MM100_IN_CRANK`.
- Pinned connector YAML, platform metadata, and board defaults resolve A6 to
  `MM100_IN_O2S2_ANALOG` / `EFI_ADC_1` / PA1 and A15 to TPS2 /
  `MM100_IN_AUX1_ANALOG` / `EFI_ADC_8` / PB0; the contrary A15/PA1 summary in
  `schematic-notes.md` is an upstream documentation inconsistency.
- C30/`MM100_IGN7` is the firmware-default main-relay output and
  C31/`MM100_OUT_PWM2` is the firmware-default fuel-pump output.
- The reviewed static allocation has capacity for every proposed Stage 1
  function and no blocking physical conflict other than the unused C32
  documentation discrepancy.

These findings do not confirm the delivered hardware revision or any Yamaha
component interface.

## 20. Proposals

**Status: Proposal**

- Use the documented 120-cavity allocation as the working Super uaEFI Stage 1
  hardware baseline.
- Use D10/D11 as the working physical CKP candidate path.
- Use the stated APS, TPS, ETB, sensor, injector, ignition, relay, power,
  interlock, tip-over and CAN cavities for subsequent evidence production.
- Keep Level 1 autonomous from Level 2 CAN and retain all direct throttle,
  fuel, ignition, synchronization, pump and shutdown authority in Level 1.

## 21. Unverified items

**Status: Unverified**

- Delivered ECU revision, build options, condition, waterproofing, connector
  fit, and correspondence to Rev B or Rev C evidence.
- All Yamaha-side connector identities, pinouts, voltages, currents, transfer
  functions, grounding, protection, polarity and compatibility.
- ETB current/thermal margin, APS/TPS plausibility, CKP signal compatibility,
  ignition-driver choice, injector compatibility, and direct tip-over path.
- Main-relay, pump-relay, key, engine-stop, sidestand, neutral and clutch
  electrical interfaces and complete safe-state logic.
- Harness, fuse, power, ground, thermal, EMC, environmental, diagnostic,
  startup, shutdown, recovery and road-use suitability.

## 22. Risks

**Review: Technical Review Required**

- Treating static cavity availability as electrical or safety acceptance.
- Building a harness against the wrong physical hardware revision.
- Energizing unknown ETB, APS/TPS, injector, ignition or Yamaha switch pins.
- Depending on D24 naming rather than its physical BUTTON1 definition and
  thereby misrouting the crank signal.
- Using C32 before its upstream discrepancy is resolved.
- Direct-driving original coils from default logic outputs without verified
  driver architecture.
- Underestimating ETB/injector/relay current, fuse, flyback or thermal demand.
- Giving an unvalidated B5Y IMU or Level 2 CAN hidden shutdown or throttle
  authority.
- Defining recovery, degraded operation or limp-home behavior without a
  reviewed safety analysis and fault-injection evidence.

## 23. Next evidence-producing actions

1. Complete HG-01 by inspecting the delivered ECU and matching its physical
   revision and build population to applicable immutable documentation.
2. Photograph and positively identify every candidate connector before any
   powered characterization.
3. Produce technically reviewed methods for HG-02 and HG-03, including
   current-limited ETB work and redundant-sensor fault testing.
4. Complete the existing original-pickup safety prerequisites and evidence
   path before testing D10/D11 under HG-04.
5. Gather original-coil and physical ECU driver-population evidence for HG-05.
6. Identify the selected injectors and authoritative electrical/fuel data for
   HG-06.
7. Define the independent direct Level 1 fall-sensor requirements and fault
   tests for HG-07 without granting authority to the unvalidated B5Y IMU.
8. Design power, grounding, protection, fusing and relay interfaces only after
   the relevant current and fault evidence exists.
9. Create subsequent bench-test records with explicit preconditions, safe
   loads, stop/recovery criteria, execution status and results. Do not mark a
   gate passed from documentation or power-on evidence alone.

## 24. Conclusion

### Confirmed

The reviewed Super uaEFI source/pinout provides sufficient physical I/O
resources for the proposed XJ900S Stage 1 allocation, and no blocking physical
pin conflict has been identified apart from the isolated C32 upstream
documentation discrepancy, which is not used by Stage 1.

### Proposal

Use the documented cavity allocation as the working Super uaEFI Stage 1
hardware baseline.

### Not accepted

Super uaEFI remains the primary Level 1 ECU candidate and purchased hardware,
but final hardware acceptance remains open until HG-01 through HG-07 and
subsequent bench validation satisfy their pass criteria. No ECU, throttle
body, DBW implementation, ignition system, injector, sensor, wiring strategy,
safe state, or road-use configuration is accepted by this record.

No ADR is created or superseded.

## 25. Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-26 | Created the Super uaEFI Stage 1 static hardware-feasibility and 120-cavity allocation record. | Preserve pinned upstream evidence, proposed project allocation, resource analysis, discrepancies, and remaining hardware/safety gates without accepting hardware. |

## 26. Navigation

[Research index](README.md) | [RESEARCH-0001](RESEARCH-0001-engine-management-platform.md) | [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [RESEARCH-0003](RESEARCH-0003-trigger-and-synchronization-strategy.md) | [RESEARCH-0005](RESEARCH-0005-1997-on-electrical-baseline.md) | [RESEARCH-0006](RESEARCH-0006-intake-and-throttle-body-interface.md) | [COMP-0004](../components/COMP-0004-2023-2024-tracer9-right-switch-dbw-grip.md) | [COMP-0005](../components/COMP-0005-2022-mt10-throttle-body-assembly.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [ADR-0002](../decisions/ADR-0002-three-level-control-architecture.md) | [Test strategy](../testing/test-strategy.md) | [Documentation index](../INDEX.md)
