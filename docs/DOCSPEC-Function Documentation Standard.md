# DOCSPEC: Function Documentation Standard

## Overview

This document defines the standard structure, purpose, and writing conventions for function documentation within the project.

Function documentation specifies the **contract** of a function. It describes what the function guarantees, what it expects from callers, and the observable behavior of its interface without exposing implementation details.

A function document should enable a developer or AI agent to correctly use the function without reading its implementation.

---

# Purpose

The purpose of function documentation is to:

* Define the function contract.
* Describe expected behavior.
* Document inputs and outputs.
* Specify preconditions and postconditions.
* Describe error conditions.
* Document complexity and side effects when relevant.

---

# Scope

This standard applies to:

* Public functions
* Public methods
* Library APIs
* Interface methods
* Virtual functions
* Template functions
* Callback interfaces

Internal helper functions should be documented only when their behavior is non-trivial.

---

# Required Sections

## 1. Function

The function name.

Example

```text
saveProject()
```

---

## 2. Summary

A concise description of the function.

The summary should answer:

* What does the function do?
* Why would a caller use it?

Keep it to one or two sentences.

---

## 3. Purpose

Describe the function's responsibility.

Focus on the observable operation rather than the implementation.

---

## 4. Parameters

Document every parameter.

For each parameter include:

* Name
* Type
* Description
* Constraints

Example

```text
path
    Output file location.

overwrite
    If true, replaces an existing file.
```

---

## 5. Return Value

Describe what is returned.

Include:

* Meaning
* Ownership (if applicable)
* Lifetime (if applicable)

---

## 6. Preconditions

Document conditions that must be true before calling the function.

Examples:

* Object is initialized.
* Path is valid.
* Configuration has been loaded.

---

## 7. Postconditions

Document guarantees after successful execution.

Examples:

* File exists.
* Cache is updated.
* Internal state is synchronized.

---

## 8. Side Effects

Document externally observable effects.

Examples:

* Writes files.
* Modifies global state.
* Sends events.
* Allocates resources.

If there are no side effects, state that explicitly.

---

## 9. Exceptions / Error Conditions

Describe failure behavior.

Include:

* Exceptions thrown
* Error codes
* Failure conditions

---

## 10. Complexity

Document algorithmic complexity when relevant.

Examples:

* Time: O(n)
* Space: O(1)

Only include if useful to callers.

---

## 11. Thread Safety

Describe concurrency guarantees.

Examples:

* Thread-safe
* Not thread-safe
* Caller synchronization required

---

## 12. Related Documents

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

Additional usage information.

---

## Examples

Usage examples.

---

## Performance Notes

Performance considerations.

---

## Limitations

Known limitations.

---

## Warnings

Potential misuse or dangerous behavior.

---

## Deprecated

Replacement function or migration guidance.

---

# Writing Guidelines

Function documentation should:

* Describe the public contract.
* Avoid implementation details.
* Describe observable behavior.
* Keep parameter descriptions concise.
* Keep terminology consistent.
* Document every externally visible side effect.
* Update whenever the public contract changes.

Do **not** describe internal algorithms unless they affect the public contract.

---

# Template

```text
/**
 * Function
 * --------
 * <Function Name>
 *
 * Summary
 * -------
 * <Short description>
 *
 * Purpose
 * -------
 * <Responsibility>
 *
 * Parameters
 * ----------
 * param1
 *     <Description>
 *
 * param2
 *     <Description>
 *
 * Return Value
 * ------------
 * <Description>
 *
 * Preconditions
 * -------------
 * ...
 *
 * Postconditions
 * --------------
 * ...
 *
 * Side Effects
 * ------------
 * ...
 *
 * Exceptions / Error Conditions
 * -----------------------------
 * ...
 *
 * Complexity
 * ----------
 * Time:
 * Space:
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

* One clear responsibility per function.
* Document behavior, not implementation.
* Keep summaries brief.
* Clearly distinguish preconditions from postconditions.
* Explicitly document side effects.
* Avoid repeating obvious information from the function signature.
* Keep complexity information relevant to callers.
* Keep documentation synchronized with the public interface.

---

# Relationship to Other Documents

| Document               | Responsibility                     |
| ---------------------- | ---------------------------------- |
| README                 | Introduces the project             |
| SPEC                   | Defines required behavior          |
| ARCH                   | Defines architectural structure    |
| ADR                    | Explains architectural decisions   |
| File Header            | Defines file responsibility        |
| Class Documentation    | Defines class responsibility       |
| Function Documentation | Defines the function contract      |
| Source Code            | Implements the documented contract |

---

# Question Coverage

| Question     | Coverage                      |
| ------------ | ----------------------------- |
| What         | ✓ Primary                     |
| How          | ✓ (public contract and usage) |
| Why          | —                             |
| What Changed | —                             |

---

# References

* Project Documentation Standard
* Documentation Architecture (ARCH)
* File Header Standard
* Class Documentation Standard
* C++ Core Guidelines
* Doxygen Manual
* ISO C++ Documentation Practices
