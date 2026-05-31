---
title: "Cost per Accepted Outcome"
subtitle: "The economic metric that matters for AI-agent delivery"
description: "A vendor-neutral whitepaper on measuring AI-agent economics by accepted engineering outcomes rather than token spend or generated output."
author: "Lavan"
date: "2026-05-31"
version: "1.0"
status: "Public whitepaper"
audience:
  - engineering leaders
  - finance leaders
  - platform teams
  - technology executives
tags:
  - ai-agents
  - engineering-metrics
  - cost-optimization
  - software-delivery
publication_note: "Personal technical perspective. Not an official product statement or employer position."
---

# Cost per Accepted Outcome

## The Economic Metric That Matters for AI-Agent Delivery

### Executive Summary

AI-agent economics are often discussed in terms of token costs, model prices, or generated lines of code. These are useful inputs, but they are not the real business metric.

The metric that matters is **cost per accepted outcome**.

An accepted outcome is a useful result that survives review and can be integrated into the delivery system: a merged pull request, an approved design, a validated test harness, a resolved incident report, or a decision record that stakeholders can trust.

The goal is not the cheapest model call. The goal is the lowest sustainable cost for useful, validated work.

---

## 1. Why Token Cost Is Not Enough

Token cost is visible and easy to measure. That makes it tempting as the main metric. But token spend alone misses several hidden costs:

- failed runs;
- retries;
- human repair time;
- review burden;
- incorrect assumptions;
- merge conflicts;
- downstream defects;
- documentation drift.

A run that is cheap but wrong is expensive. A run that costs more but produces accepted, validated work may be economically better.

---

## 2. Defining Accepted Outcome

An accepted outcome should meet three conditions:

1. It satisfies the task objective.
2. It passes required validation or review.
3. It can be used without major rework.

Examples:

| Workflow | Accepted outcome |
|---|---|
| Code change | Merged PR with tests passing |
| Documentation | Reviewed and published document |
| Architecture | Approved decision record |
| Testing | Test suite merged and runnable |
| Incident analysis | Reviewed timeline and action list |
| Modernization planning | Accepted next-action scorecard |

---

## 3. Formula

A simple starting formula:

```text
cost per accepted outcome = total workflow cost / accepted outcomes
```

Total workflow cost should include:

- model input and output cost;
- tool execution cost if material;
- human review time;
- human repair time;
- rerun cost;
- delay cost where measurable.

This does not need to be perfect to be useful. Even approximate measurement is better than optimizing token price alone.

---

## 4. Input Metrics

Recommended inputs:

| Metric | Meaning |
|---|---|
| Model cost | Direct model spend |
| Prompt size | Context cost pressure |
| Output size | Response cost pressure |
| Retry count | First-pass quality signal |
| Repair count | Human correction burden |
| Review time | Human cost |
| Validation pass rate | Quality signal |
| Accepted PR rate | Delivery signal |
| Defect escape rate | Downstream quality signal |
| Cycle time | Flow efficiency |

---

## 5. Why Generated Output Is Misleading

Generated code volume is a weak productivity metric. More code can mean more risk, more review, and more maintenance.

Better signals include:

- smaller accepted diffs;
- fewer repair comments;
- clearer evidence;
- better tests;
- faster review;
- easier rollback;
- reduced uncertainty.

Agentic delivery should improve flow, not inflate output.

---

## 6. Model Selection by Outcome

Different tasks deserve different models. The most capable model may be justified for ambiguous planning, architecture, or risk evaluation. Lower-cost models may be sufficient for mechanical edits, formatting, or repetitive documentation updates.

Route by outcome quality:

- reasoning-heavy tasks: optimize for correctness and judgement;
- mechanical tasks: optimize for cost and speed;
- high-risk tasks: optimize for evidence and reviewability;
- exploratory tasks: optimize for learning per unit cost.

---

## 7. Repair Burden

Repair burden is the silent cost of agentic delivery. A workflow may appear cheap until reviewers spend significant time correcting scope drift, missing evidence, bad PR bodies, or invalid assumptions.

Track:

- number of repair commits;
- number of review comments;
- type of repair;
- whether the error repeats;
- whether a template or check can prevent it.

Reducing repair burden often matters more than reducing raw token spend.

---

## 8. Applying the Metric

For each agent workflow, record:

```text
workflow: pull request generation
model cost: <amount>
review time: <minutes>
repair time: <minutes>
retries: <count>
validation: pass/fail
accepted: yes/no
```

Over time, compare patterns:

- which task types are profitable;
- which prompts cause repair;
- which models produce accepted work fastest;
- which validation gates prevent rework;
- which work should remain human-led.

---

## 9. Governance Use

Cost per accepted outcome helps leaders avoid two extremes:

- unrestricted agent usage with unclear value;
- over-restriction based only on token spend.

It supports better questions:

- Which workflows produce accepted output reliably?
- Which task types should use premium models?
- Where does human review time dominate cost?
- Which controls reduce rework?
- Which experiments should be promoted?

---

## Conclusion

AI-agent economics should be measured at the workflow level. Token costs matter, but only as part of the full path from task intent to accepted result.

Cost per accepted outcome gives engineering and finance leaders a shared language: not how much the model generated, but how much useful, validated work the system produced for the total cost invested.
