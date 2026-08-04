# Documentation Templates

**Purpose:** Index reusable project-documentation templates and their conventions.

## Templates

| Template | Use |
| --- | --- |
| [Requirement template](requirement-template.md) | Create a new traceable requirement |
| [ADR template](adr-template.md) | Record an accepted architecture or design decision |
| [Research record template](research-record-template.md) | Capture research, evidence, uncertainty, and open questions |
| [Component evaluation template](component-evaluation-template.md) | Evaluate a candidate component against requirements |
| [Test-case template](test-case-template.md) | Define and record a repeatable verification activity |

## Naming conventions

- Requirements: `<CATEGORY>-<NUMBER>`
- ADRs: `ADR-<NUMBER>-<short-title>.md`
- Research: `RESEARCH-<NUMBER>-<short-title>.md`
- Components: `COMP-<NUMBER>-<short-title>.md`
- Tests: `TEST-<DOMAIN>-<NUMBER>-<short-title>.md`

Check numbering against existing records before creating a file.

## Status conventions

- Document maturity: `Document status: Draft`, `Document status: Review`, or `Document status: Final`.
- Information: `Status: Confirmed`, `Status: Unverified`, `Status: Proposal`, or `Status: Accepted`.
- Execution status: `Execution status: Not started`, `Execution status: Ready`,
  `Execution status: In progress`, or `Execution status: Completed`.
- Test result: `Result: Pass`, `Result: Fail`, `Result: Inconclusive`, `Result: Blocked`, or `Result: Not run`.
- Technical review: `Review: Technical Review Required`, `Review: Technically Reviewed`, or `Review: Not Applicable`.

These dimensions shall not be merged into one label.

## Copying instructions

Copy the relevant template to its destination, assign an unused identifier,
replace every mandatory angle-bracket placeholder, remove unused optional
sections deliberately, and verify links and status labels before review.

## Navigation

[Documentation index](../INDEX.md)
