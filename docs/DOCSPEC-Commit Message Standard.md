# DOCSPEC: Commit Message Standard

## Overview

This document defines the standard structure, purpose, and writing conventions for Git commit messages within the project.

A commit message records the intent of a change at a specific point in the project's history. It provides a concise explanation of **what changed**, **why the change was made**, and, when necessary, the scope and impact of the modification.

This standard is based on the widely adopted **Conventional Commits** specification.

---

# Purpose

The purpose of a commit message is to:

* Document the intent of a change.
* Improve project history readability.
* Support code review.
* Simplify release note generation.
* Enable automated versioning and CI/CD workflows.
* Provide historical context for developers and AI agents.

---

# Scope

This standard applies to every Git commit in the repository.

It covers:

* Feature development
* Bug fixes
* Documentation
* Refactoring
* Testing
* Build configuration
* Continuous Integration
* Dependency updates
* Performance improvements

---

# Required Sections

## 1. Type

Defines the category of change.

Recommended values:

| Type     | Description                                 |
| -------- | ------------------------------------------- |
| feat     | New feature                                 |
| fix      | Bug fix                                     |
| docs     | Documentation changes                       |
| refactor | Code restructuring without behavior changes |
| perf     | Performance improvement                     |
| test     | Tests                                       |
| build    | Build system                                |
| ci       | Continuous Integration                      |
| style    | Formatting only                             |
| chore    | Maintenance                                 |
| revert   | Revert previous commit                      |

---

## 2. Scope

Identifies the affected subsystem.

Examples:

```text id="vh7oq0"
storage
kernel
config
cli
parser
graph
plugin
```

The scope is optional but strongly recommended.

---

## 3. Summary

A concise description written in the imperative mood.

Examples:

```text id="gpcbbq"
Add plugin discovery

Fix configuration loading

Refactor graph traversal
```

Guidelines:

* Present tense
* Imperative mood
* No trailing period
* Keep under 72 characters when practical

---

## 4. Body (Optional)

Explain the motivation and implementation approach.

Include:

* Why the change was needed.
* High-level implementation notes.
* Important design considerations.

Avoid repeating information already obvious from the code.

---

## 5. Footer (Optional)

Use footers for metadata.

Examples:

```text id="52lygp"
Closes #41

Refs #18

BREAKING CHANGE:

Supersedes ADR-0007
```

---

# Optional Sections

## Breaking Changes

Describe incompatible changes.

---

## Migration Notes

Required migration steps.

---

## Related Documentation

Reference:

* SPEC
* ARCH
* ADR

---

## Co-authored-by

When appropriate.

---

# Writing Guidelines

Commit messages should:

* Describe one logical change.
* Be concise and precise.
* Explain intent rather than implementation.
* Avoid vague wording.
* Use imperative verbs.
* Keep the subject independent of issue trackers.
* Reference documentation when useful.
* Separate unrelated changes into different commits.

Good commit messages explain **why**, not just **what**.

---

# Template

```text id="uwzyvr"
<type>(<scope>): <short summary>

<optional body>

<optional footer>
```

Example:

```text id="khq7zj"
feat(storage): add transactional persistence

Introduce transactional write support for project storage.
This prevents partially written project states during failures.

Refs SPEC-Storage
Refs ARCH-Storage
Implements ADR-0005
```

---

# Best Practices

* Keep commits atomic.
* One logical change per commit.
* Write the message before pushing.
* Reference related documentation when appropriate.
* Avoid mixing formatting and functional changes.
* Use `BREAKING CHANGE` for incompatible API modifications.
* Follow Conventional Commits consistently.

---

# Relationship to Other Documents

| Document       | Responsibility                                 |
| -------------- | ---------------------------------------------- |
| README         | Introduces the project                         |
| SPEC           | Defines what should be built                   |
| ARCH           | Defines how the system is designed             |
| ADR            | Explains why architectural decisions were made |
| Source Code    | Implements the change                          |
| Commit Message | Records the intent and history of the change   |

---

# Question Coverage

| Question     | Coverage  |
| ------------ | --------- |
| What         | Partial   |
| How          | Partial   |
| Why          | Partial   |
| What Changed | ✓ Primary |

---

# Lifecycle

```text
Requirement (SPEC)
        │
        ▼
Architecture (ARCH)
        │
        ▼
Decision (ADR)
        │
        ▼
Implementation
        │
        ▼
Commit
        │
        ▼
Review
        │
        ▼
Merge
```

---

# References

* Conventional Commits 1.0.0
* Semantic Versioning (SemVer)
* Project Documentation Standard
* Documentation Architecture (ARCH)
* SPEC Standard
* ARCH Standard
* ADR Standard
* Git Documentation
