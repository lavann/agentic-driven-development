---
title: "The AI Agent Operating Model"
subtitle: "Roles, boundaries, and governance for repeatable AI-agent delivery"
description: "A vendor-neutral whitepaper on organizing AI agents into a governed software delivery operating model."
author: "Lavan"
date: "2026-05-31"
version: "1.0"
status: "Public whitepaper"
audience:
  - engineering leaders
  - platform teams
  - delivery leaders
  - software architects
  - technology executives
tags:
  - ai-agents
  - operating-model
  - software-delivery
  - engineering-governance
publication_note: "Personal technical perspective. Not an official product statement or employer position."
---

# The AI Agent Operating Model

## Roles, Boundaries, and Governance for Repeatable AI-Agent Delivery

### Executive Summary

Most organizations begin their AI-agent journey with individual productivity experiments. A developer asks an assistant to explain code, write a test, or draft a function. This is useful, but it does not create a repeatable delivery capability.

To scale, organizations need an AI agent operating model: a way to assign work, define roles, review output, manage risk, and learn from every run.

The goal is not to make agents autonomous in the abstract. The goal is to make agent work safe, visible, repeatable, and valuable.

---

## 1. Why an Operating Model Is Needed

AI agents can inspect code, write files, open pull requests, update documentation, and suggest next actions. Without an operating model, this creates several risks:

- unclear ownership;
- inconsistent output quality;
- duplicated work;
- hidden assumptions;
- review overload;
- drift between code and documentation;
- experiments becoming production without evidence.

An operating model turns agent usage from ad hoc assistance into managed delivery.

---

## 2. Core Components

### 2.1 Work Intake

Agent work should begin from a clear request or issue. The request defines the objective, evidence boundary, allowed changes, stop conditions, and expected output.

### 2.2 Role Assignment

Different work needs different agent roles. Planning, implementation, testing, documentation, and evaluation should not be casually merged into one task.

### 2.3 Execution Boundary

Each agent run should define what files, systems, tools, and decisions are in scope.

### 2.4 Review Surface

Agent output needs a reviewable surface: pull request, report, decision record, test result, or documentation change.

### 2.5 Learning Loop

Repeated corrections should become templates, scripts, checks, or new operating rules.

---

## 3. Agent Roles

| Role | Responsibility | Human review focus |
|---|---|---|
| Explorer | Inspect evidence and answer questions | Accuracy and source grounding |
| Documenter | Produce current-state documentation | Completeness and clarity |
| Orchestrator | Select next safe action | Sequencing and risk |
| Designer | Propose target state or buildout | Trade-offs and assumptions |
| Implementer | Make scoped changes | Correctness and tests |
| Tester | Add or improve validation | Behavior coverage |
| Security reviewer | Assess risk and controls | Threats and gaps |
| Evaluator | Review completed slices | Scope, rollback, residual risk |

Roles can be implemented by people, agents, or a combination. The important point is separation of responsibility.

---

## 4. Human Responsibilities

Humans remain accountable for:

- setting intent;
- prioritizing work;
- accepting risk;
- approving scope expansion;
- merging or rejecting output;
- making business trade-offs;
- deciding when evidence is sufficient.

Agents can recommend. Humans decide.

---

## 5. Agent Responsibilities

Agents should:

- stay within scope;
- cite evidence;
- state uncertainty;
- stop when blocked;
- validate outputs;
- avoid changing forbidden files;
- keep review surfaces clear;
- avoid turning assumptions into facts.

This should be encoded in prompts, issue templates, and automated checks.

---

## 6. Governance Gates

Use gates where the risk changes.

Approval should be required for:

- production behavior changes;
- schema or data migration;
- security posture changes;
- broad refactors;
- infrastructure provisioning;
- unclear rollback;
- conflicting evidence.

Routine documentation, analysis, and small test additions may need lighter review, but still need traceability.

---

## 7. Operating Metrics

Measure agent work by accepted outcomes, not generated output.

Recommended metrics:

- accepted PR rate;
- repair count;
- scope violation rate;
- validation pass rate;
- review time;
- retry rate;
- evidence completeness;
- cost per accepted outcome;
- repeated-failure reduction.

These metrics show whether the system is improving, not just whether agents are busy.

---

## 8. Adoption Pattern

Start small:

1. use agents for documentation and analysis;
2. add issue templates and output contracts;
3. introduce scoped implementation tasks;
4. add evaluation and review roles;
5. automate validation and drift checks;
6. promote proven patterns into operating rules.

Avoid starting with broad autonomous implementation. The review burden can erase the benefit.

---

## Conclusion

An AI agent operating model is the bridge between individual productivity and organizational capability.

The organizations that succeed will not be those that simply allow more agent autonomy. They will be those that define roles, boundaries, evidence standards, review gates, and learning loops clearly enough that agent work becomes dependable.

---

## Field Evidence (Anonymised)

Anonymised observations from real engagements. They illustrate repeatability, not a fixed template.

**The same pattern, re-applied faster.** A "migration factory" operating pattern was first proven at an **Online Retailer** and then re-applied - more quickly - at an **Automotive Manufacturer**. The second engagement was faster precisely because it was a refined deployment of a proven pattern rather than a fresh start.

**Portable IP.** The assets that travelled between engagements were reusable playbooks, prompt libraries, and starter repositories. These are what turn a one-off success into an operating capability.

**Role separation as the spine.** Engagements consistently separated technical enablement, stakeholder and adoption work, and account context. The roles are described here by function, not by individual - the separation is what kept agent work governed as it scaled.

The evidence for an operating model is not a single fast project. It is the same model producing results again, with portable assets and clear role boundaries.
