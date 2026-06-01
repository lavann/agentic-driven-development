---
title: "Agentic-Driven Development"
subtitle: "A practical whitepaper for building software with AI agents"
description: "A vendor-neutral framework for using AI agents in software delivery while preserving engineering control, evidence, and accountability."
author: "Lavan"
date: "2026-05-31"
version: "1.0"
status: "Public whitepaper"
audience:
  - engineering leaders
  - software architects
  - platform teams
  - delivery leaders
  - technology executives
tags:
  - ai-agents
  - software-engineering
  - engineering-leadership
  - delivery-governance
  - prompt-engineering
publication_note: "Personal technical perspective. Not an official product statement or employer position."
---

# Agentic-Driven Development

## A Practical Whitepaper for Building Software with AI Agents

### Executive Summary

AI agents are changing software delivery. The shift is larger than autocomplete and broader than chat-based assistance. Teams are beginning to delegate bounded engineering work to agents: repository analysis, documentation, test generation, refactoring, migration planning, pull request preparation, and evidence collection.

This creates a new delivery model: **agentic-driven development**.

Agentic-driven development is the disciplined use of AI agents as participants in the software delivery lifecycle. It is not unmanaged automation, and it is not a replacement for engineering judgement. It is a way to increase delivery throughput by combining human intent, agent execution, structured evidence, and controlled review loops.

The central claim of this paper is simple:

> The value of AI agents in software delivery depends less on how much autonomy they have, and more on how well their work is bounded, evidenced, reviewed, and integrated.

Organizations that treat agents as uncontrolled coding assistants will see uneven quality and governance risk. Organizations that treat agents as part of an engineered delivery system can improve speed while preserving accountability.

---

## 1. What Is Agentic-Driven Development?

Agentic-driven development is a software delivery approach in which AI agents perform bounded engineering tasks inside a governed workflow.

In this model, agents may:

- inspect a codebase;
- summarize current-state architecture;
- identify candidate slices of work;
- draft implementation plans;
- generate tests;
- make scoped code changes;
- prepare pull requests;
- update documentation;
- collect validation evidence;
- propose next actions.

Humans remain responsible for intent, prioritization, approval, risk acceptance, and final accountability.

The model differs from traditional automation because agents can interpret context, make plans, and adapt within a defined boundary. It differs from ad hoc AI assistance because the agent's work is tracked, reviewed, and measured as part of the delivery system.

---

## 2. Why This Matters Now

Software teams face a familiar set of pressures:

- growing legacy estates;
- dependency and security maintenance;
- shortage of specialist knowledge;
- demand for faster modernization;
- pressure to improve engineering productivity;
- increasing governance expectations around AI use.

AI agents can help, but only if they are used with discipline. A model that can generate code quickly can also generate incorrect assumptions quickly. A tool that can open a pull request can also create review burden, hidden drift, or false confidence.

The opportunity is not simply faster coding. The larger opportunity is faster **evidence production**: turning unclear systems into understandable maps, turning vague risks into testable findings, and turning broad modernization goals into sequenced, reviewable slices.

---

## 3. From Developer Assistance to Delivery System

Most teams begin with individual assistance:

- explain this function;
- write this unit test;
- draft this API;
- refactor this method.

That is useful, but it does not by itself create a new delivery model. Agentic-driven development begins when agent work becomes part of a repeatable system.

That system needs:

1. clear work intake;
2. bounded task scope;
3. explicit evidence inputs;
4. rules for allowed and forbidden changes;
5. validation gates;
6. pull request review;
7. decision records;
8. feedback into future tasks.

Without these controls, agent output becomes another form of unmanaged work in progress.

---

## 4. The Agentic Delivery Loop

A mature agentic workflow follows a loop.

### 4.1 Intent

A human defines the objective. The objective should be specific enough to constrain agent action.

Weak intent:

```text
Improve the service.
```

Better intent:

```text
Identify the next safest modernization slice that improves deployability without changing runtime behavior.
```

### 4.2 Context

The agent receives relevant evidence: files, documentation, issue history, tests, architecture notes, logs, or prior decision records.

The context should be sufficient but not unbounded. Too little context causes hallucination. Too much context creates noise and cost.

### 4.3 Delegation

The task is delegated with a clear contract:

- objective;
- allowed files;
- forbidden files;
- expected outputs;
- validation commands;
- stop conditions;
- confidence requirements.

### 4.4 Execution

The agent performs the task within the boundary. It should stop when it lacks evidence, encounters conflicting instructions, or would need to exceed the approved scope.

### 4.5 Evidence

The agent records what it observed, what it inferred, what remains unknown, and what validation was run.

### 4.6 Review

A human or independent reviewer checks the output. Review should focus on correctness, scope discipline, evidence quality, rollback, and test coverage.

