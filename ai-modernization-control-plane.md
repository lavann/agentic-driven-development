---
title: "Why AI Modernization Needs a Control Plane"
subtitle: "Coordinating agents, evidence, governance, and delivery over long-running change"
description: "A vendor-neutral whitepaper on why AI-enabled modernization programs need a control plane beyond coding agents."
author: "Lavan"
date: "2026-05-31"
version: "1.0"
status: "Public whitepaper"
audience:
  - technology executives
  - engineering leaders
  - modernization leaders
  - platform teams
  - software architects
tags:
  - modernization
  - ai-agents
  - control-plane
  - software-delivery
  - engineering-governance
publication_note: "Personal technical perspective. Not an official product statement or employer position."
---

# Why AI Modernization Needs a Control Plane

## Coordinating Agents, Evidence, Governance, and Delivery Over Long-Running Change

### Executive Summary

AI coding agents can accelerate individual tasks. Modernization programs need more than accelerated tasks. They need sequencing, evidence, memory, governance, review, and risk control across many tasks over time.

That requires a control plane.

An AI modernization control plane is the coordination layer that decides what should be done next, what evidence supports it, which agent role should do it, what must be reviewed, and how the result changes the program state.

Without a control plane, organizations risk turning AI into a faster way to create disconnected pull requests.

---

## 1. The Gap Between Coding and Modernization

Modernization is not just code generation. It involves:

- understanding current systems;
- mapping dependencies;
- identifying domain boundaries;
- sequencing safe slices;
- preserving behavior;
- creating tests;
- managing data and runtime risk;
- updating documentation;
- aligning stakeholders;
- deciding when evidence is sufficient.

Coding agents help with parts of this, but they do not automatically coordinate the whole program.

---

## 2. What a Control Plane Does

A control plane provides:

### 2.1 State

It records what is known, what is unknown, what has changed, and what is currently in progress.

### 2.2 Sequencing

It chooses the next safe action based on evidence, readiness, dependencies, and risk.

### 2.3 Delegation

It assigns work to the right role: analysis, documentation, design, implementation, testing, security, or evaluation.

### 2.4 Governance

It enforces scope boundaries, approval gates, validation requirements, and stop conditions.

### 2.5 Evidence

It records why decisions were made and what evidence supports them.

### 2.6 Learning

It turns repeated failures into improved templates, checks, and operating rules.

---

## 3. Core Control-Plane Artifacts

Useful artifacts include:

- estate overview;
- dependency graph;
- domain map;
- hotspot register;
- open-question register;
- candidate slice catalogue;
- next-action record;
- delegation pack;
- operator dashboard;
- slice scorecard;
- execution record;
- evaluation record;
- evidence record.

These artifacts create continuity across many agent runs.

---

## 4. Why Memory Matters

Modernization programs last longer than any single model session. Without durable memory, agents repeatedly rediscover the same facts or lose important decisions.

Control-plane memory should be tiered:

- concise current summary;
- detailed recent log;
- archived historical records;
- structured decision records;
- evidence hashes and source links.

The goal is not to remember everything in active context. The goal is to remember the right things in retrievable form.

---

## 5. The Next-Best-Action Problem

One of the most valuable control-plane functions is selecting the next best action.

This decision should consider:

- value;
- readiness;
- reversibility;
- blast radius;
- dependency unlock;
- evidence quality;
- validation path;
- human approval needs.

The best next action is often a prerequisite, test, or design artifact rather than an implementation slice.

---

## 6. Human-in-the-Loop Governance

The control plane should identify when human decision is required:

- operator input is missing;
- risk is high;
- target architecture has multiple viable options;
- rollback is unclear;
- data migration is involved;
- production behavior may change;
- evidence conflicts.

Human-in-the-loop does not mean humans do all work. It means humans make the decisions that require accountability.

---

## 7. Agent Roles Inside the Control Plane

A control plane coordinates specialist agents:

- census;
- discovery;
- domain modeling;
- architecture design;
- implementation;
- testing;
- security;
- evaluation;
- documentation refresh.

Each agent performs bounded work. The control plane maintains state and sequence.

---

## 8. Measuring Control-Plane Value

Useful metrics include:

- number of unknowns closed;
- number of safe slices delivered;
- rework avoided;
- conflict rate;
- evidence completeness;
- mean time to next action;
- review repair count;
- rollback clarity;
- cost per accepted outcome.

The control plane earns its place when it reduces uncertainty and prevents expensive wrong turns.

---

## Conclusion

AI modernization needs more than coding speed. It needs a system that can coordinate evidence, decisions, agents, and review over time.

The control plane is that system. It turns disconnected agent work into governed modernization progress.

---

## Field Evidence (Anonymised)

Anonymised observations from regulated-delivery engagements. Figures are banded; sectors that could identify a single organisation are generalised.

**Coverage as the trust gate.** At a **Global Bank**, roughly 80% unit-test coverage functioned as the confidence-and-compliance gate that allowed agentic speed to be trusted at scale. Without that gate, speed would have been a liability rather than an asset.

**Standards-compliant output under control.** At a **Financial-Markets Data Provider**, two parallel proofs of concept reached standards-compliant output in a regulatory-reporting format, complete with tests, logging, and documentation - reaching roughly 90% functional coverage within a three-week build. In a separate feeds programme, standards and compliance checks were embedded directly into automated transformation and validation, rather than bolted on afterwards.

**The counter-case.** Where speed is applied without a control plane - without a coverage gate, embedded compliance, and evidence records - the same agent capability that accelerates delivery can just as quickly produce unreviewed, non-compliant change at scale.

**Future work.** A concrete, publishable security-vulnerability example - where the control plane caught or prevented a defect before it reached production - would sharpen this section; it is deferred until a suitable anonymised case is available.
