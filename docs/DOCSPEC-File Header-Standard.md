# DOCSPEC: File Header Standard

## Overview

This document defines the standard structure, purpose, and writing conventions for source file headers within the project.

A File Header provides a concise description of a source file's responsibility, its role within the architecture, and its relationship to other components. It is intended to help developers and AI agents understand a file before reading its implementation.

A File Header should describe **what the file is responsible for**, not how it is implemented.

---

# Purpose

The purpose of a File Header is to:

* Identify the responsibility of a source file.
* Define its architectural role.
* Describe its public purpose.
* Document important dependencies.
* Provide navigation to related documentation.

---

# Scope

This standard applies to:

* Source files (`.cpp`, `.c`, `.cc`)
* Header files (`.h`, `.hpp`)
* Implementation files
* Entry-point files
* Public interface files

It does **not** apply to:

* Generated code
* Third-party libraries
* Vendor code

---

# Required Sections

## 1. File

The relative file path.

Example

```text
File: src/storage/storage_manager.cpp
```

---

## 2. Summary

A one- or two-sentence description of the file.

The summary should answer:

* What is this file?
* Why does it exist?

---

## 3. Responsibility

Describe the primary responsibility of the file.

A file should have a single primary responsibility.

Examples:

* Implements the storage manager.
* Provides configuration loading.
* Defines the plugin interface.

---

## 4. Architectural Role

Describe where the file belongs within the architecture.

Examples:

* Kernel Component
* Storage Layer
* Infrastructure
* CLI
* Plugin System

---

## 5. Public Contents

List the major public elements defined by the file.

Examples:

* Classes
* Interfaces
* Functions
* Constants
* Enumerations

Do not list private implementation details.

---

## 6. Dependencies

Document significant dependencies.

Include only architectural dependencies.

Examples:

* ConfigManager
* StorageBackend
* Logger

---

## 7. Related Documents

Reference associated documentation.

Examples:

* SPEC
* ARCH
* ADR
* API

---

# Optional Sections

Include when appropriate.

## Notes

Important implementation-independent information.

---

## Thread Safety

Concurrency guarantees.

---

## Lifetime

Object lifetime expectations.

---

## Ownership

Ownership model for resources.

---

## Limitations

Known limitations.

---

## Future Work

Planned improvements.

---

# Writing Guidelines

A File Header should:

* Be concise.
* Describe responsibility rather than implementation.
* Avoid algorithm descriptions.
* Avoid code duplication.
* Avoid historical information.
* Avoid documenting private implementation details.
* Be updated whenever the architectural responsibility changes.

Prefer architectural terminology over implementation terminology.

---

# Template

```text
/******************************************************************************
 * File
 * ----
 * <relative file path>
 *
 * Summary
 * -------
 * <Short description of the file>
 *
 * Responsibility
 * --------------
 * <Primary responsibility>
 *
 * Architectural Role
 * ------------------
 * <Layer / Component / Module>
 *
 * Public Contents
 * ---------------
 * - ClassA
 * - InterfaceB
 * - FunctionC()
 *
 * Dependencies
 * ------------
 * - ConfigManager
 * - Logger
 *
 * Related Documents
 * -----------------
 * - SPEC-...
 * - ARCH-...
 * - ADR-...
 ******************************************************************************/
```

---

# Best Practices

* One responsibility per file.
* Keep the summary under three sentences.
* List only architecturally relevant dependencies.
* Prefer linking to documentation instead of repeating it.
* Keep implementation details inside the code, not the header.
* Keep the header synchronized with the file's actual responsibility.

---

# Relationship to Other Documents

| Document               | Responsibility                                |
| ---------------------- | --------------------------------------------- |
| README                 | Introduces the project                        |
| SPEC                   | Defines functional requirements               |
| ARCH                   | Defines architectural structure               |
| ADR                    | Explains architectural decisions              |
| File Header            | Defines the responsibility of one source file |
| Class Documentation    | Defines class responsibilities                |
| Function Documentation | Defines function contracts                    |
| Source Code            | Implements the documented behavior            |

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
* README Standard
* SPEC Standard
* ARCH Standard
* ADR Standard
* Class Documentation Standard
* Function Documentation Standard
