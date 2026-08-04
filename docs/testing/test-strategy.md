# Test Strategy

**Purpose:** Define project-level verification and validation and connect
requirements, architecture, stages, safety review, and evidence.

**Document status: Draft**

Detailed procedures, limits, equipment, and results remain incomplete.

## Verification and validation principles

**Status: Accepted**

- Every accepted requirement shall identify a verification method and linked
  evidence. Power-on or brief operation alone is not validation.
- Testing progresses from isolated, low-hazard inspection and bench work toward
  integrated road operation. Safety-critical changes require prior review.
- Expected results, criteria, scope, and limitations shall precede formal tests.
- Failures and unexpected behavior remain recorded; corrective changes require
  appropriate regression testing.
- Assumptions are not evidence. Intended operation and credible failures shall
  be tested where practical. Level 3 is not required for Level 1 validation.

## Terminology

- **Verification:** evidence that an item satisfies a specified requirement.
- **Validation:** evidence of suitability for intended use within tested scope.
- **Inspection:** review of documents, construction, dimensions, installation,
  routing, labels, or visible condition.
- **Analysis:** engineering reasoning, calculation, comparison, or evidence review.
- **Bench test:** controlled isolated, simulated, safe-load, or stationary test.
- **Functional test:** confirmation of expected behavior under defined conditions.
- **Fault-injection test:** deliberate fault simulation to test detection,
  containment, safe state, diagnostics, and recovery.
- **Regression test:** repetition after change to protect prior behavior.
- **Road test:** controlled operation after prerequisite evidence and review.
- **Technical review:** documented safety engineering review of design, method,
  evidence, results, and risk.

## Evidence model

`Requirement -> Architecture or decision -> Implementation -> Test case -> Test result -> Review status`

Formal tests require unique IDs and identified configurations. Evidence is
stored or referenced in the repository and may include photos, measurements,
logs, calibration files, diagrams, and instrument output. Source, date, tester,
and configuration are recorded where practical. Repeats retain individual
results; failures remain in the record; acceptance uses all applicable evidence.

## Requirement verification methods

| Method | Purpose | Typical evidence | Appropriate use | Limitation |
| --- | --- | --- | --- | --- |
| Documentation/traceability review | Check records and links | Review record, matrix | Requirements and decisions | Does not prove operation |
| Architecture/engineering review | Evaluate design and reasoning | Analysis, review notes | Boundaries and feasibility | Depends on inputs |
| Design/visual/dimensional inspection | Check implementation | Photos, measurements | Construction and installation | Limited dynamic evidence |
| Electrical test | Check electrical behavior | Readings and logs | Power, grounding, protection | Scope-specific |
| Bench/functional/stationary test | Check controlled behavior | Test record and logs | Inputs, outputs, sequences | Not road validation |
| Fault-injection test | Check failure behavior | Fault/result record | Containment and recovery | Must control hazards |
| Controlled first-start/progressive road test | Validate integration | Logs and observations | Approved progression | Covers only tested range |
| Post-test inspection | Find test effects | Inspection record | After operation | May not reveal latent faults |
| Technical review | Assess safety evidence | Signed review record | Safety progression | Does not replace testing |

## Verification by requirement category

| Category | Typical methods |
| --- | --- |
| SYS | Documentation, architecture, design inspection, integrated functional test |
| SAF | Architecture, electrical, functional, fault injection, technical review, controlled road test |
| REL | Design inspection, environmental/electrical checks, repeated operation, post-test inspection, road test |
| SRV | Design inspection, maintenance walkthrough, diagnostic demonstration, documentation review |
| ARC | Architecture/interface review, bench test, fault injection, independence testing |
| DEV | Traceability, stage-gate, test-record, and configuration review |
| DOC | Documentation, link, traceability, and decision-history review |

Review: Technical Review Required

This label applies to SAF verification. Each requirement's specified method
remains controlling unless changed by an accepted update.

## Verification by implementation stage

| Stage | Verification focus | Minimum evidence before exit | Road operation permitted |
| --- | --- | --- | --- |
| 0 | Repository, requirements, architecture, ADRs, links | Consistency review | No modification authorized |
| 1 | Baseline condition, safety systems, faults | Baseline and safety record | Only within known condition and assessment |
| 2 | Measurements, open requirements, evaluation data | Verified measurement record | No modernization-dependent road test |
| 3 | Capability, sensing, I/O, shutdown, gaps | Accepted concept evidence | No EFI road test |
| 4 | Protected power, I/O, sequences, faults, diagnostics | Bench records | Bench only |
| 5 | Level 1, first start, control and shutdown | Static/bench evidence and Gate F approval | After safety prerequisites |
| 6 | Level 2 independence and interfaces | Independence and review evidence | Within validated Level 1 scope |
| 7 | Warnings, diagnostics, display independence | Rider/service evidence | Within existing validated scope |
| 8 | Reliability, safety, environment, faults | Integrated evidence and reviews | Progressive approved operation |
| 9 | Routing, mounting, identification, service access | Final inspection and records | Within validated scope |
| 10 | Optional interfaces and independence | Interface evidence | No Level 3 approval from preparation alone |

No stage or gate is marked complete.

## Three-level architecture testing

### Level 1

Test crank/cam inputs where used, synchronization, plausibility, injection,
ignition, pump shutdown, starting, idle where used, state transitions, fall
shutdown, faults, diagnostics, safe responses, and drive-by-wire only if later
selected. Use safe loads and simulated inputs before installed critical outputs
where practical.

