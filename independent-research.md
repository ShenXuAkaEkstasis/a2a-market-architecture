---
layout: default
title: Independent Technical Follow-up — Agent Memory and Decision Authority
description: A third-party Databricks MVP experiment following Shen Xu's research on stale agent memory and current authorization.
---
# Independent Technical Follow-up: Agent Memory and Decision Authority

**Recorded:** October 2026  
**Original author:** Shen Xu (徐慎)  
**Independent experimenter:** [gnakan](https://community.databricks.com/t5/user/viewprofilepage/user-id/175114) (Databricks MVP)

## Research lineage

**Original research:** Shen Xu, [*Beyond Chat History: Designing Portable Memory and Decision Boundaries for Enterprise AI Agents*](https://community.databricks.com/t5/community-articles/beyond-chat-history-designing-portable-memory-and-decision/m-p/172381#M1815), Databricks Community, October 2026.

The article argues that persisted context, portable knowledge and authorization are separate architectural concerns. Its central distinction is that **memory can inform an agent's decision, but should not independently grant permission to act**. It identifies stale permissions and historical authorization as cases worth testing.

**Independent follow-up:** Databricks MVP **gnakan** [responded directly to the original article](https://community.databricks.com/t5/community-articles/beyond-chat-history-designing-portable-memory-and-decision/m-p/173115#M1825) and published [*Unity Catalog functions kept AI agents from acting on stale memory*](https://medium.com/lab-notes/unity-catalog-functions-kept-ai-agents-from-acting-on-stale-memory-7d63e15f992b), describing an experiment and linking lab notes / a test notebook.

## Experiment findings reported by the independent author

The author's published summary reports outcomes across **72 requests involving stale memory**:

| Authorization approach | Agent actions on stale memory, as reported |
| --- | ---: |
| Dated memory without an enforced current-policy check | 54 / 72 |
| Unity Catalog function made available as a policy-check tool | 6 / 72 |
| Authorization check enforced in application code | 0 / 72 |

These are the independent experimenter's reported figures, **not measurements collected or reproduced by Shen Xu**. Refer to the [independent write-up](https://medium.com/lab-notes/unity-catalog-functions-kept-ai-agents-from-acting-on-stale-memory-7d63e15f992b) for the experiment's design, test notebook and interpretation.

## Relevance and limits

This third-party work is a **technical follow-up to a specific research question**: an agent's recollection of historical permission should not replace verification of current authority at execution time. The reported reduction in stale-memory actions when checks are enforced is consistent with that narrow architectural distinction.

It is **not** a validation of the complete Decision Authority Economy (DAE), Agentic Search Optimization (ASO), or A2A Commerce frameworks. It is not a peer-reviewed academic replication, a Databricks corporate endorsement, or a benchmark of the full four-layer portable-memory architecture. Scope and results should be attributed to the independent experimenter.

## Primary links

- [Shen Xu — original Databricks research article](https://community.databricks.com/t5/community-articles/beyond-chat-history-designing-portable-memory-and-decision/m-p/172381#M1815)
- [gnakan — direct Databricks community response mentioning Shen Xu](https://community.databricks.com/t5/community-articles/beyond-chat-history-designing-portable-memory-and-decision/m-p/173115#M1825)
- [gnakan — independent experiment, lab notes and test notebook reference](https://medium.com/lab-notes/unity-catalog-functions-kept-ai-agents-from-acting-on-stale-memory-7d63e15f992b)

[Back to the research home](index.md) · [Decision Authority Economy](decision-authority.md) · [Publications](publications.md)
