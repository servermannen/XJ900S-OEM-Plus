# Implementation Roadmap

**Purpose:** Translate the accepted requirements and three-level architecture
into an ordered engineering and validation process.

**Document status: Draft**

This sequence is a planning framework and will evolve as research and component
decisions are completed.

## Roadmap principles

- Work shall proceed in controlled stages with documented entry criteria, work
  products, tests, and exit criteria.
- Dependent work shall not be complete before prerequisite evidence exists.
- Safety-critical systems shall be reviewed and tested before road use; bench
  testing shall precede motorcycle integration where practical.
- Components shall follow requirements and evidence, not convenience alone.
- The motorcycle shall remain recoverable to a known state where practical.
- Documentation, decisions, and evidence shall be maintained throughout.
- Level 3 functions shall not delay the initial reliable implementation.

## Stage overview

| Stage | Objective | Main outputs | Road-use status | Completion state |
| --- | --- | --- | --- | --- |
| 0 | Establish project foundation | Requirements, architecture, ADRs, roadmap | No change authorized | In progress |
| 1 | Validate baseline motorcycle | Baseline record and fault list | Baseline checks only | Not started |
| 2 | Capture requirements and measurements | Verified data and criteria | No modernization road use | Not started |
| 3 | Validate engine-management concept | Accepted concept decisions | No implementation road use | Not started |
| 4 | Validate EFI bench system | Bench evidence and interfaces | Bench only | Not started |
| 5 | Integrate motorcycle EFI | Level 1 system and test evidence | Controlled testing after safety validation | Not started |
| 6 | Integrate Level 2 | Selected body-control functions | After applicable validation | Not started |
| 7 | Add instrumentation and diagnostics | Rider and service information | Must not enable unsafe operation | Not started |
| 8 | Validate reliability and safety | Integrated validation evidence | Progressive, controlled testing | Not started |
| 9 | Refine OEM+ implementation | Production-like packaging and documentation | Within validated scope | Not started |
| 10 | Prepare future interfaces | Level 3 provisions | Not an initial requirement | Not started |

## Stage 0 — Project foundation

**Objective:** Establish repository purpose, principles, requirements,
architecture, decisions, and documentation conventions.

Status: In progress

**Outputs:** README, AGENTS.md, documentation index, accepted requirements,
three-level architecture, ADR-0001, ADR-0002, this roadmap, and the initial
test-strategy framework.

**Exit criteria:** Purpose and conventions are documented; architecture is
recorded; navigation is usable; and no unresolved requirements/architecture
contradiction remains. These criteria have not been declared satisfied.

## Stage 1 — Baseline motorcycle validation

**Objective:** Establish the mechanical, electrical, and operational baseline
before major modernization.

**Work:** Verify starting, charging, fuel delivery, ignition, cooling, and basic
electrical operation; document wiring, modifications, faults, maintenance,
braking, steering, suspension, chassis, dimensions, installation space,
photographs, measurements, and test results.

**Exit criteria:** The baseline and comparison functions are documented;
measurements and sources are retained; and safety-critical defects are either
addressed or explicitly block further work.

Review: Technical Review Required

## Stage 2 — Requirements and measurement capture

**Objective:** Convert open areas into measurable requirements and verified
motorcycle data.

**Work:** Capture engine sensing, fuel system, charging and electrical load,
physical space, intake and throttle measurements, injector and fuel-pressure
requirements, sensor environment, rider controls, instrumentation, diagnostics,
safe states, degraded operation, and legal or inspection considerations.

**Outputs:** Updated requirements, verified measurements, research records,
component evaluation criteria, open questions, and ADRs for accepted decisions.

**Exit criteria:** Required measurements and evaluation criteria are traceable,
with unresolved matters explicitly recorded. No final component is selected by
this roadmap.

## Stage 3 — Engine-management concept validation

**Objective:** Establish that an engine-management approach can meet accepted
requirements before a complete system is built.

**Work:** Evaluate platform capabilities; sensing and synchronization strategy;
ignition and injection channels; pump and fall-event shutdown; cable and
drive-by-wire alternatives; sensing and actuation functions; diagnostics and
logging; capability gaps; and externally handled functions.

**Exit criteria:** Platform and control-strategy ADRs are accepted; inputs,
outputs, synchronization, and shutdown architecture are evidence-based; and
major gaps have accepted mitigations.

Review: Technical Review Required

## Stage 4 — EFI bench system

**Objective:** Build and validate an off-motor engine-management system before
motorcycle installation.

**Work:** Validate protected power, grounding, crank/cam inputs, sensors, safe
injector and ignition test loads, pump logic, fall behavior, startup/shutdown,
diagnostics, fault simulation, and logging.

**Exit criteria:** Inputs, outputs, and faults behave as designed; no unsafe
unintended output is observed; evidence links to requirements; and wiring and
interface records are current.

