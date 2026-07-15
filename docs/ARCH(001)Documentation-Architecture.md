# ARCH-001: Documentation Architecture

## Purpose

This document defines the documentation architecture of the project. It establishes the responsibility, scope, and relationship of each documentation artifact, ensuring that both developers and AI agents have a single, consistent source of truth.

---

# Scope

This architecture covers the following documentation artifacts:

* README
* Specification (SPEC)
* Architecture Design (ARCH)
* Architecture Decision Record (ADR)
* File Header
* Class Documentation
* Function Documentation
* Commit Message

---

# Documentation Hierarchy

```text
Repository
│
├── README
├── SPEC
├── ARCH
├── ADR
│
└── Source Code
    ├── File Header
    ├── Class Documentation
    └── Function Documentation

Version Control
└── Commit History
```

---

# Documentation Responsibilities

## README

### Responsibility

Provides the project entry point.

### Contents

* Project overview
* Features
* Installation
* Build
* Usage
* Repository structure
* Documentation index

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |     ✓    |
| How          |  Partial |
| Why          |     —    |
| What Changed |     —    |

---

## SPEC

### Responsibility

Defines functional requirements and expected behavior.

### Contents

* Goals
* Requirements
* Acceptance Criteria
* Constraints
* Test Scenarios

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |     ✓    |
| How          |  Partial |
| Why          |     —    |
| What Changed |     —    |

---

## ARCH

### Responsibility

Describes the system architecture and implementation strategy.

### Contents

* Components
* Responsibilities
* Interfaces
* Data Flow
* Dependencies
* Design Principles

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |  Partial |
| How          |     ✓    |
| Why          |     —    |
| What Changed |     —    |

---

## ADR

### Responsibility

Records significant architectural decisions and their rationale.

### Contents

* Context
* Decision
* Alternatives
* Consequences

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |  Partial |
| How          |  Partial |
| Why          |     ✓    |
| What Changed |     —    |

---

## File Header

### Responsibility

Defines the purpose and scope of a source file.

### Typical Contents

* Purpose
* Responsibilities
* Dependencies
* Related Modules

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |     ✓    |
| How          |  Partial |
| Why          |     —    |
| What Changed |     —    |

---

## Class Documentation

### Responsibility

Defines the responsibility and collaboration contract of a class.

### Typical Contents

* Responsibility
* Ownership
* Collaboration
* Invariants
* Lifecycle

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |     ✓    |
| How          |  Partial |
| Why          |     —    |
| What Changed |     —    |

---

## Function Documentation

### Responsibility

Defines the contract of a function.

### Typical Contents

* Purpose
* Parameters
* Return Value
* Preconditions
* Postconditions
* Exceptions
* Complexity

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |     ✓    |
| How          |     ✓    |
| Why          |     —    |
| What Changed |     —    |

---

## Commit Message

### Responsibility

Documents the intent of a change.

### Typical Contents

* Type
* Scope
* Summary
* Motivation (optional)

### Primary Questions

| Question     | Coverage |
| ------------ | :------: |
| What         |  Partial |
| How          |  Partial |
| Why          |  Partial |
| What Changed |     ✓    |

---

# Coverage Matrix

| Artifact               | What | How | Why | What Changed |
| ---------------------- | :--: | :-: | :-: | :----------: |
| README                 |   ✓  |  ◐  |  —  |       —      |
| SPEC                   |   ✓  |  ◐  |  —  |       —      |
| ARCH                   |   ◐  |  ✓  |  —  |       —      |
| ADR                    |   ◐  |  ◐  |  ✓  |       —      |
| File Header            |   ✓  |  ◐  |  —  |       —      |
| Class Documentation    |   ✓  |  ◐  |  —  |       —      |
| Function Documentation |   ✓  |  ✓  |  —  |       —      |
| Commit Message         |   ◐  |  ◐  |  ◐  |       ✓      |

---

# Architectural Relationships

```text
README
   │
   ▼
SPEC
   │
   ▼
ARCH
   │
   ▼
Source Code
├── File Header
├── Class Documentation
└── Function Documentation
   │
   ▼
Commit History
```

Architectural Decision Records are orthogonal to the documentation hierarchy. They capture the rationale behind significant architectural choices and may reference any layer of the system.

```text
                 ADR
           ┌─────┼─────┐
           ▼     ▼     ▼
         SPEC   ARCH   Source Code
```

---

# Summary

The documentation architecture answers four complementary questions:

* **What** should the system do? → README, SPEC
* **How** is the system designed and implemented? → ARCH, Source Code Documentation
* **Why** was a design decision made? → ADR
* **What Changed** over time? → Commit History
