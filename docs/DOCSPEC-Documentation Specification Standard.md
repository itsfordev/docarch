# DOCSPEC: Documentation Specification Standard

## Overview

This document defines the standard structure, purpose, and writing conventions for **Documentation Specification (DOCSPEC)** documents.

A DOCSPEC describes the **standard** for a particular type of documentation. It defines what a document is expected to contain, how it should be organized, and the conventions authors should follow.

Unlike project documentation (README, SPEC, ARCH, ADR), a DOCSPEC does not describe the software system itself. Instead, it specifies **how a documentation artifact should be written**.

---

# Purpose

The purpose of a DOCSPEC is to:

* Standardize documentation across the project.
* Ensure consistency for developers and AI agents.
* Reduce ambiguity in documentation structure.
* Define mandatory and optional sections.
* Improve documentation quality and maintainability.
* Serve as the authoritative specification for a document type.

---

# Scope

This standard applies to all documentation standards within the project, including:

* README Standard
* SPEC Standard
* ARCH Standard
* ADR Standard
* File Header Standard
* Class Documentation Standard
* Function Documentation Standard
* Commit Message Standard
* Future documentation standards

---

# Required Sections

## 1. Title

The document title.

Example

```text
# DOCSPEC: ARCH Standard
```

---

## 2. Overview

Describe:

* What document type this standard defines.
* Why the document exists.
* Who the intended audience is.

---

## 3. Purpose

Describe the objectives of the document type.

Examples:

* Standardize documentation.
* Improve consistency.
* Define required content.

---

## 4. Scope

Specify where the standard applies.

Include:

* Applicable document types
* Exclusions
* Examples

---

## 5. Required Sections

Define every mandatory section of the target document.

For each section include:

* Name
* Purpose
* Expected contents

---

## 6. Optional Sections

Describe additional sections that may be included when appropriate.

Explain when each optional section should be used.

---

## 7. Writing Guidelines

Define writing conventions.

Examples:

* Use Markdown.
* Use consistent terminology.
* Avoid duplicated information.
* Prefer references over repetition.
* Keep sections concise.
* Use present tense.
* Describe responsibilities rather than implementation.

---

## 8. Template

Provide a complete reusable template.

The template should represent the canonical structure of the document type.

---

## 9. Best Practices

Provide recommendations beyond the minimum standard.

Examples:

* Keep documents focused.
* Maintain links between related documents.
* Update documentation together with code.
* Prefer one responsibility per document.

---

## 10. Relationship to Other Documents

Describe how this document type interacts with other documentation.

Include:

* Dependencies
* References
* Position within the documentation architecture

---

## 11. Question Coverage

Indicate which documentation question(s) the target document primarily answers.

| Question     | Coverage                 |
| ------------ | ------------------------ |
| What         | Primary / Partial / None |
| How          | Primary / Partial / None |
| Why          | Primary / Partial / None |
| What Changed | Primary / Partial / None |

---

## 12. References

List related standards and external references.

---

# Optional Sections

Include when appropriate.

## Audience

Target readers.

---

## Examples

Representative examples.

---

## Naming Convention

File naming rules.

---

## Versioning

Version management for the standard.

---

## Validation Checklist

Checklist for reviewing compliance.

---

## Change History

Revision history of the standard itself.

---

# Writing Guidelines

A DOCSPEC should:

* Specify **how documentation should be written**, not how software should be implemented.
* Be technology independent whenever possible.
* Define structure before content.
* Separate mandatory from optional sections.
* Use normative language ("should", "must", "may") consistently.
* Avoid project-specific implementation details unless intentionally defining a project standard.
* Be stable over time and evolve only when the documentation policy changes.

---

# Template

```markdown
# DOCSPEC: <Document Type> Standard

## Overview

## Purpose

## Scope

## Required Sections

## Optional Sections

## Writing Guidelines

## Template

## Best Practices

## Relationship to Other Documents

## Question Coverage

## References
```

---

# Best Practices

* Create one DOCSPEC per document type.
* Maintain a consistent structure across all DOCSPECs.
* Treat DOCSPECs as the single source of truth for documentation standards.
* Version DOCSPECs only when the documentation policy changes.
* Reference DOCSPECs from the project's Developer Guide or Documentation Index.
* Keep examples minimal but representative.

---

# Relationship to Other Documents

```text
DOCSPEC
   │
   ├── README
   ├── SPEC
   ├── ARCH
   ├── ADR
   ├── File Header
   ├── Class Documentation
   ├── Function Documentation
   └── Commit Message
```

DOCSPEC documents define **how documentation is written**. They do not describe the software system directly; instead, they govern the structure and quality of all other documentation artifacts.

---

# Question Coverage

| Question     | Coverage                                       |
| ------------ | ---------------------------------------------- |
| What         | ✓ Primary (what a document should contain)     |
| How          | ✓ Primary (how the document should be written) |
| Why          | Partial (why the document type exists)         |
| What Changed | —                                              |

---

# References

* Project Documentation Architecture
* README Standard
* SPEC Standard
* ARCH Standard
* ADR Standard
* Markdown Guide
* Conventional Commits Specification
