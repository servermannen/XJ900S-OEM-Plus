# Connector Identification Record

**Purpose:** Record connector, terminal, locking, depinning, crimping, and
compatibility evidence without converting appearance, partial markings, mating
fit, or successful service actions into unsupported identity or compatibility
claims.

**Document status: Draft**

**Status:** `<Unverified | Proposal | Confirmed>`

**Review:** `<Technical Review Required | Technically Reviewed | Not Applicable>`

Use this template for OEM harness connectors, ECU connectors, sensor/actuator
connectors, switchgear connectors, lighting/body connectors, relay connectors,
inline connectors, replacement/service connectors, terminals, seals, and
depinning/removal tools.

Confirmation of one dimension does not confirm any other dimension. For
example, a housing part number does not establish terminal family; a mating
connector does not establish pin function; matching cavity count does not
establish compatibility; visual similarity does not establish family;
successful insertion does not establish terminal retention; successful
depinning does not establish correct removal-tool identity; and wire colour
does not establish cavity numbering or circuit function without applicable
evidence.

## Evidence hierarchy

Prefer evidence in this order:

1. OEM service manuals, wiring diagrams, and parts catalogues.
2. Connector manufacturer drawings, catalogues, and datasheets.
3. Terminal manufacturer drawings and datasheets.
4. Authoritative service-tool documentation.
5. Direct physical markings and dimensional measurements.
6. Documented controlled fit or depinning tests.
7. Reputable technical references.
8. Marketplace photos or listings.
9. Forums, videos, or anecdotal material.

Marketplace material may support observations about visible markings, shape,
keying, availability, and variant comparison. Marketplace material alone shall
not confirm exact family, terminal specification, current rating, sealing,
pinout, circuit function, or safety suitability.

## Identification

- Project connector reference/name: `<Reference>`
- Associated component / harness: `<Component or harness>`
- Vehicle/model/year/source: `<Vehicle, model, year, and source>`
- Connector side: `<Harness-side housing | Device/header-side | Inline mating half>`
- Manufacturer: `<Manufacturer or Unknown>`
- Connector family: `<Family or Unknown>`
- Exact housing part number: `<Part number or Unknown>`
- Visible markings exactly as observed: `<Literal markings or None observed>`
- Number of cavities: `<Number or Unknown>`
- Keying / polarization: `<Evidence or Unknown>`
- Colour: `<Colour or Unknown>`
- Sealed / unsealed: `<Sealed | Unsealed | Unknown>`
- Source/evidence: `<Source references, photos, measurements>`
- Information status: `<Confirmed | Unverified | Proposal>`

## Mating Interface

- Exact mating housing/header part number: `<Part number or Unknown>`
- Manufacturer: `<Manufacturer or Unknown>`
- Family: `<Family or Unknown>`
- Keying compatibility: `<Evidence or Unknown>`
- Latch/interface: `<Evidence or Unknown>`
- CPA where applicable: `<CPA evidence, Not applicable, or Unknown>`
- Evidence status: `<Confirmed | Unverified | Proposal>`

Do not infer mating part numbers from appearance alone.

## Terminal System

Use one row for each terminal type used.

| Terminal role | Manufacturer | Terminal family | Exact terminal part number | Male/female | Nominal terminal size/system | Wire-size range | Conductor cross-section range | Insulation range | Plating/material | Current rating | Seal part number | Cavity plug / blanking seal | Evidence/source | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `<Role>` | `<Manufacturer or Unknown>` | `<Family or Unknown>` | `<Part number or Unknown>` | `<Male | Female | Unknown>` | `<Size/system or Unknown>` | `<Range or Unknown>` | `<Range or Unknown>` | `<Range or Unknown>` | `<Evidence or Unknown>` | `<Only with authoritative evidence, else Unknown>` | `<Part number, Not applicable, or Unknown>` | `<Part number, Not applicable, or Unknown>` | `<Source>` | `<Confirmed | Unverified | Proposal>` |

Do not infer terminal family from housing appearance alone.

## Cavity Map

Orientation/view definition: `<Connector face viewed from terminal/mating side | Connector viewed from wire-entry side | Other documented view>`

Cavity numbering must not be inferred from left-to-right visual order without
authoritative numbering or a documented project numbering scheme. If OEM
numbering is unknown, use a temporary project locator and label it as such; do
not present it as OEM cavity numbering.

