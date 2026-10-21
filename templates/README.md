# Record authoring guide

Use the matching JSON Schema under schemas/ and copy a record with the same type as a starting example.

## Before adding a record

1. Choose the significance level: R0/R1 do not normally create immediate Research Events; R2/R3/R4 do.
2. Link immutable accepted artifacts where available (repository path, commit/blob SHA, URL).
3. Label open Issues, unmerged PRs and chat context honestly. They are not accepted main truth.
4. Fill each Claim maturity axis independently.
5. State the wording ceiling and limitations explicitly.
6. For a theory change, preserve the old model and rationale; do not overwrite the previous Theory Evolution record.
7. Use a new ID for a new record. Use supersedes/superseded_by to correct prior records.
8. Do not create a duplicate record just because the same concept appears in both historical archives; add provenance to the existing record.

## Current examples

- Research Events: events/RM-2026-001 through RM-2026-004
- Claims: claims/CL-001 through CL-005
- Theory Evolution: theory/TE-001 through TE-004
- Concept Event: events/CE-2026-001
- Paper Map: paper_map/PM-P1-FORMALIZATION.json
- Evidence Pack: evidence_packs/EP-001.json