Review: Technical Review Required

## Stage 5 — Motorcycle EFI integration

**Objective:** Install and validate Level 1 engine management.

**Work:** Integrate mechanics, intake, throttle, fuel, crank/cam sensing where
applicable, sensors, actuators, ignition, protected wiring and grounding, pump
safety, calibration, static tests, controlled first start, idle and low load,
then progressive road load only after prerequisite safety checks.

**Exit criteria:** Engine operation and shutdown are predictable; fuel and
ignition are stable within the test scope; fall shutdown works; safety-critical
faults do not remain before road tests; and calibration, test evidence, and EFI
conversion are documented. Starting alone does not approve road use.

Review: Technical Review Required

## Stage 6 — Level 2 body-control integration

**Objective:** Add selected non-engine functions without compromising Level 1.

**Potential scope:** Rider inputs, lighting, signaling, horn, brake-light logic,
relays, accessories, heated grips, warnings, power management, legacy-circuit
adaptation, and fall-sensor distribution. Initial scope requires a separate ADR.

**Exit criteria:** Level 2 cannot unintentionally command fuel, ignition, or
throttle; Level 1 retains basic operation; safety-supporting behavior is
reviewed; interfaces and diagnostics are documented; and functions are tested
independently and together.

Review: Technical Review Required

This review applies only to safety-influencing Level 2 functions.

## Stage 7 — Instrumentation and diagnostics

**Objective:** Provide useful rider information, fault visibility, and service
diagnostics.

**Work:** Implement required warnings, operating information, fault visibility,
logging, service access, diagnostic interface, plausibility information, and
documented normal/fault indications while separating required warnings from
optional display functions.

**Exit criteria:** Warnings are understandable; diagnostics support practical
troubleshooting; optional display failure does not compromise Level 1; and
service instructions exist.

## Stage 8 — Reliability and safety validation

**Objective:** Validate the integrated motorcycle under realistic conditions.

**Work:** Test electrical load and charging, hot/cold operation, vibration,
connectors, moisture protection, repeated starts/stops, fault injection, fall
sensing, fuel leaks, wiring temperature, brakes and controls, progressive road
operation, post-test condition, and corrective-change retests.

**Exit criteria:** Safety requirements have linked evidence; no unresolved
critical fault remains; findings and corrections are documented; dependable
operation is demonstrated within the validated scope; and reviews are complete.

Review: Technical Review Required

## Stage 9 — OEM+ refinement

**Objective:** Refine packaging, appearance, ergonomics, serviceability, and
documentation after core systems are proven.

**Work:** Refine harness routing, connectors, enclosures, brackets, controls,
instrumentation, service access, labels, diagrams, parts records, maintenance
instructions, and remove temporary test arrangements.

**Exit criteria:** Integration is durable, identifiable, serviceable, and fully
documented. Cosmetic refinement shall not conceal unresolved technical faults.

## Stage 10 — Future-ready interfaces

**Objective:** Document and, where justified, prepare interfaces for Level 3.

**Potential areas:** Wheel speed, ABS coordination, IMU, traction support,
rider modes, suspension, advanced power distribution, expanded networking,
telemetry, and connected instrumentation.

Function status: Proposal

**Exit criteria:** These functions remain outside initial completion; each
requires requirements, research, ADRs, and validation; and no future interface
becomes a hidden Level 1 dependency.

## Decision gates

| Gate | Decision |
| --- | --- |
| A | Baseline motorcycle suitable for modernization |
| B | Measurable requirements and verified dimensions available |
| C | Engine-management platform and sensing strategy accepted |
| D | Bench system safe and functional |
| E | Motorcycle ready for controlled first start |
| F | Ready for controlled road testing |
| G | Level 2 integration accepted |
| H | Reliability and safety validation complete |
| I | Initial OEM+ implementation complete |

No gate is declared passed. Evidence and applicable technical review are
required before approval.

## Dependencies

- Components depend on verified requirements and measurements; road testing
  depends on prerequisite safety validation.
- Level 2 depends on stable Level 1 boundaries; instrumentation shall not
  become an undocumented engine dependency.
- Level 3 depends on stable Level 1 and Level 2 interfaces.
- Cosmetic completion does not replace validation.
- Accepted ADRs shall precede major irreversible decisions.

## Open planning questions

Status: Unverified

- Final project-completion definition; stage ownership and review roles; legal
  and inspection evidence; and detailed gate acceptance criteria.
- Required test equipment; parts-procurement sequence; rideability between
  stages; and EFI backup and rollback strategy.
- Initial Level 2 scope; documentation for future maintainers; and criteria for
  beginning each Level 3 function.

## Navigation

[Documentation index](../INDEX.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Decision register](../decisions/README.md) | [Test strategy](../testing/test-strategy.md)