| Cavity number or project locator | Orientation/view definition | Wire colour | Conductor size | Terminal | Seal | Circuit/function | Source | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `<Cavity or temporary locator>` | `<View>` | `<Colour or Unknown>` | `<Size or Unknown>` | `<Terminal or Unknown>` | `<Seal or Unknown>` | `<Function or Unknown>` | `<Source>` | `<Confirmed | Unverified | Proposal>` |

## Locking System

- Terminal primary locking lance: `<Housing lance | Terminal lance | Other | Unknown>`
- Access side: `<Terminal/mating side | Wire-entry side | Other | Unknown>`
- Terminal secondary lock: `<TPA | Retainer | Wedge | Other | None documented | Unknown>`
- Secondary-lock service position: `<Evidence or Unknown>`
- Evidence/source: `<Source>`

Do not use TPA, CPA, retainer, wedge, or secondary lock as interchangeable
terms. CPA is connector-position assurance and shall not be recorded as the
terminal secondary lock unless authoritative manufacturer documentation
explicitly uses different terminology.

## Depinning / Terminal Removal

- Exact removal/depinning tool manufacturer: `<Manufacturer or Unknown>`
- Exact removal/depinning tool part number: `<Part number or Unknown>`
- Tip dimensions/profile if documented: `<Dimensions/profile or Unknown>`
- Tool insertion side: `<Terminal/mating side | Wire-entry side | Other | Unknown>`
- Secondary-lock preparation: `<Procedure or Unknown>`
- Release action: `<Procedure or Unknown>`
- Pull direction: `<Direction or Unknown>`
- Wire/terminal handling precautions: `<Precautions>`
- Terminal reuse status: `<Reusable if manufacturer/service documentation permits | Replace after removal | Unknown>`
- Inspection after removal: `<Inspection requirement>`
- Evidence/source: `<Source>`

Do not force a terminal out, pull on the wire before the locking lance is
released, damage a seal with the release tool, bend a terminal retention lance
unless the manufacturer procedure requires it, or assume a generic pin tool is
correct because it fits into the cavity.

## Crimping / Replacement

- Terminal part number: `<Part number or Unknown>`
- Seal part number: `<Part number, Not applicable, or Unknown>`
- Wire gauge/cross-section: `<Gauge/cross-section or Unknown>`
- Strip length from authoritative data: `<Length or Unknown>`
- Crimp tool: `<Tool or Unknown>`
- Die: `<Die or Unknown>`
- Locator/positioner if applicable: `<Locator/positioner, Not applicable, or Unknown>`
- Conductor crimp: `<Requirement or Unknown>`
- Insulation/support crimp: `<Requirement or Unknown>`
- Seal crimp where applicable: `<Requirement, Not applicable, or Unknown>`
- Pull-test or inspection requirement: `<Requirement or Unknown>`
- Acceptance criteria/source: `<Source or Unknown>`

Do not invent crimp height, strip length, pull force, or current rating.

## Compatibility Status

Do not use one overall "compatible" field to hide unresolved subdimensions.

| Dimension | Status | Evidence and boundary |
| --- | --- | --- |
| Physical mating compatibility | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Terminal compatibility | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Wire-size compatibility | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Sealing/environmental compatibility | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Electrical compatibility | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Circuit/pin-function compatibility | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Serviceability | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Safety suitability | `<Confirmed | Unverified | Proposal>` | `<Evidence and boundary>` |
| Final project acceptance decision | `<Accepted | Unverified | Proposal>` | `<Decision evidence and boundary>` |

Confirmed compatibility evidence is not the same as project acceptance.
`Accepted` is reserved for a deliberate project acceptance decision.

Connector work affecting ignition, fuel, DBW/throttle, engine shutdown,
fuel-pump control, safety inputs, braking-related electrical functions, or
electrical protection requires `Review: Technical Review Required` before
operational use. Successful power-on, continuity, connector mating, or engine
start does not alone validate connector correctness.

## Evidence and Photographs

Required where applicable:

- Overall connector photo.
- Connector face.
- Wire-entry side.
- Visible markings.
- Secondary lock.
- Terminal removed, when safe/applicable.
- Mating half.
- Scale/reference measurement when dimensions matter.

Photographs are evidence of observed geometry and markings only unless tied to
authoritative identification.

## Change History and Traceability

- Related component record: `<Component record or None>`
- Related harness: `<Harness or None>`
- Source documents: `<Source documents>`
- Measurement records: `<Measurement records or None>`
- Related test records: `<Test records or None>`

| Date | Evidence/status change | Reason |
| --- | --- | --- |
| `<YYYY-MM-DD>` | `<Change>` | `<Reason>` |

## Navigation

[Template index](README.md) | [Documentation index](../INDEX.md)
