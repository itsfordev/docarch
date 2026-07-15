# DOCSPEC: Class Documentation Standard

## Overview

This document defines the standard structure, purpose, and writing conventions for class documentation within the project.

Class documentation describes the **architectural responsibility**, **contract**, and **collaboration** of a class. It explains the role of a class within the system without exposing implementation details.

A class document should answer **what the class represents**, **what responsibility it owns**, and **how it collaborates with other components**.

---

# Purpose

The purpose of class documentation is to:

* Define the responsibility of a class.
* Document its public contract.
* Describe ownership and lifecycle.
* Explain collaborations with other classes.
* Document design invariants.
* Help developers and AI agents understand the class before reading its implementation.

---

# Scope

This standard applies to:

* Public classes
* Internal classes
* Abstract base classes
* Interfaces
* Template classes
* Singleton classes
* Service classes
* Manager classes

It does not apply to:

* Local classes
* Anonymous classes
* Compiler-generated types

---

# Required Sections

## 1. Class

The class name.

Example

```text
StorageManager
```

---

## 2. Summary

A short description of the class.

The summary should answer:

* What is this class?
* Why does it exist?

---

## 3. Responsibility

Describe the single primary responsibility of the class.

Examples:

* Coordinates storage operations.
* Manages plugin lifecycle.
* Represents parser configuration.

Avoid describing implementation details.

---

## 4. Architectural Role

Describe where the class belongs.

Examples:

* Kernel
* Storage Layer
* Infrastructure
* Parser
* CLI
* Plugin Framework

---

## 5. Public Responsibilities

Describe the responsibilities exposed through the public interface.

Examples:

* Load configuration.
* Save state.
* Register plugins.

---

## 6. Collaboration

List major collaborators.

For each collaborator briefly describe the relationship.

Example:

```text
ConfigManager
    Provides runtime configuration.

StorageBackend
    Performs persistent storage.
```

---

## 7. Ownership

Describe ownership responsibilities.

Examples:

* Owns StorageBackend.
* References Logger.
* Does not own Plugin instances.

---

## 8. Lifetime

Describe object lifetime.

Examples:

* Process lifetime.
* Session lifetime.
* Request lifetime.
* Stack allocated.
* Singleton.

---

## 9. Invariants

Document conditions that must always remain true.

Examples:

* Configuration is loaded before initialization.
* Storage backend is never null.
* Plugin identifiers are unique.

---

## 10. Thread Safety

Document concurrency guarantees.

Examples:

* Thread-safe.
* Not thread-safe.
* External synchronization required.

---

## 11. Related Documents

Reference associated documentation.

Examples:

* SPEC
* ARCH
* ADR
* API

---

# Optional Sections

Include when appropriate.

## State Model

Describe object states.

---

## Extension Points

Document supported extension mechanisms.

---

## Error Handling

Describe the class error model.

---

## Performance Notes

Architectural performance considerations.

---

## Limitations

Known design limitations.

---

## Future Work

Planned architectural improvements.

---

# Writing Guidelines

Class documentation should:

* Describe **responsibility**, not implementation.
* Follow the Single Responsibility Principle.
* Avoid documenting private member variables.
* Avoid describing algorithms.
* Avoid documenting every public method.
* Use architectural terminology.
* Remain stable as implementation evolves.
* Be updated whenever the class responsibility changes.

---

# Template

```text
/**
 * Class
 * -----
 * <Class Name>
 *
 * Summary
 * -------
 * <Short description>
 *
 * Responsibility
 * --------------
 * <Primary responsibility>
 *
 * Architectural Role
 * ------------------
 * <Layer / Component>
 *
 * Public Responsibilities
 * -----------------------
 * - ...
 *
 * Collaboration
 * -------------
 * - ClassA : ...
 * - ClassB : ...
 *
 * Ownership
 * ---------
 * ...
 *
 * Lifetime
 * --------
 * ...
 *
 * Invariants
 * ----------
 * ...
 *
 * Thread Safety
 * -------------
 * ...
 *
 * Related Documents
 * -----------------
 * - SPEC-...
 * - ARCH-...
 * - ADR-...
 */
```

---

# Best Practices

* One primary responsibility per class.
* Keep documentation independent of implementation.
* Document collaboration rather than call sequences.
* Document architectural constraints explicitly.
* Prefer references to ARCH documents over duplicated explanations.
* Keep invariants synchronized with implementation.
* Keep ownership rules explicit.

---

# Relationship to Other Documents

| Document               | Responsibility                            |
| ---------------------- | ----------------------------------------- |
| README                 | Project overview                          |
| SPEC                   | Defines required behavior                 |
| ARCH                   | Defines architecture                      |
| ADR                    | Explains architectural decisions          |
| File Header            | Defines file responsibility               |
| Class Documentation    | Defines class responsibility and contract |
| Function Documentation | Defines operation contracts               |
| Source Code            | Implements the documented behavior        |

---

# Question Coverage

| Question     | Coverage  |
| ------------ | --------- |
| What         | ✓ Primary |
| How          | Partial   |
| Why          | —         |
| What Changed | —         |

---

# References

* Project Documentation Standard
* Documentation Architecture (ARCH)
* File Header Standard
* Function Documentation Standard
* SOLID Principles
* C++ Core Guidelines
