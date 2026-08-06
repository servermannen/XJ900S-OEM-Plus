# System Requirements

**Purpose:** Define the established system-level requirements for the XJ900S
OEM+ project and provide a traceable basis for later design, implementation,
and testing work.

**Document status: Draft**

## Requirement conventions

Each requirement has a stable identifier, an information status, a rationale,
and a verification method. `Status: Accepted` identifies an established project
requirement; it does not claim that an implementation has been validated.

`Review: Technical Review Required` is separate from information status and is
used only for safety-critical requirements that require later technical
validation.

## System and project requirements

### SYS-001

Requirement ID: SYS-001
Requirement: The project shall develop the 1997 Yamaha XJ900S Diversion according to the Diversion 2027 vision.
Status: Accepted
Rationale: Establishes the accepted project vision.
Verification method: Documentation review.

### SYS-002

Requirement ID: SYS-002
Requirement: The finished motorcycle shall retain the recognizable identity and original character of the XJ900S.
Status: Accepted
Rationale: Preserves the model identity defined by the project vision.
Verification method: Design inspection.

### SYS-003

Requirement ID: SYS-003
Requirement: New systems shall be integrated according to an OEM+ approach rather than appearing as unrelated aftermarket additions.
Status: Accepted
Rationale: Applies the accepted OEM+ project principle.
Verification method: Design inspection.

### SYS-004

Requirement ID: SYS-004
Requirement: The project shall be implemented in controlled stages.
Status: Accepted
Rationale: Reduces development risk through staged implementation.
Verification method: Documentation review.

### SYS-005

Requirement ID: SYS-005
Requirement: Each stage shall be validated before dependent stages are considered complete.
Status: Accepted
Rationale: Requires evidence before dependent work is accepted.
Verification method: Traceability review.

### SYS-006

Requirement ID: SYS-006
Requirement: Reliability, safety, and serviceability shall take priority over novelty, maximum complexity, or unnecessary feature count.
Status: Accepted
Rationale: Applies the accepted project priorities to all system decisions.
Verification method: Documentation review.

## Functional modernization requirements

### SYS-007

Requirement ID: SYS-007
Requirement: The motorcycle shall be converted from carburetion to electronically controlled fuel injection.
Status: Accepted
Rationale: Establishes electronically controlled fuel injection as an accepted project objective.
Verification method: Architecture review.
Review: Technical Review Required

### SYS-008

Requirement ID: SYS-008
Requirement: The engine-management system shall provide the functions required for fuel delivery and ignition control.
Status: Accepted
Rationale: Defines the required engine-management function without selecting an implementation.
Verification method: Functional test.
Review: Technical Review Required

### SYS-009

Requirement ID: SYS-009
Requirement: The engine-management design shall include the sensing and actuation functions required to control fuel delivery, ignition, engine state, and applicable safety functions.
Status: Accepted
Rationale: Supports reliable engine operation without prescribing component choices.
Verification method: Architecture review.
Review: Technical Review Required

### SYS-010

Requirement ID: SYS-010
Requirement: The electrical architecture shall support modern controls, lighting, instrumentation, safety functions, and engine management.
Status: Accepted
Rationale: Defines the system-level electrical modernization scope.
Verification method: Architecture review.

### SYS-011

Requirement ID: SYS-011
Requirement: Modernized systems shall operate as an integrated motorcycle-level system rather than as isolated modifications.
Status: Accepted
Rationale: Supports coherent OEM+ integration.
Verification method: Architecture review.

### SYS-012

Requirement ID: SYS-012
Requirement: The architecture shall allow future expansion without requiring the initial implementation to include every possible future feature.
Status: Accepted
Rationale: Preserves staged development and avoids unnecessary initial complexity.
Verification method: Architecture review.

### SYS-013

Requirement ID: SYS-013
Requirement: The Level 1 engine-management system shall use a crankshaft-position input for engine-speed determination and synchronization.
Status: Accepted
Rationale: Records the accepted need for crankshaft sensing without selecting a sensor, trigger pattern, location, conditioning, decoder, or final implementation.
Verification method: Architecture review and functional test.
Review: Technical Review Required

### SYS-014

Requirement ID: SYS-014
Requirement: The project shall retain the original field-regulated generator architecture unless measured evidence supports a superseding ADR.
Status: Accepted
Rationale: Implements ADR-0003 while preserving an evidence-based reopening path.
Verification method: Documentation review.
Review: Technical Review Required

