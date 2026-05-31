---
title: "Evidence-Driven Modernization"
subtitle: "Modernizing software systems from observed facts, not assumptions"
description: "A vendor-neutral whitepaper on using evidence, confidence markers, and candidate slices to make modernization safer and more measurable."
author: "Lavan"
date: "2026-05-31"
version: "1.0"
status: "Public whitepaper"
audience:
  - engineering leaders
  - software architects
  - modernization teams
  - delivery leaders
  - technology executives
tags:
  - modernization
  - software-architecture
  - ai-agents
  - engineering-governance
  - evidence-based-delivery
publication_note: "Personal technical perspective. Not an official product statement or employer position."
---

# Evidence-Driven Modernization

## Modernizing Software Systems From Observed Facts, Not Assumptions

### Executive Summary

Modernization programs often begin with a target architecture and a sense of urgency. That is understandable, but it is not enough. A legacy estate is rarely just old code. It is a set of runtime assumptions, data dependencies, build constraints, operational habits, and business rules that have accumulated over time.

Evidence-driven modernization starts by making those facts visible. It treats the current system as evidence to be understood before it is changed. AI agents can help accelerate this work, but only if their output is grounded in source evidence and reviewed through a disciplined operating model.

The central principle is:

> Do not modernize what you have not first made observable.

---

## 1. Why Modernization Needs Evidence

Modernization risk often comes from unknown coupling. A system may appear to have independent modules, but share database tables, configuration, session state, identity assumptions, scheduled jobs, or deployment scripts. A change that looks small can fail because the real dependency graph is not documented.

Evidence-driven modernization addresses this by creating a current-state evidence base:

- repository inventory;
- runtime and deployment view;
- dependency graph;
- data ownership map;
- hotspot register;
- open-question register;
- candidate modernization slices;
- decision records;
- validation evidence.

This evidence base turns modernization from a speculative rewrite into a sequence of controlled decisions.

---

## 2. The Evidence Ladder

Modernization evidence should be built in layers.

### 2.1 Estate Census

Inventory repositories, languages, frameworks, solutions, projects, tests, build scripts, configuration, and runtime dependencies.

Output:

- what exists;
- what appears runnable;
- what is obsolete;
- where evidence is missing.

### 2.2 System Discovery

Explain how the system behaves today. This includes major flows, persistence, integration points, authentication, deployment assumptions, and operational constraints.

Output:

- current-state architecture;
- key runtime paths;
- integration inventory;
- build and deployment notes.

### 2.3 Domain Mapping

Identify business capabilities, bounded contexts, shared models, and seams. Technical modules do not always match domain boundaries.

Output:

- capability map;
- domain ownership;
- shared model risks;
- candidate seams.

### 2.4 Hotspots and Open Questions

Record risks and unknowns explicitly. Unknowns are not failures. Hidden unknowns are failures.

Output:

- hotspot register;
- open-question register;
- confidence markers;
- proposed resolution paths.

### 2.5 Candidate Slices

Convert evidence into small, reversible modernization actions. Each slice should have a value case, blast radius, dependency assessment, validation path, and rollback story.

Output:

- candidate slice catalogue;
- readiness score;
- next best action.

---

## 3. Confidence Markers

Modernization documents should distinguish what is known from what is inferred.

Recommended confidence markers:

- **observed**: directly supported by source code, configuration, logs, tests, or documented runtime evidence;
- **inferred**: reasoned from observed evidence;
- **assumption**: accepted temporarily for planning but not proven;
- **unknown**: unresolved and requiring investigation.

This prevents planning documents from turning uncertainty into false certainty.

---

## 4. Candidate Slice Scoring

A modernization slice should be scored before implementation.

Useful dimensions:

| Dimension | Question |
|---|---|
| Feasibility | Can the change be made with current evidence and skills? |
| Reversibility | Can it be rolled back cleanly? |
| Value | Does it reduce material business or technical risk? |
| Dependency unlock | Does it enable higher-value future work? |
| Blast radius | How much of the system can it affect? |
| Evidence quality | Are claims supported by observed facts? |

The highest-scoring slice is not always the best next action. A prerequisite that unlocks several blocked slices may be more valuable than a visible implementation.

---

## 5. AI Agents in Evidence-Driven Modernization

AI agents are useful when they accelerate evidence production:

- reading large codebases;
- summarizing modules;
- tracing call paths;
- identifying repeated patterns;
- drafting documentation;
- proposing candidate slices;
- generating tests;
- checking drift after changes.

They should not be treated as authorities. Agent output must remain reviewable, cited, and validated.

The best use of agents is to convert unknown systems into structured evidence faster than a human team could do unaided.

---

## 6. Governance Model

Evidence-driven modernization needs lightweight governance:

- all material claims cite evidence;
- all unknowns are tracked;
- all slices have rollback notes;
- all implementation work follows a planning decision;
- all completed slices are evaluated;
- documentation is refreshed after changes;
- decision records remain append-only or versioned.

Governance should make delivery faster by reducing ambiguity, not slower by adding ceremony.

---

## 7. Expected Impact

Evidence-driven modernization improves:

- prioritization;
- review quality;
- stakeholder confidence;
- risk visibility;
- sequencing discipline;
- agent reliability;
- onboarding speed;
- auditability.

The biggest benefit is avoiding expensive wrong turns. A well-evidenced small step often beats a large transformation plan built on assumptions.

---

## 8. Minimum Viable Standard

Before starting a modernization implementation, require:

- current-state inventory;
- known runtime dependencies;
- open-question register;
- hotspot register;
- candidate slice scoring;
- rollback strategy;
- validation plan;
- human approval for risk acceptance.

This is enough to begin safely without waiting for a perfect architecture document.

---

## Conclusion

Modernization is not primarily a coding problem. It is a knowledge, risk, and sequencing problem.

AI agents can accelerate modernization when they are used to build and maintain the evidence base. The teams that benefit most will be those that combine agent speed with evidence discipline, small slices, clear confidence markers, and reviewable decisions.