Review: Technical Review Required

### Level 2

Test rider inputs, lighting, brake light, horn, relays, accessories, heated grips
where used, warnings, power management, fall-signal distribution, Level 1
interfaces, sequences, recovery, and failure independence. A Level 2 fault shall
not command fuel, ignition, or throttle.

Review: Technical Review Required

This applies only to safety-influencing Level 2 functions.

### Level 3

Function status: Proposal

Future functions need separate test plans. Their absence, failure, invalid data,
or shutdown shall not compromise Level 1 unless later accepted. Interface
preparation is not validation, and initial Level 1 validation is independent.

## Safety-critical verification

Braking, throttle, fuel, ignition, shutdown, fall response, electrical
protection, warnings, and authority boundaries require defined preconditions,
hazards, protective measures, safe state, criteria, stop conditions, recovery,
configuration, and review status. Informal observation is insufficient.

Review: Technical Review Required

## Bench testing

Progress through documentation/wiring review, continuity and isolation,
unpowered inspection, current-limited initial power where applicable, power and
ground verification, input simulation, safe-load output tests, combined tests,
startup/shutdown, fault injection, repetition, and post-test inspection.
Hazardous outputs are inhibited, disconnected, fused, or replaced by safe loads
where practical; no ratings are prescribed here.

## Motorcycle integration testing

Progress through installation, grounding/protection, plausibility, actuator
isolation, key-on/engine-off, cranking without fuel or ignition where practical,
controlled critical-function enablement, first start, stationary idle,
temperature/leak inspection, repeated starts/stops, low load, post-test
inspection, then approved road testing. Deviations need justification and safety
review where applicable.

## Fault-injection testing

Potential faults include open/short circuits, implausible or stale data,
missing/delayed communication, controller reset, power interruption, ground
disturbance, unavailable optional systems, fall activation, and unexpected
startup/shutdown. Record injected condition, detection, output, safe state,
diagnostic, recovery/reset, actual result, and follow-up. Never knowingly create
uncontrolled mechanical, fuel, ignition, thermal, or electrical risk.

## Road-test progression

### Road-test prerequisite review

Require passed in-scope static/bench tests; no unresolved safety fault;
inspection of brakes, steering, suspension, wheels, tires, controls, fuel, and
electrics; available shutdown; defined route/scope, logging, and stop conditions;
and completed applicable review.

### Progressive phases

1. Stationary operation.
2. Restricted-area movement.
3. Very low-load operation.
4. Short low-risk route.
5. Progressive load and duration.
6. Repeated hot/cold operation where applicable.
7. Wider range only after review.

Unexpected safety conditions stop progression. Passing one phase does not
approve the next. Evidence records the tested range; untested operation is not
validated.

Review: Technical Review Required

## Regression testing

Scope follows changed functions, affected interfaces, shared power/grounding or
communication, safety dependencies, prior failures, calibration/configuration,
installation, and software changes. Shared-power Level 2 changes retest Level 1
sequences; sensor changes retest plausibility and operation; harness changes
retest inspection and affected functions; corrected failures and related prior
behavior are retested. Documentation-only changes do not universally require a
full regression.

## Test records and traceability

Use future IDs `TEST-<DOMAIN>-<NUMBER>` with domains such as `SYS`, `SAF`,
`REL`, `SRV`, `ARC`, `EFI`, `ELEC`, `BODY`, `DIAG`, and `ROAD`.

Records contain ID, title, purpose, requirements, ADRs/architecture, configuration,
preconditions, equipment, precautions, procedure, expected/actual results,
evidence, classification, deviations, defects/actions, tester, date, and review.
No individual test records are created by this strategy.

## Test-result classification

- **Pass:** all applicable criteria met within documented scope.
- **Fail:** one or more applicable criteria not met.
- **Inconclusive:** evidence supports neither pass nor fail.
- **Blocked:** prerequisites, configuration, equipment, safety, or decisions prevent execution.
- **Not run:** defined but not executed.

A partial success is not Pass when any applicable criterion failed or was not evaluated.

## Technical review

Review considers requirements, architecture/authority, hazards/safe states,
method, configuration, criteria, results/anomalies, evidence, limitations,
additional tests, and stage progression. Review and testing do not replace one
another. Scope and configuration are identified; changes may require reassessment.
`Review: Technically Reviewed` follows only a documented review.

## Test interruption and rollback

Stop for fuel leakage; smoke/heat; unexpected acceleration; throttle or braking
loss; uncommanded output; repeated resets; unexplained protection activation;
unsafe motion; lost shutdown; incorrect safety warnings; or unacceptable risk.

After interruption: establish a safe state; control power, fuel, ignition, and
mechanical hazards; record configuration/behavior; investigate; review action;
identify regression tests; and resume only after prerequisites return. Rollback
planning is especially important for EFI and shared power/control changes.

## Open test-strategy questions

Status: Unverified

- Electrical limits and measurement accuracy; equipment list; environmental,
  vibration, and moisture methods; and formal hazard-analysis method.
- Braking and throttle validation; fuel pressure/leak criteria; ignition safe
  methods; charging and temperature limits; logging rates and retention.
- Road-test risk controls; reviewer qualifications; record storage; calibration
  versioning; full-project validation; and legal/inspection evidence.

## Navigation

[Documentation index](../INDEX.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Implementation roadmap](../implementation/roadmap.md) | [Decision register](../decisions/README.md)
