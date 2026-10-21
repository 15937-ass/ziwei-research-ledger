# RSM-1 Source Audit and Migration Decisions — 2026-10-22

## 1. Source checkpoint

At bootstrap, the main repository head was:

- Repository: https://github.com/15937-ass/ziwei-state-space
- Ref: main
- Commit: f6944c896efd8f215d4e7d9d89f9fa4db84759f6
- The checkpoint is a curated bootstrap baseline. It is not a claim that every historical commit was replayed.

Primary files inspected:

- PROJECT_CONSTITUTION.md — blob SHA eadad9e01cd85fbf1bcee48240b7e688ffe7012c
- DECISION_LOG.md — blob SHA 183423d9ec507625dc7eb344573ccbdfd75f0f9d
- paper/outline.md — blob SHA ece8b30328fe1e7b8a9c8ba37c13f516b7e325e7
- paper/manuscript_v0.1.md — blob SHA 281127cbaea3b84d23021092089cddf25eae1369
- governance/archive/2026-10-21-chat-theory-design-philosophy-preservation.md — blob SHA b2bc548831da43ccfe2575764a0bed200ca2d3b8
- product/PRODUCT_FUTURE_WORKPLAN_v0.1.md — blob SHA 302cd22721f6a1721d078450cea7168af0e0b856

## 2. Issue / PR state

- Issue #513 is OPEN and records the PI-approved-in-chat design direction and non-interference contract.
- PR #562 is OPEN and UNMERGED. At first inspection GitHub returned mergeable=false; a later recheck returned mergeable=true. Its recorded base SHA (9114300e306abc908ab1fe1724faa7957ad728b9) predates the inspected main head above. Mergeability is only a technical conflict hint: the PR's diff and required validation still need review against current main before acceptance. This Sidecar bootstrap does not merge or update PR #562.
- PR #562 proposes DECISION_LOG D-021 and governance/archive/2026-10-21-pre-delete-chat-archaeology.md. Neither proposed file is treated here as accepted main truth.
- PR #514 is CLOSED without merge and explicitly says it was superseded by the refreshed PR #562. It is not the current implementation PR.
- The accepted main archive's section 7.1 still points to Issue #513 / PR #514 and describes it as open. That pointer is stale. This sidecar records the correction as a migration note; it does not silently edit the main archive or treat the sidecar as authority over main.

## 3. Archive overlap

Accepted main archive:
- governance/archive/2026-10-21-chat-theory-design-philosophy-preservation.md
- approximately 20,183 characters and 76 headings at audit time.
- Broad thematic synthesis with explicit sections on project philosophy, G1-G6, A0-A2, N/E/S/A/C, product-first, evaluation boundaries, AI method ladder, multi-school isolation and open questions.

PR #562 proposed archive:
- governance/archive/2026-10-21-pre-delete-chat-archaeology.md
- approximately 19,716 characters and 118 headings at audit time.
- More explicitly decomposed into CE-001 onward, with old-model/new-model rationale and Git mapping for each conceptual transition.

The archives have substantial topical overlap. Their different heading counts and text lengths do not make them independent evidence. A token-level overlap estimate is not reliable for Chinese text and is not used as a scientific metric here.

Migration decision:
1. Do not copy either archive verbatim into the sidecar as one giant “truth” document.
2. Decompose the accepted main archive into curated RM / TE / CL / PM / EP records with source links.
3. Use the proposed PR #562 archive only as a historical, unmerged candidate source when it adds useful rationale not already represented; retain UNMERGED_PR provenance and do not promote D-021 to accepted decision until merged.
4. Where the same concept appears in both archives, keep one canonical sidecar record with multiple provenance links, not duplicate records.
5. Preserve chat-derived philosophy such as “命不是固定轨迹” as a research hypothesis / project philosophy, not a canonical Zhongzhou rule.

## 4. Manuscript and paper files

- paper/outline.md is the research-question and section plan.
- paper/manuscript_v0.1.md is a working manuscript snapshot, not current project state or an independent source of evidence.
- Quantitative statements in the manuscript must be traced to their actual validation artifacts before they are used as empirical findings in a paper or Evidence Pack.
- The current Paper 1 wording ceiling remains formalization, traceability, reproducibility and internal fidelity within the defined corpus; it does not establish real-world predictive accuracy, causal validity, or a physical mechanism for qi.

## 5. No cross-lane mutation

This work reads main-repository evidence only. It does not modify Product or Knowledge paths, change canonical rules, add a fourth authoritative lane, create a required check, or add/invoke GitHub Actions.


## 6. Final checkpoint catch-up during bootstrap

After the curated seed was written, main advanced by exactly one commit:

- Previous seed source SHA: `f6944c896efd8f215d4e7d9d89f9fa4db84759f6`
- Newly observed main SHA: `11f9eedd6bfcb05e5d0fcb2f17327bc3c288de86`
- Compare result: one commit ahead, zero behind.
- Changed files: P10 Property direct-transform remainder audit/map, P10 state checkpoint, targeted test and execution evidence.

This commit was inspected and classified as **R1 cumulative Knowledge progress**, not a distinct R2/R3/R4 research event. The checkpoint in RESEARCH_STATE.yaml therefore advances to the new SHA so it will not be replayed indefinitely. This is not a complete historical replay: `history_replay_complete` remains false, and earlier unseeded history remains outside this curated bootstrap.

The new commit is a Knowledge-lane artifact. This sidecar records only the replay/checkpoint decision; it does not modify the source Knowledge files or promote their semantics.
