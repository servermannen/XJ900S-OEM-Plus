# COMP-<NUMBER>: <Component name>

**Purpose:** Evaluate a candidate component against accepted requirements.

**Document status: Draft**

Identification, evidence, compatibility status, safety, and recommendation are mandatory.

## Candidate identification

- Component: `<Name>`
- Manufacturer: `<Manufacturer>`
- Source model: `<Model>`
- Model year or range: `<Year or range>`
- OEM part number: `<Part number or Unknown>`
- Variant identifiers: `<Identifiers>`
- Source or listing: `<Link>`
- Evaluation date: `<YYYY-MM-DD>`

## Evaluation status

**Status:** `<Unverified | Proposal | Confirmed | Accepted>`

**Review:** `<Technical Review Required | Technically Reviewed | Not Applicable>`

## Intended function

<Project function being evaluated.>

## Applicable requirements

- `<Requirement ID>`

## Known specifications

| Attribute | Value | Unit | Source | Status |
| --- | --- | --- | --- | --- |
| `<Attribute>` | `<Value>` | `<Unit>` | `<Source>` | `<Confirmed or Unverified>` |

## Physical compatibility

- Dimensions: `<Known value or Unknown>`
- Mounting: `<Evidence or Unknown>`
- Clearances: `<Evidence or Unknown>`
- Connectors and routing: `<Evidence or Unknown>`
- Environmental suitability: `<Evidence or Unknown>`
- Required modifications: `<Evidence or Unknown>`

## Electrical or functional compatibility

- Supply and signals: `<Evidence or Unknown>`
- Inputs and outputs: `<Evidence or Unknown>`
- Communication and diagnostics: `<Evidence or Unknown>`
- Control authority and failure behavior: `<Evidence or Unknown>`
- Required interface hardware: `<Evidence or Unknown>`

Connector appearance alone is not compatibility evidence.

## Integration assessment

### Benefits
- `<Benefit>`

### Risks and constraints
- `<Risk>`

### Required adaptations
- `<Adaptation>`

### Missing evidence
- `<Evidence needed>`

## Safety assessment

<Impact on braking, throttle, fuel, ignition, protection, warnings, or other safety functions.>

## Serviceability and availability

- Replaceability and availability: `<Evidence>`
- Documentation and connector availability: `<Evidence>`
- Long-term support and alternatives: `<Evidence>`

## Decision recommendation

**Recommendation:** `<Reject | Continue research | Bench evaluate | Accept>`

**Rationale:** `<Evidence-based reason>`

Do not use `Accept` while material compatibility questions remain unresolved.

## Required validation

- `<Inspection or test>`

## Traceability

- Related research: `<Research records>`
- Related ADRs: `<ADR records>`
- Related tests: `<Test records>`
- Roadmap stage: `<Stage>`

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| `<YYYY-MM-DD>` | `<Description>` | `<Reason>` |

## Guidance

Similarity and purchase do not establish fit or acceptance. Keep availability,
specification, physical/electrical compatibility, and acceptance separate.
Record exact variants and model years. Safety-critical candidates need review
and test evidence.

## Navigation

[Component index](../components/README.md) | [Documentation index](../INDEX.md) | [Template index](README.md)
