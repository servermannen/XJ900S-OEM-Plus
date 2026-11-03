---
name: xj900s-engineering-evidence
description: Evaluate XJ900S OEM+ engineering claims against source evidence, accepted ADRs, and safety review requirements.
---

# XJ900S Engineering Evidence (Draft)

Use for technical findings, compatibility claims, measurements, connector research and ADR impact reviews in this repository.

## Authority
1. Read `AGENTS.md`, `docs/INDEX.md`, and relevant accepted ADRs before conclusions.
2. Apply ADR-0004 precedence: safety > reliability > serviceability > OEM-like integration > functional improvement > future expandability.
3. Keep document maturity, information status, and technical review status separate. Use repository labels exactly: `Status: Confirmed | Unverified | Proposal | Accepted`; `Review: Technical Review Required | Technically Reviewed`.
4. `Accepted` means an explicit decision, not an inferred fit or successful test.

## Evidence workflow
1. State the exact claim, its scope, and what would falsify it.
2. Record source URL or repository path, revision/date, applicable Yamaha model/year/part number, measurement method, units, tolerances and uncertainty.
3. Distinguish OEM/manufacturer documentation, directly observed measurements, calculations, photogrammetric estimates and third-party assertions. Direct measurement confirms only the measured property.
4. Assign information status *per claim*, not one blanket status per component. Leave unknown properties unverified.
5. Cross-check conflicts against accepted ADRs and requirements; document unresolved contradictions, blockers, and required next verification.
6. Mark claims affecting braking, throttle/DBW, fuel, ignition, engine shutdown, or electrical protection `Review: Technical Review Required` until reviewed.
7. Never claim component compatibility from appearance, shared connector cavity count, wire color, physical mating, or similar Yamaha part numbers.
8. For connectors, use `docs/templates/connector-identification-template.md`; record cavity view, locking, terminal, seal, depinning and separate compatibility dimensions.
9. For numbered engineering documents, inspect the existing series and indexes and search the entire repository for collisions before proposing a new ID.
10. Do not modify accepted ADRs, declare safety validation, or advance an implementation gate without separate authorization.

## Output
- Claim and project scope
- Evidence with precise source references
- Confirmed / Unverified / Proposal findings (use repository status labels)
- Measurement uncertainty and compatibility boundaries
- ADR/requirements impact
- Technical review status
- Blocking unknowns and smallest safe next verification

## Draft verification scenarios
- MT-10 throttle-body pitch directly measured at 84.0 mm: do not infer XJ900S head port spacing or fit.
- Photogrammetric XJ900S intake spacing estimate: retain uncertainty, do not mark OEM-confirmed.
- Four-cavity connector with matching colors: refuse pinout/terminal compatibility inference.
- A brake/DBW proposal with apparent functional fit: require technical review and test evidence before acceptance.

Document status: Draft. Not tested against independent baseline and post-skill scenarios.