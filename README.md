---
title: "Agentic-Driven Development"
description: "Public whitepapers on governed AI-agent software delivery, modernization, context optimization, and measurable delivery economics."
author: "Lavan"
date: "2026-05-31"
status: "Public index"
publication_note: "Personal technical perspective. Not an official product statement or employer position."
---

# Agentic-Driven Development

This repository contains public whitepapers on practical, governed use of AI agents in software delivery.

The common theme is simple: AI agents create value when their work is bounded, evidenced, measured, and reviewed. The goal is not unchecked autonomy. The goal is repeatable delivery with clear human intent, useful automation, and defensible engineering control.

## Whitepapers

### 1. [Agentic-Driven Development](agentic-driven-development.md)

**What**: A delivery model for using AI agents as participants in the software development lifecycle.

**Why**: Many teams are moving from individual AI assistance to delegated agent work: analysis, documentation, tests, pull requests, migration planning, and evidence collection. Without a delivery model, this can create drift, review burden, and false confidence.

**Impact**: Establishes a practical operating model for agentic software delivery: bounded tasks, issue-based work intake, evidence-backed claims, validation gates, pull request review, rollback discipline, and learning loops.

### 2. [AI Agent Cost Optimization](ai-agent-cost-optimization.md)

**What**: A framework for reducing the cost and latency of AI-agent workflows without losing evidence or governance.

**Why**: Agentic workflows often send large volumes of repeated tool output, logs, JSON, file trees, and conversation history to models. More context can mean higher cost, slower responses, and lower signal.

**Impact**: Defines practical methods for cost control: context budgets, reversible compression, stable prompt prefixes, evidence retrieval, workflow metrics, and cost-per-accepted-outcome measurement.

### 3. [Evidence-Driven Modernization](evidence-driven-modernization.md)

**What**: A modernization approach that starts from observed system evidence rather than assumptions, preferences, or target-state slogans.

**Why**: Modernization programs often fail when teams jump from codebase to solution without understanding dependencies, risks, data ownership, and runnable constraints.

**Impact**: Defines how to turn legacy estates into evidence maps, open questions, candidate slices, and sequenced decisions that can be reviewed and executed safely.

### 4. [The AI Agent Operating Model](ai-agent-operating-model.md)

**What**: A practical operating model for using AI agents across planning, implementation, testing, review, and documentation.

**Why**: Agents need roles, boundaries, review surfaces, and escalation rules. Without an operating model, organizations get isolated experiments rather than repeatable delivery.

**Impact**: Provides a role-based model for agent work, human approval gates, evidence standards, and continuous learning.

### 5. [Cost per Accepted Outcome](cost-per-accepted-outcome.md)

**What**: A measurement model for evaluating AI-agent economics by accepted engineering outcomes instead of raw token spend or generated code volume.

**Why**: Token reduction alone can be misleading. A cheap run that needs heavy repair is not economically better.

**Impact**: Introduces metrics for accepted PRs, repair count, validation pass rate, review time, retry rate, and cost per usable output.

### 6. [Reversible Context Compression](reversible-context-compression.md)

**What**: A method for reducing prompt size while preserving exact source evidence behind retrievable pointers.

**Why**: Summaries can lose the one detail that matters. Compression for engineering work must be auditable and reversible.

**Impact**: Defines source IDs, content hashes, retrieval records, no-compression zones, and shadow-run validation for context reduction.

### 7. [Why AI Modernization Needs a Control Plane](ai-modernization-control-plane.md)

**What**: A control-plane view of AI-enabled modernization programs.

**Why**: Coding agents alone do not solve sequencing, risk, evidence, governance, or long-running program memory.

**Impact**: Describes the coordination layer needed to turn agent output into governed modernization progress.

## How to Read These Papers

- Start with **Agentic-Driven Development** if you are thinking about delivery model, governance, and engineering operating rhythm.
- Read **The AI Agent Operating Model** if you need to organize roles, gates, and accountability.
- Read **Evidence-Driven Modernization** and **Why AI Modernization Needs a Control Plane** if you are applying agents to legacy or transformation work.
- Read **AI Agent Cost Optimization**, **Cost per Accepted Outcome**, and **Reversible Context Compression** if you are scaling agent usage and need to manage economics, context quality, and evidence preservation.

## Position

These papers are vendor-neutral and intended as public technical perspectives. They do not depend on proprietary customer data, internal implementation details, or any single model provider's roadmap.