## Safety requirements

### SAF-001

Requirement ID: SAF-001
Requirement: Following a detected fall or tip-over event, the motorcycle shall stop engine operation and fuel delivery and shall require a deliberate reset or restart action before engine operation can resume.
Status: Accepted
Rationale: Addresses the accepted safety need for a detected fall or tip-over event.
Verification method: Functional test.
Review: Technical Review Required

### SAF-002

Requirement ID: SAF-002
Requirement: A failure in a nonessential convenience function shall not cause loss of a safety-critical motorcycle function.
Status: Accepted
Rationale: Limits the safety impact of nonessential-function failures.
Verification method: Fault-injection test.
Review: Technical Review Required

### SAF-003

Requirement ID: SAF-003
Requirement: Safety-critical functions shall use defined safe states where technically applicable.
Status: Accepted
Rationale: Requires deliberate handling of safety-critical failures.
Verification method: Architecture review.
Review: Technical Review Required

### SAF-004

Requirement ID: SAF-004
Requirement: Braking, throttle control, fuel delivery, ignition, and electrical protection shall require documented technical review and validation.
Status: Accepted
Rationale: Identifies the systems that require safety-focused technical evidence.
Verification method: Traceability review.
Review: Technical Review Required

### SAF-005

Requirement ID: SAF-005
Requirement: Modifications shall not knowingly reduce the motorcycle's braking capability, controllability, or operational safety.
Status: Accepted
Rationale: Preserves the project's safety priority during modification work.
Verification method: Road test after prerequisite safety validation.
Review: Technical Review Required

### SAF-006

Requirement ID: SAF-006
Requirement: Electrical circuits shall be appropriately protected against overcurrent and foreseeable wiring faults.
Status: Accepted
Rationale: Addresses electrical protection as a safety-critical requirement.
Verification method: Electrical test.
Review: Technical Review Required

### SAF-007

Requirement ID: SAF-007
Requirement: Safety-related faults shall be diagnosable to a practical extent.
Status: Accepted
Rationale: Supports practical identification of safety-related faults.
Verification method: Functional test.
Review: Technical Review Required

### SAF-008

Requirement ID: SAF-008
Requirement: The project shall include a fall or tip-over sensor whose valid activation causes Level 1 fuel-pump, injector, and ignition shutdown and requires deliberate reset or restart behavior.
Status: Accepted
Rationale: Records the accepted sensor requirement and Level 1 shutdown authority without selecting the sensor or its implementation.
The exact reset sequence, state conditions, timing, missing-signal behavior,
and restart interlocks remain Unverified and require a later accepted safety
strategy.
Verification method: Functional and fault-injection test.
Review: Technical Review Required

## Reliability requirements

### REL-001

Requirement ID: REL-001
Requirement: The motorcycle shall remain suitable for dependable road use.
Status: Accepted
Rationale: Applies the project reliability priority to the completed motorcycle.
Verification method: Road test after prerequisite safety validation.

### REL-002

Requirement ID: REL-002
Requirement: Systems and components shall be selected and designed for the environmental conditions expected on a motorcycle, including vibration, moisture, temperature variation, and electrical disturbances.
Status: Accepted
Rationale: Addresses the operating conditions relevant to dependable motorcycle use.
Verification method: Design inspection.
Review: Technical Review Required

### REL-003

Requirement ID: REL-003
Requirement: The design shall avoid unnecessary single points of failure where a practical alternative exists.
Status: Accepted
Rationale: Improves fault tolerance where practical.
Verification method: Architecture review.

### REL-004

Requirement ID: REL-004
Requirement: Proven production components shall be preferred where they meet the requirements.
Status: Accepted
Rationale: Applies the accepted preference for proven production components.
Verification method: Documentation review.

### REL-005

Requirement ID: REL-005
Requirement: Custom development shall be used only where it provides clear technical or integration value.
Status: Accepted
Rationale: Limits custom development to cases with documented value.
Verification method: Design inspection.

### REL-006

Requirement ID: REL-006
Requirement: Connections, wiring, mounting, and enclosure methods shall be suitable for long-term motorcycle use.
Status: Accepted
Rationale: Supports durable integration in the motorcycle environment.
Verification method: Visual inspection.
Review: Technical Review Required

