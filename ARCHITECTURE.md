# Research Memory Sidecar v1 — Architecture

## 1. Purpose

Preserve the research meaning of important project changes: what changed in understanding, why it changed, which claims gained or lost support, and where the evidence lives. Do not turn the sidecar into a second project-state authority or a mandatory development stage.

## 2. Authority hierarchy

For factual claims, prefer the highest available level:

1. Approved source artifacts and explicit Human Gates for canonical Zhongzhou meanings.
2. Accepted artifacts on the main branch of ziwei-state-space.
3. Accepted validation/benchmark evidence tied to a recoverable version.
4. Merged Issue/PR rationale.
5. Explicitly captured Concept Events, with their epistemic status preserved.
6. Research synthesis and manuscript prose.

An open Issue records proposed or approved-in-chat design intent, but does not make unmerged files part of main. An unmerged PR is a review candidate, not accepted implementation. Sidecar records may cite these sources with their authority status; they must not silently upgrade them.

## 3. One-way, non-interfering topology

ziwei-state-space -> accepted evidence read -> ziwei-research-ledger

There is no reverse write path from the sidecar into Product or Knowledge. A Research record may raise a gap/candidate note, but it may not repair canonical rules, alter runtime semantics, create a required check, or gate Product/Knowledge merges.

The sidecar may lag. If unavailable, normal project execution continues. No scheduled ingestion or GitHub Actions workflow is part of v1.

## 4. Record types

- **Research Event (RM):** a significant change in what the project knows or can demonstrate.
- **Claim (CL):** a bounded statement with independent maturity axes.
- **Theory Evolution (TE):** an append-only record of a model change, including old model, limitation, new model, rationale and consequences.
- **Concept Event (CE):** a significant theory/philosophy idea not yet represented as an accepted canonical artifact. It remains explicitly non-canonical unless separately source-reviewed.
- **Paper Map (PM):** maps research questions to claims, methods, evidence, manuscript sections and wording ceilings.
- **Evidence Pack (EP):** a bounded bundle of accepted artifacts, claims, limitations and safe wording. V1 packs are curated manually; an automated generator is deferred.

## 5. Significance policy

- **R0 — routine engineering:** typo, routine refactor, fixture repair; no immediate research record.
- **R1 — cumulative progress:** routine extraction/review batches under an unchanged schema; accumulate counters and summarize later.
- **R2 — major research milestone:** a domain closes, a reusable compiler stage becomes executable, a benchmark family becomes operational, or a significant null/negative result is established.
- **R3 — theory/paradigm milestone:** ontology, epistemic boundary, research method or system architecture changes materially.
- **R4 — empirical finding:** a preregistered prospective/held-out result, reproducible null result, calibration failure or replicated incremental signal.

R2/R3/R4 are captured promptly. R0/R1 are not individually logged unless their accumulation changes a research conclusion.

## 6. Multi-axis claim maturity

Never collapse the following into a single “confidence” score:

- **source_status:** what the cited source or project artifact explicitly supports;
- **implementation_status:** whether the representation is specified, partial, implemented or deprecated;
- **internal_fidelity:** whether internal contract/case/benchmark checks have passed;
- **empirical_status:** whether an external target has been tested retrospectively/prospectively or replicated;
- **causal_status:** whether evidence is associational or causally identified.

A strong source basis does not imply implementation. An implementation does not imply internal fidelity. Internal fidelity does not imply predictive validity. Predictive association does not imply causality.

## 7. Provenance and correction

Every record should link to exact repository artifacts, immutable commit/blob SHAs where available, and the authority status at capture time. Do not cite a moving branch alone when a commit SHA is available.

Historical records are append-only. To correct a record, create a replacement/superseding record and connect both IDs with supersedes/superseded_by. Mutable indexes and RESEARCH_STATE.yaml may be updated as derived views.

## 8. Replay and checkpoint

RESEARCH_STATE.yaml stores last_seen_main_sha. On catch-up:

1. read the checkpoint;
2. inspect accepted main history after it;
3. classify candidate changes R0–R4;
4. create only missing R2–R4 records;
5. update derived claim/theory/paper views;
6. advance the checkpoint only after records are durably committed.

Bootstrap exception: the initial checkpoint is a curated baseline, not proof that every historical commit was replayed. The exact seed scope and exclusions are recorded in migration/2026-10-22-source-audit.md.

## 9. Manuscripts and evidence packs

Manuscripts are outputs/snapshots, not project memory. A manuscript may lag without changing project truth. Before a claim enters an Evidence Pack, the pack must include current accepted support, counterevidence/limitations, and a wording ceiling. Do not use manuscript prose alone as proof of its own quantitative claims.

## 10. V1 exclusions

Preregistration/experiment registry, dataset/model cards, automated scheduled ingestion, RO-Crate export and automatic manuscript rewriting are deferred until their need is concrete. No Actions workflows are added or invoked in this work unit.
