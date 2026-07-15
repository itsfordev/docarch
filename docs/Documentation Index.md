# Documentation Index

## Overview

The **DOCARCH** directory contains the documentation architecture and documentation standards used throughout the project.

These documents define **how documentation should be written**, ensuring consistency, maintainability, and efficient collaboration between developers and AI agents.

This directory serves as the single entry point for all documentation standards.

---

## Purpose

The objectives of this documentation library are to:

* Standardize project documentation.
* Establish consistent documentation practices.
* Define the responsibility of each document type.
* Reduce duplicated documentation.
* Improve navigation between related documents.
* Enable AI agents to efficiently locate and understand project knowledge.

---

## Documentation Hierarchy

```text
Documentation Standards (DOCSPEC)
                │
                ▼
README
SPEC
ARCH
ADR
                │
                ▼
Source Code Documentation
├── File Header
├── Class Documentation
└── Function Documentation
                │
                ▼
Git History
└── Commit Messages
```

---

# Documentation Architecture

The following architectural document defines the overall documentation model.

| Document                                                                          | Description                                                                                   |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| [ARCH-001 Documentation Architecture](ARCH%28001%29Documentation-Architecture.md) | Defines the documentation architecture and relationships between all documentation artifacts. |

---

# Documentation Standards

## Core Documentation

| Document                                              | Purpose                                          |
| ----------------------------------------------------- | ------------------------------------------------ |
| [DOCSPEC-README Standard](DOCSPEC-README-Standard.md) | Standard for repository and module README files. |
| [DOCSPEC-SPEC Standard](DOCSPEC-SPEC-Standard.md)     | Standard for functional specifications.          |
| [DOCSPEC-ARCH Standard](DOCSPEC-ARCH-Standard.md)     | Standard for architectural documentation.        |
| [DOCSPEC-ADR Standard](DOCSPEC-ADR-Standard.md)       | Standard for Architecture Decision Records.      |

---

## Source Code Documentation

| Document                                                                              | Purpose                                |
| ------------------------------------------------------------------------------------- | -------------------------------------- |
| [DOCSPEC-File Header Standard](DOCSPEC-File Header-Standard.md)                       | Standard for documenting source files. |
| [DOCSPEC-Class Documentation Standard](DOCSPEC-Class Documentation-Standard.md)       | Standard for documenting classes.      |
| [DOCSPEC-Function Documentation Standard](DOCSPEC-Function Documentation Standard.md) | Standard for documenting functions.    |

---

## Version Control Documentation

| Document                                                              | Purpose                           |
| --------------------------------------------------------------------- | --------------------------------- |
| [DOCSPEC-Commit Message Standard](DOCSPEC-Commit Message Standard.md) | Standard for Git commit messages. |

---

## Documentation Standards

| Document                                                                                        | Purpose                                                               |
| ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| [DOCSPEC-Documentation Specification Standard](DOCSPEC-Documentation Specification Standard.md) | Defines the standard for creating documentation standards (DOCSPECs). |

---

# Recommended Reading Order

For new developers and AI agents:

1. Documentation Index *(this document)*
2. ARCH-001 Documentation Architecture
3. DOCSPEC-Documentation Specification Standard
4. DOCSPEC-README Standard
5. DOCSPEC-SPEC Standard
6. DOCSPEC-ARCH Standard
7. DOCSPEC-ADR Standard
8. DOCSPEC-File Header Standard
9. DOCSPEC-Class Documentation Standard
10. DOCSPEC-Function Documentation Standard
11. DOCSPEC-Commit Message Standard

---

# Relationships

Each documentation artifact answers a different question.

| Document               | Primary Question                              |
| ---------------------- | --------------------------------------------- |
| README                 | **What is the project?**                      |
| SPEC                   | **What should be built?**                     |
| ARCH                   | **How is it designed?**                       |
| ADR                    | **Why was this design chosen?**               |
| File Header            | **What is this file responsible for?**        |
| Class Documentation    | **What is this class responsible for?**       |
| Function Documentation | **What contract does this function provide?** |
| Commit Message         | **What changed?**                             |

---

# Directory Structure

```text
DOCARCH/
│
├── ARCH(001)Documentation-Architecture.md
│
├── DOCSPEC-Documentation Specification Standard.md
│
├── DOCSPEC-README-Standard.md
├── DOCSPEC-SPEC-Standard.md
├── DOCSPEC-ARCH-Standard.md
├── DOCSPEC-ADR-Standard.md
│
├── DOCSPEC-File Header-Standard.md
├── DOCSPEC-Class Documentation-Standard.md
├── DOCSPEC-Function Documentation Standard.md
│
├── DOCSPEC-Commit Message Standard.md
│
└── README.md   ← Documentation Index
```

---

# References

* [ARCH-001 Documentation Architecture](ARCH%28001%29Documentation-Architecture.md)
* DOCSPEC-Documentation Specification Standard
* Project Documentation Standards