## Serviceability requirements

### SRV-001

Requirement ID: SRV-001
Requirement: Routine maintenance and fault diagnosis shall remain practical.
Status: Accepted
Rationale: Applies the project serviceability priority.
Verification method: Design inspection.

### SRV-002

Requirement ID: SRV-002
Requirement: Components requiring maintenance or replacement shall remain reasonably accessible.
Status: Accepted
Rationale: Supports practical service work.
Verification method: Visual inspection.

### SRV-003

Requirement ID: SRV-003
Requirement: Wiring, connectors, fuses, relays, controllers, sensors, and interfaces shall be identifiable in the project documentation.
Status: Accepted
Rationale: Supports fault diagnosis and maintenance.
Verification method: Documentation review.

### SRV-004

Requirement ID: SRV-004
Requirement: The design shall use replaceable and obtainable components where practical.
Status: Accepted
Rationale: Supports long-term maintenance and repair.
Verification method: Documentation review.

### SRV-005

Requirement ID: SRV-005
Requirement: Diagnostic information shall be accessible without requiring unnecessary disassembly.
Status: Accepted
Rationale: Supports efficient fault diagnosis.
Verification method: Design inspection.

### SRV-006

Requirement ID: SRV-006
Requirement: Modifications shall be reversible or repairable where reasonably practical.
Status: Accepted
Rationale: Preserves practical repair options.
Verification method: Design inspection.

### SRV-007

Requirement ID: SRV-007
Requirement: The motorcycle shall not depend on undocumented one-off knowledge for normal maintenance or troubleshooting.
Status: Accepted
Rationale: Ensures maintenance knowledge is retained in project records.
Verification method: Documentation review.

## Architecture and integration requirements

### ARC-001

Requirement ID: ARC-001
Requirement: Engine-critical control functions shall reside in the engine-management system.
Status: Accepted
Rationale: Establishes a clear boundary for engine-critical control.
Verification method: Architecture review.
Review: Technical Review Required

### ARC-002

Requirement ID: ARC-002
Requirement: Non-engine body-control functions may be handled by a separate control unit where this improves modularity, reliability, or serviceability.
Status: Accepted
Rationale: Allows modular separation when it provides project value.
Verification method: Architecture review.

### ARC-003

Requirement ID: ARC-003
Requirement: Future systems shall be isolated from engine-critical control unless an approved interface requires interaction.
Status: Accepted
Rationale: Reduces unintended influence on engine-critical control.
Verification method: Architecture review.
Review: Technical Review Required

### ARC-004

Requirement ID: ARC-004
Requirement: Interfaces between control units shall be documented.
Status: Accepted
Rationale: Supports integration, diagnosis, and future change control.
Verification method: Documentation review.

### ARC-005

Requirement ID: ARC-005
Requirement: The architecture shall separate mandatory initial functions from optional and future functions.
Status: Accepted
Rationale: Supports staged implementation and controlled scope.
Verification method: Architecture review.

### ARC-006

Requirement ID: ARC-006
Requirement: Failure of an optional future subsystem shall not prevent basic engine operation unless explicitly required by an accepted safety architecture.
Status: Accepted
Rationale: Protects basic operation from unrelated optional-subsystem failures.
Verification method: Fault-injection test.
Review: Technical Review Required

### ARC-007

Requirement ID: ARC-007
Requirement: The system shall support modular testing of major subsystems before complete motorcycle integration.
Status: Accepted
Rationale: Enables staged validation before vehicle-level integration.
Verification method: Architecture review.

### ARC-008

Requirement ID: ARC-008
Requirement: Electrical and logical interfaces shall be designed to reduce unintended coupling between subsystems.
Status: Accepted
Rationale: Supports modularity and limits unintended interactions.
Verification method: Architecture review.
Review: Technical Review Required

## Development and validation requirements

### DEV-001

Requirement ID: DEV-001
Requirement: Development shall proceed through defined stages with documented entry and exit criteria.
Status: Accepted
Rationale: Provides controlled progress and objective stage completion.
Verification method: Documentation review.

### DEV-002

Requirement ID: DEV-002
Requirement: Safety-critical changes shall be tested before road use.
Status: Accepted
Rationale: Requires prior safety evidence before road exposure.
Verification method: Traceability review.
Review: Technical Review Required