### 4.7 Integration

Accepted work is merged or published. Rejected work is corrected, closed, or converted into a learning record.

### 4.8 Learning

Patterns from the run are fed back into future prompts, templates, tests, and governance.

---

## 5. Work Units: Issues, Pull Requests, and Dispatches

Agentic-driven development benefits from treating work as explicit units.

### 5.1 Issue

The issue describes the task and the contract. It is the handoff from human intent to agent execution.

An effective issue includes:

- objective;
- source evidence;
- scope;
- stop conditions;
- expected output;
- review criteria.

### 5.2 Dispatch

The dispatch is the act of assigning work to an agent. It should record which agent or mode was used, what model class was selected if relevant, and what boundaries apply.

### 5.3 Pull Request

The pull request is the review surface. It should not simply say that work was done. It should show:

- what changed;
- why it changed;
- which evidence was used;
- what validation passed;
- what was not verified;
- what the rollback path is.

---

## 6. Principles of Agentic-Driven Development

### Principle 1: Bound the Work

Agents perform best when the task is explicit and scoped. Broad mandates increase the risk of unnecessary changes, hidden assumptions, and difficult reviews.

### Principle 2: Preserve Human Intent

The human defines the goal and accepts risk. The agent can recommend, draft, and execute bounded work, but it should not silently change the goal.

### Principle 3: Require Evidence

Every material claim should be tied to evidence. The distinction between observed, inferred, assumed, and unknown should be explicit.

### Principle 4: Prefer Small Slices

Small, reversible slices reduce risk and improve learning. Large agent-generated changes are difficult to review and harder to trust.

### Principle 5: Validate Before Confidence

Agent fluency is not evidence. Tests, builds, static checks, reviews, and source citations matter.

### Principle 6: Keep Rollback Visible

Every change should have a rollback story. If rollback is unclear, the task is probably too large or too risky.

### Principle 7: Separate Planning From Implementation

Design, orchestration, implementation, testing, and evaluation are different tasks. Combining them in one agent run often increases risk.

### Principle 8: Learn Mechanically

Repeated mistakes should become templates, checks, scripts, or workflow rules. Prose reminders alone are weak controls.

---

## 7. Agent Roles in the Delivery Lifecycle

Different work needs different agent roles.

| Role | Purpose | Typical output |
|---|---|---|
| Census agent | Inventory repository structure and technologies | Estate overview, dependency map |
| Documentation agent | Explain current behavior | System documentation |
| Domain agent | Identify business boundaries and seams | Domain model, candidate seams |
| Orchestrator agent | Choose the next safe action | Scorecard, delegation pack |
| Modernization agent | Design target state and migration path | Target architecture, buildout, plan |
| Implementation agent | Make one scoped change | Code PR, tests, execution record |
| Test agent | Build confidence around behavior | Test strategy, test cases, harness |
| Security agent | Assess controls and risk | Security posture, remediation plan |
| Evaluation agent | Review completed work | Slice evaluation, residual risk |
| Documentation refresh agent | Reduce drift after change | Updated docs and changelog |

Not every organization needs this exact taxonomy. The important pattern is role separation: planning agents should not casually implement, and implementation agents should not silently redefine architecture.

---

## 8. Governance Model

Agentic-driven development needs lightweight governance that travels with the work.

### 8.1 Scope Governance

Each task defines allowed and forbidden surfaces. For example:

- documentation only;
- tests only;
- one service only;
- no database schema changes;
- no infrastructure provisioning;
- no external network calls.

### 8.2 Evidence Governance

The workflow records:

- source files read;
- commands run;
- tests executed;
- decisions made;
- confidence markers;
- known gaps.

### 8.3 Approval Governance

Human approval is required when:

- risk exceeds the task boundary;
- production behavior may change;
- rollback is unclear;
- security posture is affected;
- data migration is involved;
- the agent encounters conflicting evidence.

### 8.4 Learning Governance

Patterns should be promoted carefully. A one-off success should not immediately become doctrine. Run experiments beside the known-good path, measure them, and promote only when evidence supports the change.

---

## 9. Prompt and Context Design

Agentic-driven development depends on high-quality context.

Strong task prompts include:

1. objective;
2. current state;
3. evidence boundary;
4. allowed changes;
5. forbidden changes;
6. validation commands;
7. stop conditions;
8. output format;
9. confidence rules;
10. review expectations.

The most important constraints should appear early. Long background material should be below the contract or retrievable by reference.

Context should be optimized, not maximized. The agent needs enough information to act correctly, not every available token.

---

## 10. Review and Quality Gates

Agent output should be reviewed with the same seriousness as human output, but with some additional checks.

Review questions:

