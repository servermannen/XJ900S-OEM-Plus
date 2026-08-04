# TEST-<DOMAIN>-<NUMBER>: <Test title>

**Purpose:** Define and record one repeatable verification activity.

**Document status: Draft**

Identification, objective, configuration, procedure, criteria, result, and evidence are mandatory.

## Test identification

- Test ID: `TEST-<DOMAIN>-<NUMBER>`
- Related requirements: `<Requirement IDs>`
- Related ADRs: `<ADR identifiers>`
- Architecture reference: `<Section or relative link>`
- Roadmap stage: `<Stage>`
- Test type: `<Inspection, electrical, bench, functional, fault injection, road, etc.>`

## Execution status

**Execution status:** `<Not started | Ready | In progress | Completed>`

**Review:** `<Technical Review Required | Technically Reviewed | Not Applicable>`

## Objective

<What this test proves or evaluates.>

## Tested configuration

- Motorcycle or subsystem: `<Value>`
- Hardware revision: `<Value>`
- Software or firmware version: `<Value>`
- Calibration and wiring revision: `<Value>`
- Installed components: `<Value>`
- Location, date, and tester: `<Values>`

Mark unknown or inapplicable values explicitly.

## Preconditions

- `<Precondition>`

## Hazards and precautions

- Hazard: `<Hazard>`
- Protective measure: `<Measure>`
- Required safe state: `<Safe state>`
- Emergency shutdown method: `<Method>`
- Stop conditions: `<Conditions>`

## Equipment

| Equipment | Identifier | Accuracy or range | Calibration status |
| --- | --- | --- | --- |
| `<Equipment>` | `<Identifier>` | `<Value or Not defined>` | `<Status>` |

## Inputs and initial state

- `<Input or starting condition>`

## Procedure

1. `<Step>`
2. `<Step>`

## Expected results and acceptance criteria

| Step or measurement | Expected result | Acceptance criterion |
| --- | --- | --- |
| `<Reference>` | `<Expected behavior>` | `<Criterion>` |

Define criteria before formal execution.

## Actual results

| Step or measurement | Actual result | Evidence reference |
| --- | --- | --- |
| `<Reference>` | `<Observed behavior>` | `<Evidence>` |

## Result classification

**Result:** `<Pass | Fail | Inconclusive | Blocked | Not run>`

Do not use Pass if a criterion failed or was not evaluated.

## Deviations
- `<Deviation>`

## Defects and follow-up actions
- `<Defect or action>`
- Related issue or record: `<Reference>`

## Regression impact
- Retest required: `<Yes, No, or Undetermined>`
- Related tests and reason: `<References and reason>`

## Technical review
- Reviewer: `<Name>`
- Review date: `<YYYY-MM-DD>`
- Review scope and outcome: `<Details>`
- Remaining limitations: `<Limitations>`

Use `Review: Technically Reviewed` only after this section is completed.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| `<YYYY-MM-DD>` | `<Description>` | `<Reason>` |

## Guidance

Use one primary objective, preserve failed/inconclusive and repeated evidence,
and define criteria before execution. Road and safety tests require stop and
recovery provisions. Never knowingly create uncontrolled fuel, ignition,
electrical, thermal, braking, throttle, or mechanical risk.

## Navigation

[Test strategy](../testing/test-strategy.md) | [Documentation index](../INDEX.md) | [Template index](README.md)
