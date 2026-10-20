---
layout: default
title: Decision Authority Economy
description: Decision rights, authorization and accountability in AI agent systems.
---
# Decision Authority Economy (DAE)

**Shen Xu (徐慎)** · [Home](index.md) · [Unified framework](framework.md)

DAE examines how the capacity and legitimacy to make commercial decisions are allocated among people, organizations and AI agents.

## Working distinctions

1. **Information access:** retrieve and interpret information.
2. **Recommendation:** suggest options without authority to decide.
3. **Bounded selection:** choose within an authorized scope.
4. **Authorized execution:** perform specific permitted actions.
5. **Continuing delegated discretion:** make bounded decisions over time with oversight and revocation.

These are proposed analytical distinctions, not a settled external taxonomy. An agent's autonomy label is not evidence of its actual permissions.

## Context, discretion and authority — IBM TechXchange Community (October 2026)

In [*Decision Authority in AI Agents: Why Context Matters More Than Automation*](https://community.ibm.com/community/user/blogs/shen-xu/2026/10/13/decision-authority-in-ai-agents), Shen Xu distinguishes the ability to execute predefined actions from the delegated discretion to interpret competing objectives. Access to contextual evidence is not itself an authorization to disregard an existing instruction. Likewise, a model's judgment about what to do and the authority to take the action must be evaluated separately.

The article illustrates this boundary with subscription renewal and enterprise procurement scenarios, including conflicts among standing permissions, retrieved memories and evolving user goals. Decision Authority is treated as a dynamic relationship among human intent, rules, permissions, context and consequential action—not a single autonomy threshold.

[Structured research note and decision workflow](notes/2026-10-13-ibm-decision-authority.md). This is author-published conceptual technical writing on an IBM community platform, not independent validation or an IBM endorsement.

## Memory is not authority

Persistent context and preferences can inform a choice, but cannot alone grant permission to purchase, disclose, or execute. Authorization must be scoped and evaluated separately.

**Selected technical investigations**
- [Beyond Chat History: Designing Portable Memory and Decision Boundaries for Enterprise AI Agents — Databricks Community](https://community.databricks.com/t5/community-articles/beyond-chat-history-designing-portable-memory-and-decision/td-p/172381)
- [Portable AI Agent Memory: What Should Move When Users Switch Agents? — DEV Community](https://dev.to/shen_xu/portable-ai-agent-memory-what-should-move-when-users-switch-agents-900)

The two articles above are by Shen Xu and should not be presented as independent validation.

## Independent technical follow-up — October 2026

Databricks MVP **gnakan** [replied to the Databricks article](https://community.databricks.com/t5/community-articles/beyond-chat-history-designing-portable-memory-and-decision/m-p/173115#M1825) and published [an independent Unity Catalog policy-check experiment](https://medium.com/lab-notes/unity-catalog-functions-kept-ai-agents-from-acting-on-stale-memory-7d63e15f992b). The author's reported stale-memory outcomes were **54/72** without an enforced check, **6/72** with a check available as a tool, and **0/72** with authorization enforced in application code.

The finding is consistent with this page's distinction between **remembered information** and **current authorization**. It addresses one technical proposition, **not the whole DAE framework**, and should not be presented as peer-reviewed replication or Databricks endorsement.

[Research provenance, experiment summary and source links](independent-research.md)

[Research directory](publications.md)