- Did the agent stay within scope?
- Are claims backed by evidence?
- Did it modify any forbidden files?
- Are tests meaningful?
- Did validation actually run?
- Is rollback clear?
- Did it introduce hidden coupling?
- Did documentation and decision records stay in sync?
- Are unresolved questions visible?

Quality gates should be automated where possible:

- build and test checks;
- linting;
- PR body contract checks;
- required file checks;
- evidence record validation;
- secret scanning;
- dependency scanning.

---

## 11. Metrics for Agentic Delivery

The wrong metric is lines of code generated. The right metrics focus on accepted outcomes and reduced uncertainty.

Recommended metrics:

| Metric | Why it matters |
|---|---|
| Accepted PR rate | Measures usable output |
| Repair count | Tracks review burden |
| Cycle time | Measures delivery speed |
| Validation pass rate | Measures operational quality |
| Scope violation rate | Measures governance quality |
| Rollback clarity | Measures release safety |
| Evidence completeness | Measures auditability |
| Cost per accepted outcome | Measures economic value |
| Human review time | Measures actual productivity gain |
| Repeated-failure reduction | Measures learning |

Agentic development should reduce total delivery friction, not merely increase generated output.

---

## 12. Adoption Roadmap

### Phase 1: Assisted Engineering

Start with low-risk individual tasks:

- explanations;
- test suggestions;
- documentation drafts;
- small refactors;
- code review assistance.

Goal: build familiarity and identify safe patterns.

### Phase 2: Bounded Agent Tasks

Move to issue-based tasks with strict scope:

- documentation updates;
- test harness additions;
- dependency analysis;
- small code changes.

Goal: create repeatable agent contracts.

### Phase 3: Evidence-Driven Planning

Use agents to inventory systems, identify risks, and propose candidate slices.

Goal: turn ambiguous work into sequenced, evidence-backed actions.

### Phase 4: Controlled Implementation

Let agents implement small, reversible slices with validation and review.

Goal: increase delivery throughput without losing engineering control.

### Phase 5: Continuous Learning

Feed repeated review findings into templates, scripts, prompts, and checks.

Goal: make the system better over time.

---

## 13. Common Failure Modes

### 13.1 Vague Delegation

The agent receives a broad goal and invents scope.

Mitigation: explicit boundaries and stop conditions.

### 13.2 Confident But Unsupported Claims

The agent states conclusions without evidence.

Mitigation: confidence markers and source references.

### 13.3 Oversized Changes

The agent generates a large diff that is difficult to review.

Mitigation: small slices and file-level budgets.

### 13.4 Hidden Drift

Code, documentation, tests, and decision records diverge.

Mitigation: zero-drift checks and post-change documentation refresh.

### 13.5 Automation Without Accountability

The team treats agent output as self-validating.

Mitigation: human review and objective validation gates.

### 13.6 Experiment Becomes Production Too Quickly

A new agent pattern works once and is adopted everywhere.

Mitigation: dual-run experiments beside the known-good path before promotion.

---

## 14. A Minimum Viable Operating Standard

An organization starting agentic-driven development should require:

- issue-based work intake;
- explicit task scope;
- allowed and forbidden file surfaces;
- stop conditions;
- evidence references;
- validation commands;
- pull request review;
- rollback notes;
- post-run learning capture.

This standard is lightweight enough to adopt quickly but strong enough to prevent unmanaged automation.

---

## 15. Conclusion

Agentic-driven development is not about giving AI agents unlimited autonomy. It is about designing a delivery system where agents can contribute safely, visibly, and repeatedly.

The winning pattern is bounded autonomy:

- humans set intent;
- agents execute scoped work;
- evidence supports claims;
- validation gates protect quality;
- reviews preserve accountability;
- learning improves the system.

This is how AI moves from isolated developer assistance to a governed engineering capability.

---

## Field Evidence (Anonymised)

The following observations are drawn from real engagements. Names, and any sector detail that could identify a single organisation, have been removed; exact figures are banded. They are directional field evidence, not benchmarks.

**Supervised speed, not unmanaged autonomy.** In a four-week coding-agent proof of concept at a **Software Vendor**, effectively all development work was routed through the agent using review-and-refine loops, with manual intervention only where the agent lacked evidence or reached a boundary. The supervision was not a tax on speed - it was the mechanism that made the speed safe to accept. Editor-level assistance alone contributed roughly a 30% productivity uplift, before counting the larger delegated-agent work.

**Codifying the loop so it repeats.** At a **Wealth-Tech Platform**, a single team built a reusable editor agent and codified an upgrade procedure in an `agent.md` contract. This turned a manual, prompt-by-prompt task into an automated, repeatable upgrade with human checkpoints at each step - the operating pattern this paper describes, observed in practice.

The common thread: the agent moved fast, and humans stayed on the loop. Boundaries, review, and a codified contract were what allowed the output to be trusted.
