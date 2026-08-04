# RESEARCH-0003: Trigger and synchronization strategy

**Purpose:** Establish evidence needed for a later Level 1 crankshaft and camshaft sensing decision without selecting a trigger, sensor, ECU, ignition topology, or donor component.

**Document status: Draft**

Status: Unverified

Review: Technical Review Required

## Research question

What are the verified original ignition, firing-order, and timing-reference characteristics of the 1997 Yamaha XJ900S engine, and which crankshaft and camshaft sensing strategies are mechanically and electrically feasible for reliable aftermarket engine management?

## Scope

Included: the relevant model/engine variant, cylinder and ignition architecture, original pickup/rotor/controller relationship, crank/cam access, trigger packaging, synchronization, signal behavior, serviceability, reversibility, bench testing, and motorcycle measurements.

Excluded: final ECU/rusEFI hardware, sensor, tooth pattern, bracket, machining, coil/igniter, injector strategy, pinout, calibration, implementation, or architecture decision.

## Vehicle identification boundary

- Model: Yamaha XJ900S Diversion.
- Model year: 1997.
- Model designation currently recorded by the project: 4KM.

Every source shall be verified against the relevant engine and model variant. Differences between XJ900S years, regions, XJ900 variants, related engine families, and parts-catalogue supersessions shall not be transferred without explicit evidence.

## Sources

