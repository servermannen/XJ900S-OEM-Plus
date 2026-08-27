# AGENTS.md

## Project purpose

This repository documents the engineering and development of the XJ900S OEM+
project: a 1997 Yamaha XJ900S Diversion reimagined as if Yamaha had continued
developing the model into 2027.

## Documentation standards

- Write all repository documentation in English.
- Prioritize reliability, safety, serviceability, and OEM-like integration.
- Prefer proven production components where practical.
- Clearly distinguish confirmed facts, unverified information, proposals, and
  accepted decisions.
- Never convert an assumption into a confirmed fact.
- Preserve source links and Yamaha OEM part numbers when known.
- Do not overwrite an accepted decision without documenting why.

## Documentation labels

Document maturity describes the state of a document, for example
`Document status: Draft`. Information status describes the confidence level of
an individual fact, finding, proposal, or decision. Technical review status is
separate from both and records whether a safety-critical claim has received
technical review.

Use these information status labels where applicable:

- `Status: Confirmed`
- `Status: Unverified`
- `Status: Proposal`
- `Status: Accepted`

Use these technical review labels where applicable:

- `Review: Technical Review Required`
- `Review: Technically Reviewed`

## Safety

Claims concerning braking, throttle control, fuel, ignition, or electrical
protection are safety-critical. Mark them `Review: Technical Review Required`
until they have received technical review, then use
`Review: Technically Reviewed`.

## Git workflow

- Make focused changes related only to the requested task.
- Before proposing or creating an ID in any sequentially numbered document
  series (for example `RESEARCH-*`, `ADR-*`, `TEST-PLAN-*`, `COMP-*`,
  `COMPONENT-*`, or a future equivalent), inspect the existing family sequence
  and search the entire repository, including already committed files, for the
  exact proposed ID; for example, run `rg -n "RESEARCH-0007" .` and
  `rg -n "RESEARCH-[0-9]{4}" .`. Absence from `git diff` or the working tree
  does not establish that an ID is unused.
- Check `docs/INDEX.md` and the applicable family-specific README or index when
  one exists; for `RESEARCH-*`, check both `docs/INDEX.md` and
  `docs/research/README.md`. Do not create the document until the proposed ID
  is confirmed unused repository-wide.
- Show the diff before committing.
- Do not commit or push unless explicitly instructed.
