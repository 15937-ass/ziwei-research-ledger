# Record Semantics and Schema Guide

Schema files under schemas/ are JSON Schema draft 2020-12. Seed JSON records are the examples. All records use schema_version 1.0.

## ID conventions

- Research Event: RM-YYYY-NNN
- Claim: CL-NNN
- Theory Evolution: TE-NNN
- Concept Event: CE-YYYY-NNN
- Paper Map: PM-<stable slug>
- Evidence Pack: EP-NNN

IDs are stable and never reused. If a record is superseded, retain its ID and history.

## Authority labels for artifact references

- ACCEPTED_MAIN: artifact exists on the main branch at the recorded checkpoint.
- MERGED_PR: a PR that has actually merged.
- OPEN_ISSUE: design or execution context still open; not proof of implementation.
- UNMERGED_PR: proposed changes not accepted into main.
- CLOSED_UNMERGED_PR: closed without merge, including a superseded PR.
- CHAT_CONTEXT: explicitly captured conversation rationale.
- DERIVED_SYNTHESIS: this repository's own synthesis, not independent source evidence.

Always state the authority status; do not imply that all links are equal evidence.

## Claim axis definitions

### source_status
EXPLICIT, TRANSPARENT_INFERENCE, SOURCE_UNDERDETERMINED, SOURCE_CONFLICT, NOT_APPLICABLE.

This axis describes support from the claim's stated evidence basis. For PROJECT_ARTIFACT claims, EXPLICIT means explicit in accepted project documentation, not necessarily explicit in a classical Zi Wei source. evidence_basis must disambiguate that.

### implementation_status
NOT_SPECIFIED, SPECIFIED, PARTIALLY_IMPLEMENTED, IMPLEMENTED, DEPRECATED.

### internal_fidelity
UNTESTED, CONTRACT_PASS, CASE_RECONSTRUCTION_PASS, BENCHMARKED, NOT_APPLICABLE.

### empirical_status
UNTESTED, RETROSPECTIVE, PROSPECTIVE, REPLICATED, NULL_RESULT, INCONCLUSIVE, NOT_APPLICABLE.

### causal_status
NONE, ASSOCIATIONAL, PARTIALLY_IDENTIFIED, IDENTIFIED, NOT_APPLICABLE.

These axes are independent. No axis may be promoted because another axis is mature.

## Epistemic boundary

The term “canonical method boundary” means a frozen project-method constraint, not a canonical Zhongzhou rule. Research normalizations such as 气→象→事 and the N/E/S/A/C trajectory model must be explicitly distinguished from source-authored doctrine. A Concept Event is not canonical Zhongzhou truth unless separately source-supported and approved through the normal Knowledge lane.

## Safe wording

Prefer bounded wording: “the current source-bounded model specifies…”, “the current implementation supports…”, or “the held-out benchmark found…”. Avoid “proven accurate”, “scientifically validated”, or causal recommendations unless the relevant evidence axis independently supports that wording.
