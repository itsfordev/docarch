# DOCSPEC: ADR Standard

## Overview

This document defines the standard structure, purpose, and writing conventions for Architecture Decision Records (ADR) within the project.

An ADR captures a **significant architectural decision**, the context in which it was made, the selected solution, the alternatives considered, and the resulting consequences.

Unlike an ARCH document, which describes the architecture itself, an ADR explains **why the architecture is the way it is**.

An ADR is immutable once accepted. If a decision changes, a new ADR supersedes the previous one.

---

# Purpose

The purpose of an ADR is to:

* Record significant architectural decisions.
* Preserve architectural rationale.
* Document alternatives and trade-offs.
* Improve long-term maintainability.
* Provide historical context for future developers and AI agents.

---

# Scope

This standard applies to decisions affecting:

* System architecture
* Module boundaries
* Public APIs
* Storage design
* Plugin systems
* Communication protocols
* Dependency selection
* Build systems
* Security architecture
* Performance architecture
* Infrastructure architecture

Examples:

* ADR-0001-Repository-Layout.md
* ADR-0002-Configuration-System.md
* ADR-0003-Plugin-Architecture.md

---

# Required Sections

## 1. Title

A concise description of the decision.

Example

```text
# ADR-0003: Plugin Architecture
```

---

## 2. Status

Current decision state.

Recommended values:

* Proposed
* Accepted
* Rejected
* Superseded
* Deprecated

---

## 3. Date

Decision date.

Use ISO 8601.

Example

```text
2026-07-12
```

---

## 4. Context

Describe the problem or situation that required a decision.

Include:

* Existing limitations
* Requirements
* Constraints
* Architectural forces

Avoid discussing the chosen solution here.

---

## 5. Decision

Describe the selected solution.

State the decision clearly and unambiguously.

---

## 6. Alternatives Considered

List realistic alternatives.

For each alternative include:

* Description
* Advantages
* Disadvantages
* Reason for rejection

---

## 7. Consequences

Describe the impact of the decision.

Include both:

### Positive

Benefits introduced.

### Negative

Costs, limitations, or risks.

---

## 8. Related Documents

Reference associated documentation.

Examples:

* SPEC
* ARCH
* Previous ADRs
* API
* Issues

---

# Optional Sections

Include when appropriate.

## Assumptions

Assumptions made during decision making.

---

## Risks

Potential future risks.

---

## Compatibility

Compatibility with existing systems.

---

## Migration Plan

Required migration steps.

---

## Open Questions

Questions remaining after acceptance.

---

## References

External references supporting the decision.

---

# Writing Guidelines

An ADR should:

* Capture one decision only.
* Be concise and objective.
* Explain *why* the decision was made.
* Describe trade-offs honestly.
* Avoid implementation details.
* Avoid business documentation.
* Avoid future speculation unless clearly identified.
* Never be rewritten after acceptance.

If circumstances change, create a new ADR that supersedes the previous one.

---

# Template

```markdown
# ADR-XXXX: <Decision Title>

## Status

Accepted

## Date

YYYY-MM-DD

## Context

## Decision

## Alternatives Considered

### Alternative A

#### Advantages

#### Disadvantages

### Alternative B

#### Advantages

#### Disadvantages

## Consequences

### Positive

### Negative

## Related Documents

### SPEC

### ARCH

### Previous ADRs

### API

### Issues

---

## Optional

### Assumptions

### Risks

### Compatibility

### Migration Plan

### Open Questions

### References
```

---

# Best Practices

* One ADR per architectural decision.
* Number ADRs sequentially.
* Keep ADRs immutable after acceptance.
* Create a new ADR instead of modifying an accepted one.
* Link ADRs to affected ARCH and SPEC documents.
* Record rejected alternatives.
* Explain architectural trade-offs explicitly.
* Keep ADRs short and focused.

---

# Relationship to Other Documents

| Document       | Responsibility                                     |
| -------------- | -------------------------------------------------- |
| README         | Introduces the project                             |
| SPEC           | Defines **what** should be built                   |
| ARCH           | Describes **how** the system is designed           |
| ADR            | Explains **why** architectural decisions were made |
| Source Code    | Implements the selected architecture               |
| Commit History | Records implementation of architectural decisions  |

---

# Question Coverage

| Question     | Coverage  |
| ------------ | --------- |
| What         | Partial   |
| How          | Partial   |
| Why          | ✓ Primary |
| What Changed | —         |

---

# Lifecycle

```text
Problem
   │
   ▼
Context
   │
   ▼
Decision
   │
   ▼
Implementation
   │
   ▼
Review

If the decision changes:
      │
      ▼
Create a New ADR
(Supersedes Previous ADR)
```

---

# References

* Michael Nygard, *Architecture Decision Records*
* Project Documentation Standard
* Documentation Architecture (ARCH)
* README Standard
* SPEC Standard
* ARCH Standard
* API Documentation Standard
* Conventional Commits