### DEV-003

Requirement ID: DEV-003
Requirement: Subsystems shall be bench-tested where practical before installation.
Status: Accepted
Rationale: Enables controlled subsystem validation before integration.
Verification method: Bench test.

### DEV-004

Requirement ID: DEV-004
Requirement: Requirements shall have an identified verification method.
Status: Accepted
Rationale: Establishes traceable verification planning.
Verification method: Traceability review.

### DEV-005

Requirement ID: DEV-005
Requirement: Test results shall be retained and linked to the applicable requirement.
Status: Accepted
Rationale: Preserves evidence for requirement validation.
Verification method: Traceability review.

### DEV-006

Requirement ID: DEV-006
Requirement: Failures and unexpected behavior discovered during testing shall be documented.
Status: Accepted
Rationale: Retains evidence for corrective action and future decisions.
Verification method: Documentation review.

### DEV-007

Requirement ID: DEV-007
Requirement: A system shall not be described as validated solely because it powers on or operates briefly.
Status: Accepted
Rationale: Prevents insufficient evidence from being treated as validation.
Verification method: Traceability review.

### DEV-008

Requirement ID: DEV-008
Requirement: Changes affecting braking, throttle, fuel, ignition, or electrical protection shall require technical review.
Status: Accepted
Rationale: Applies technical review to safety-critical changes.
Verification method: Traceability review.
Review: Technical Review Required

## Documentation and traceability requirements

### DOC-001

Requirement ID: DOC-001
Requirement: Important requirements, research findings, proposals, decisions, implementation records, and test results shall be retained in the repository.
Status: Accepted
Rationale: Preserves the project record and supporting evidence.
Verification method: Traceability review.

### DOC-002

Requirement ID: DOC-002
Requirement: Confirmed facts, unverified information, proposals, and accepted decisions shall remain clearly distinguishable.
Status: Accepted
Rationale: Prevents information confidence from being misrepresented.
Verification method: Documentation review.

### DOC-003

Requirement ID: DOC-003
Requirement: Assumptions shall not be presented as confirmed facts.
Status: Accepted
Rationale: Protects the integrity of project information.
Verification method: Documentation review.

### DOC-004

Requirement ID: DOC-004
Requirement: Accepted decisions shall preserve their rationale.
Status: Accepted
Rationale: Retains the reasoning needed to understand later decisions.
Verification method: Documentation review.

### DOC-005

Requirement ID: DOC-005
Requirement: Superseded decisions shall remain traceable to the record that replaced them.
Status: Accepted
Rationale: Preserves decision history and change rationale.
Verification method: Traceability review.

### DOC-006

Requirement ID: DOC-006
Requirement: OEM part numbers, source models, model years, measurements, and source links shall be recorded when relevant and known.
Status: Accepted
Rationale: Preserves source evidence without asserting unavailable information.
Verification method: Documentation review.

### DOC-007

Requirement ID: DOC-007
Requirement: Each accepted implementation decision shall be traceable to supporting requirements and evidence.
Status: Accepted
Rationale: Connects implementation decisions to their supporting basis.
Verification method: Traceability review.

### DOC-008

Requirement ID: DOC-008
Requirement: Unresolved questions shall remain explicitly marked as unresolved or unverified.
Status: Accepted
Rationale: Prevents open issues from being treated as established information.
Verification method: Documentation review.

### DOC-009

Requirement ID: DOC-009
Requirement: Repository documentation shall be written in English.
Status: Accepted
Rationale: Applies the repository documentation standard.
Verification method: Documentation review.

## Open requirement areas

The following areas require later definition. No requirement values or solutions
are established in this document.

- Measurable performance targets — Status: Unverified
- Emissions and legal-compliance targets — Status: Unverified
- Electrical load and power-budget limits — Status: Unverified
- Measurable environmental and electrical qualification limits — Status: Unverified
- Diagnostic protocol requirements — Status: Unverified
- Limp-home and degraded-operation behavior — Status: Unverified
- Detailed human-machine-interface requirements — Status: Unverified
- Final acceptance criteria for each implementation stage — Status: Unverified

## Navigation

[Documentation index](../INDEX.md) · [System architecture](../architecture/system-architecture.md) · [Test strategy](../testing/test-strategy.md)
