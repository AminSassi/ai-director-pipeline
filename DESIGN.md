# Design Philosophy

This document explains why the repository is structured the way it is. Contributors should read this before making changes.

---

## Core Principles

### 1. Modular, Not Monolithic

The repository is split into small, focused modules (camera/, style/, knowledge/, routing/, etc.) instead of one giant prompt file.

**Why:** LLMs behave better with focused instructions. A 4,000-line system prompt loses influence over time. Small, loaded-on-demand modules stay authoritative.

**Never:** Merge modules into one file. This destroys the architecture.

### 2. Deterministic Workflow

Every phase has explicit input, output, allowed actions, forbidden actions, and exit conditions.

**Why:** LLMs drift when instructions are prose. Contracts are harder to misinterpret than narratives.

**Never:** Replace contracts with "do your best" instructions.

### 3. Immutable Artifacts

Each phase produces a file. No phase recreates earlier artifacts from memory.

**Why:** This prevents accidental data loss and makes the pipeline auditable. You can always trace what changed and when.

**Never:** Let an agent regenerate an earlier artifact without explicit confirmation.

### 4. State-Aware Execution

Before any action, the agent checks the current state and whether the request requires a phase transition.

**Why:** This prevents workflow drift—the #1 cause of agent failure in multi-step pipelines.

**Never:** Allow "continue" or "paste" to reopen completed phases.

### 5. Compression Is Editing

Compression performs deterministic edits on existing text. It never regenerates, rewrites, or invents sentences.

**Why:** Writing and editing are fundamentally different tasks. Mixing them causes the word-count spiral problem.

**Never:** Let compression become rewriting.

---

## Rule Separation

The repository separates two types of rules:

### Creative Rules (How to Think)
- `knowledge/critical-rules.md` — production principles
- `camera/angles.md` — camera reference
- `style/rules.md` — visual style
- `knowledge/additional-rules.md` — director's rules

### Execution Rules (How to Work)
- `AGENTS.md` — bootstrap, pipeline rules, workflow
- `knowledge/workflow.md` — phase contracts, state guard
- `tests/regression-tests.md` — behavioral tests

**Why:** Creative rules and execution rules serve different purposes. Mixing them makes both harder to maintain.

**Never:** Put workflow rules in knowledge files, or creative rules in workflow files.

---

## What Contributors Should Never Change

1. **The bootstrap sequence** — It's the entrypoint. Breaking it breaks everything.
2. **The artifact naming convention** — Phase-0-script.md, phase-0.1-script-with-ctas.md, etc.
3. **The invalidation model** — Changing a phase invalidates all downstream phases.
4. **The compression algorithm** — 5-pass deterministic editing, not rewriting.
5. **The state guard** — Check state before every action.

These are architectural invariants. Everything else can evolve.

---

## Versioning

The repository uses semantic versioning (MAJOR.MINOR.PATCH).

- **MAJOR:** Breaking change to workflow or artifact format
- **MINOR:** New feature (new routing type, new module)
- **PATCH:** Bug fix, documentation update

See CHANGELOG.md for history.
