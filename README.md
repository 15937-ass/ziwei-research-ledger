# ziwei-research-ledger

**Research Memory Sidecar v1** for [ziwei-state-space](https://github.com/15937-ass/ziwei-state-space).

This repository stores non-authoritative research memory: major research events, multi-axis claims, theory evolution, concept events, paper/research-question mappings, and bounded evidence packs.

## Authority and non-interference

- The main repository's accepted artifacts and approved Human Gates remain authoritative.
- This repository is a read-mostly, derived memory layer; it cannot modify canonical Zhongzhou knowledge or Product runtime.
- Product and Knowledge never depend on this repository. Ledger downtime, delay, or failure must not block their work or PR merges.
- Records sourced only from an open Issue, unmerged PR, or chat are explicitly labelled and cannot be represented as accepted main truth.
- Historical records are append-only. Corrections create a superseding record; they do not silently rewrite prior conclusions.
- No GitHub Actions workflow or required check is introduced by this bootstrap.

## Repository map

- **ARCHITECTURE.md** — authority hierarchy, non-interference, capture and replay policy.
- **SCHEMA.md** — human-readable record semantics and maturity axes.
- **RESEARCH_STATE.yaml** — source checkpoint and migration status.
- **schemas/** — JSON Schema contracts for each record type.
- **events/** — R2/R3/R4 milestones and explicit Concept Events (RM-2026-001 through RM-2026-010).
- **claims/** — claim registry with independent source, implementation, internal-fidelity, empirical and causal axes (CL-001 through CL-012).
- **theory/** — theory evolution and supersession history (TE-001 through TE-006).
- **paper_map/** — research questions, claims, manuscript sections and evidence links.
- **evidence_packs/** — curated claim-bounded evidence packs (EP-001 through EP-006).
- **migration/** — source audit, overlap notes and migration limitations.
- **templates/** — capture guidance and ID conventions.

## First bootstrap boundary

The initial records are a **curated historical seed**, not a complete replay of every historical commit or chat. The checkpoint records the main-repository SHA examined for this seed. Historical manuscript text is a snapshot/output, not project memory and not independent evidence of predictive validity.

See [Issue #1](https://github.com/15937-ass/ziwei-research-ledger/issues/1) for the bounded bootstrap and [Issue #5](https://github.com/15937-ass/ziwei-research-ledger/issues/5) for the targeted evidence backfill.