| Source | Type | Accessed | Relevance and limitation |
| --- | --- | --- | --- |
| [Yamaha XJ900S(G) service manual sample, 4KM-28197-20](https://www.aservicemanualpdf.com/Samplepages/SM-1995%20Yamaha%20XJ900S%28G%29%20Service%20Repair%20Manual.pdf) | Online sample/manual-identification source | 2026-08-04 | Identifies the manual; technical findings in this record come from the local complete manual reference, not these sample pages. |
| [Yamaha XJ900S 1998 parts catalogue](https://www.recambios-motos.com/yamaha/pdf/XJ900S%20DIVERSION%201998.pdf) | Yamaha parts-catalogue copy | 2026-08-04 | Adjacent model year only; use to identify questions and supersessions, not to confirm 1997 specification. |
| [Yamaha XJ900S 1995 ignition catalogue](https://www.bike-parts-yam.com/yamaha-motorcycle/900-MOTO/1995/DIVERSION/XJ900S/IGNITION/50_4974-4974/B39/0/30325) | Dealer catalogue presenting Yamaha parts data | 2026-08-04 | Different year; confirms that an ignition catalogue must be checked, not 1997 pairing or geometry. |
| Yamaha XJ900S(G) Service Manual, 4KM-28197-20 | Local ChatGPT project reference | 2026-08-04 | Authoritative for the manual-stated XJ900S 4KM1 (1995); not a confirmed exact service manual for the 1997 project motorcycle. Pages referenced below were analysed but are not copied here. |

The project baseline records the motorcycle as 1997 XJ900S, 4KM. No specific 1997 parts-catalogue URL supporting a year-specific submodel code is recorded here; that exact submodel code remains Unverified. The 1995 4KM1 manual is authoritative for that variant only; 1997 applicability requires 1997 parts data and direct motorcycle inspection.

## Required factual verification

| Fact ID | Question | Finding | Status | Best source | Remaining uncertainty |
| --- | --- | --- | --- | --- | --- |
| TRG-F001 | Engine type and arrangement | Air-cooled four-stroke DOHC, forward-inclined parallel four; 892 cm3. | Confirmed | Manual 2-1, PDF 21. | Confirmed for 4KM1; 1997 applicability unverified. |
| TRG-F002 | Cylinder numbering | #1 through #4 used by manual. | Confirmed | Manual 3-8/3-9. | 1997 applicability unverified. |
| TRG-F003 | Firing order | 1-2-4-3 from documented compression-TDC sequence. | Confirmed | Manual 3-8/3-9. | Confirmed for 4KM1; 1997 applicability unverified. |
| TRG-F004 | Ignition-system type | Digital TCI. | Confirmed | Manual 2-3/2-17. | 1997 applicability unverified. |
| TRG-F005 | Ignitor identification | 4JT051, Mitsubishi. | Confirmed | Manual 2-17. | 1997 applicability unverified. |
| TRG-F006 | Ignition-coil count | Two coils; four plugs shown. | Confirmed | Manual 7-1/7-4. | 1997 applicability unverified. |
| TRG-F007 | Ignition-coil identification | J0312/J0313 Nippondenso; specified resistance and spark gap. | Confirmed | Manual 2-17. | 1997 part continuity unverified. |
| TRG-F008 | Coil-to-cylinder pairing | Indicated 1/4 and 2/3; HT leads not labelled. | Unverified | Manual 3-8/3-9, 7-1/7-4. | Trace 1997 HT leads. |
| TRG-F009 | Wasted-spark architecture | Strongly supported inference, not explicit manual terminology. | Unverified | Manual topology. | Direct 1997 confirmation required. |
| TRG-F010 | Pickup count | One pickup shown. | Confirmed | Manual 7-1/7-4. | 1997 applicability unverified. |
| TRG-F011 | Pickup electrical specification | 446-545 ohms at 20 C; White/Red and White/Green. | Confirmed | Manual 2-17. | 1997 applicability unverified. |
| TRG-F012 | Pickup sensor technology | Two-wire coil consistent with passive/VR, not explicitly classified. | Unverified | Manual 2-17. | Documentation or waveform required. |
| TRG-F013 | Pickup and timing-plate location | Behind timing-plate cover; plate, bolt, pin, and base identified. | Confirmed | Manual 3-19, 4-10/4-68. | 1997 applicability unverified. |
| TRG-F014 | Trigger geometry | Events, features, index, angle, polarity, amplitude, gap, runout, pulse width, decoder compatibility unknown. | Unverified | Manual illustrations insufficient. | Direct measurement. |
| TRG-F015 | Initial ignition timing | 5 degrees BTDC at 1,000 rpm. | Confirmed | Manual 2-3. | 1997 applicability unverified. |
| TRG-F016 | Advanced ignition timing | 40 degrees BTDC at 5,000 rpm; electrical advance uses speed/throttle. | Confirmed | Manual 2-3/2-17. | 1997 applicability unverified. |
| TRG-F017 | Cam-position input | No cam-position sensor, cam-position input, or dedicated sensor provision is shown in the reviewed wiring and camshaft sections for the manual-stated 4KM1. | Confirmed | Manual 7-1/7-4 and 4-72 to 4-78. | Applicability to the 1997 project motorcycle remains Unverified. |
| TRG-F018 | Camshaft and sprocket arrangement | Two chain-driven cams and sprockets. | Confirmed | Manual 4-72 to 4-78. | 1997 applicability unverified. |
| TRG-F019 | Existing timing marks | #1 compression TDC lobes apart; crank mark aligns with pointer. | Confirmed | Manual 4-6. | 1997 applicability unverified. |
| TRG-F020 | Crankshaft-access opportunities | Timing-plate location evidenced; generator/internal locations unmeasured. | Unverified | Manual 3-19/4-10/4-68. | 1997 packaging/relationship. |
| TRG-F021 | Camshaft-access opportunities | The manual procedure requires removal of the cylinder-head cover and surrounding components; no dedicated factory cam-sensor provision is shown in the reviewed sections. | Confirmed | Manual 4-72 to 4-78. | 1997 packaging and direct physical inspection remain Unverified. |

## Original ignition architecture and phase implications

For 1995 4KM1, the manual documents digital TCI, one ignitor, one pickup, two coils, and four plugs. Initial timing is 5 degrees BTDC at 1,000 rpm and specified advance is 40 degrees BTDC at 5,000 rpm; the advance graph uses speed and throttle opening. Coil primary resistance is 1.87-2.53 ohms, secondary resistance is 12-18 kohms, minimum spark-gap test is 6 mm, and pickup resistance is 446-545 ohms at 20 C. Do not infer EFI suitability from original operation.

**Status:** Unverified

The combination of one crank pickup, no documented cam-position input, two ignition coils, and four spark plugs strongly supports a wasted-spark architecture. The service-manual material reviewed does not explicitly use the term "wasted spark", so direct confirmation from the 1997 wiring arrangement or motorcycle inspection remains required.

**Status:** Unverified

The verified firing order and conventional paired-TDC relationship strongly indicate ignition pairs 1/4 and 2/3. The reviewed circuit diagram does not label the high-tension leads by cylinder. The actual coil-to-cylinder connections shall be traced on the motorcycle before the pairing is marked Confirmed.

**Status:** Unverified

The manual confirms a two-wire pickup coil with a specified winding resistance. This is consistent with a passive magnetic or variable-reluctance pickup, but the reviewed pages do not explicitly classify the sensor technology. Final classification requires component documentation or waveform measurement.

The 1-2-4-3 firing order is confirmed for the manual-stated 4KM1 variant. The exact coil pairing on the 1997 motorcycle and the resulting phase-related implementation conclusions remain unverified pending direct inspection. Crank angle alone may not establish 720-degree phase; a cam signal can establish it where its fixed phase relationship is verified.

## Existing crank-trigger assessment

| Potential role | Supporting evidence | Evidence against or missing | Required test | Preliminary status |
| --- | --- | --- | --- | --- |
| RPM-only input | One pickup coil and its timing-plate location are documented for the manual-stated 4KM1. | Geometry, waveform, resolution, signal conditioning, and 1997 applicability unresolved. | Inspect and capture waveform. | Unverified |
| Basic ignition reference | Original controller relationship requires verification. | Timing resolution and index unknown. | Correlate waveform to crank angle. | Unverified |
| Cranking synchronization | None. | Cranking amplitude and decoder behavior unknown. | Cranking capture and bench simulation. | Unverified |
| Full angular input | None. | Events, unique index, resolution, and runout unknown. | Rotor inspection and angular measurement. | Unverified |
| Backup/secondary input | None. | Interface and independence unknown. | Architecture review. | Proposal |
| Unsuitable without replacement | None. | Cannot conclude before evidence. | Complete above checks. | Unverified |

Assess events/revolution, resolution, unique index, speed range, amplitude, polarity, noise, direction ambiguity, air gap, runout, conditioning, and candidate-decoder compatibility. Exact electrical values remain unverified without manual, datasheet, or direct measurement.

## Candidate sensing locations

| Location ID | Location | Relationship, packaging, and access | Modification/reversibility | Evidence status | Required measurement |
| --- | --- | --- | --- | --- | --- |
| CRK-LOC-01 | Existing pickup/timing plate behind timing-plate cover | Physical location/service access confirmed for 4KM1; applicability and physical continuity on the 1997 project motorcycle require direct inspection. Best-evidenced first location to inspect. | Suitability for modern EFI unverified. | Unverified | Photograph, identify, measure waveform/geometry. |
| CRK-LOC-02 | Generator/rotor area | AC generator is a separate removable assembly; drive relationship, backlash, and direct crank-angle suitability are unverified. Do not assume direct crank mounting. | Unverified. | Unverified | Relationship, backlash, diameters, clearance. |
| CRK-LOC-03 | Starter clutch/internal crank | Requires substantially more disassembly and has poorer serviceability evidence than timing plate. | Unverified. | Unverified | Relationship, runout, access. |
| CRK-LOC-04 | External wheel or replacement internal rotor | Packaging, retention, and sealing unverified. | Potentially high; reversibility unverified. | Proposal | Space, retention, runout. |
| CAM-LOC-01 | Intake/exhaust cam end or sprocket | Two chain-driven cams/sprockets provide valid 1:2 relationship for 4KM1; no factory sensor provision shown. | Added target may require cover/head modification. | Unverified | Cover/head space, oil, heat, air gap, service access. |
| CAM-LOC-02 | Cam-driven component or external target | Fixed 1:2 relationship required; no factory provision confirmed. | Unverified. | Unverified | Relationship, target access, service impact. |
| CAM-LOC-03 | Internal target or cover/head modification | May be required; sealing, temperature, air gap, fabrication, debris, and access unverified. | Potentially high; reversibility unverified. | Proposal | Modification, debris, sealing, access. |

A convenient rotating component is not a valid crank or cam reference until its rotational relationship, space, and mounting are verified.

## Trigger-strategy candidates

| Strategy | Crank modification | Cam modification | 720-degree phase | Sequential potential | Ignition potential | Complexity/serviceability/reversibility | Evidence maturity | Preliminary status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| STRAT-01 Retain original crank pickup only | No/Unverified | No | Unverified | Conditional | Conditional | Low/Unverified/High | Low | Unverified |
| STRAT-02 Enhanced crank, no cam | Yes | No | No or Conditional | Conditional | Conditional | Medium/Unverified/Medium | Low | Proposal |
| STRAT-03 Enhanced crank plus cam | Yes | Yes | Yes | Yes | Yes | High/Unverified/Medium | Low | Proposal |
| STRAT-04 Original crank plus cam | Unverified | Yes | Conditional | Conditional | Conditional | Medium/Unverified/Medium | Low | Proposal |
| STRAT-05 Replacement crank plus retained pickup | Yes | Optional | Conditional | Conditional | Conditional | High/Unverified/Medium | Low | Proposal |

STRAT-01 must be assessed for resolution, phase ambiguity, decoder support, starting robustness, timing accuracy, and diagnostics. STRAT-04 depends on original-crank resolution and reliable synchronization. No strategy is accepted.

## Sensor and trigger-pattern considerations

Variable-reluctance sensing requires assessment of passive operation, speed-dependent amplitude, polarity, cranking performance, air gap, zero-crossing conditioning, noise, shielding, and ECU compatibility. Hall-effect sensing requires assessment of supply, digital output, target, pull-up/output type, cranking consistency, environment, fault behavior, and ECU compatibility. Magnetoresistive or other active sensing is Status: Unverified and needs specific evidence.

Consider single-event, evenly spaced, missing-tooth, unique-index, and crank-plus-cam patterns; tooth/gap geometry, edge, direction, cranking quality, maximum speed, concentricity, runout, material, air gap, decoder support, startup, and resynchronization. Complexity shall be justified by control and diagnostic need, not tooth count.

## Mechanical, electrical, and fault criteria

No interference; maximum-speed retention; controlled runout and air gap; heat/oil/vibration/debris protection; fastener retention; serviceability; replaceability; reversibility; lubrication/sealing preservation; and documented true crank/cam reference are required.

Correct supply, ground/reference, shielding, ignition-noise separation, input protection, polarity, amplitude, thresholds, hysteresis, filtering, timeout, missing/implausible/stale detection, startup state, diagnostics, logging, connectors, moisture, and vibration must be assessed. Final thresholds are unverified.

Review: Technical Review Required

Synchronization-delay, unknown-phase behavior, temporary crank/cam loss, degraded cam-loss operation, immediate crank-loss shutdown, resynchronization, false-edge rejection, stop detection, reverse rotation, fault storage, post-safety-shutdown restart, and power-interruption recovery are Status: Unverified. Do not define limp-home behavior without accepted safety analysis.

## Required motorcycle inspection and measurements

- Photograph coils, wiring, pickup, connector, covers, valve cover, head ends, timing marks, and accessible rotating parts; record visible coil, pickup, and controller part numbers and cylinder pairings.
- Verify pickup-to-controller wiring; measure resistance only with an accepted safe procedure.
- Measure crank/cam space, diameters, holes, air gap, cover clearance, mounting access, oil exposure, target options, and service consequences.
- Capture the original pickup during cranking and, if safe, idle; record amplitude, polarity, frequency, noise, reference conditions, probe/grounding method, and crank-angle correlation where possible.
- Do not connect measuring equipment without a reviewed safe measurement plan.

Review: Technical Review Required

## Required source research and evidence gaps

Obtain the correct Yamaha service manual, wiring diagram, ignition troubleshooting, timing/valve-timing section, and parts diagrams for crank, generator, pickup, cam, head, and valve cover; then cross-reference OEM part numbers, bulletins, and reliable original-part photographs. Consult ECU decoder documentation only after original trigger facts are established.

Gaps: 1997 applicability, coil pairing, pickup geometry/waveform/angle, cam and crank packaging/dimensions/exposure, trigger requirements, synchronization criteria, conditioning, decoder compatibility, degraded-operation policy, fabrication method, and validation procedure.

## Preliminary conclusion

For the manual-stated 1995 4KM1 engine, the service manual documents a digital
TCI system with one pickup coil, two ignition coils, and four spark plugs. The
documented compression-TDC sequence establishes a 1-2-4-3 firing order for that
variant. This topology strongly supports wasted-spark operation, but
applicability and exact coil-to-cylinder wiring shall be verified on the 1997
project motorcycle before confirmation.

The existing pickup and timing-plate location is the best-evidenced first crank-reference location for physical inspection and waveform characterization. Its geometry, angular resolution, cranking behavior, and EFI suitability remain unverified.

The current research shall compare preservation of the original crank reference, an enhanced or replacement crank trigger, and addition of a cam-phase signal. No future trigger strategy, added sensor technology, future ignition topology, or cam-sensor installation location is accepted by this research record.

## Decision impact

- Related research: [RESEARCH-0001](RESEARCH-0001-engine-management-platform.md) and [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md).
- Related requirements: SYS-007 through SYS-009; applicable SAF, REL, SRV, ARC, and DEV.
- Related architecture: Level 1; related roadmap stages: Stage 2, Stage 3, and Stage 4.
- ADR required: Yes. Component evaluation required: Yes, after candidates exist. Bench testing required: Yes. Motorcycle measurements required: Yes.
- Recommended next action: 1. Verify motorcycle model code and engine number. 2. Trace both coils to spark-plug cylinders. 3. Photograph and measure timing plate, pickup, clearance, and mounting. 4. Develop a technically reviewed measurement plan. 5. Capture pickup waveform during cranking and idle. 6. Correlate events with TDC/firing marks. 7. Inspect and measure cam-end and cam-sprocket locations.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-04 | Created initial research record. | Define evidence required for later trigger and synchronization decisions. |

## Navigation

[Research index](README.md) | [RESEARCH-0001](RESEARCH-0001-engine-management-platform.md) | [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [Documentation index](../INDEX.md)
