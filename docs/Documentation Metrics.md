# Documentation Metrics for Project-Level Documents

## Purpose

To optimize documentation for AI agents, each project-level document is evaluated using two quantitative metrics:

* **Documentation Cost (α)**
* **Documentation Utility (β)**

These metrics are defined independently for each project-level document type.

---

# 1. Documentation Cost (α)

## Definition

Documentation cost is the ratio between the token count of a document and the token count of the project source code it describes.

```
α_D = T(D) / T(Project)
```

Where:

* **D** = project-level document
* **T(D)** = token count of the document
* **T(Project)** = token count of the project source code

---

## Project-Level Documents

### README

```
α_README = T(README) / T(Project)
```

---

### Documentation Index

```
α_INDEX = T(Index) / T(Project)
```

---

### Architecture Document

```
α_ARCH = T(Architecture) / T(Project)
```

---

### Architecture Decision Record (ADR)

```
α_ADR = T(ADR) / T(Project)
```

If an ADR documents only a subsystem rather than the entire project, the denominator may instead be the token count of that subsystem.

---

# 2. Documentation Utility (β)

## Definition

Documentation utility measures the probability that an AI agent can complete a task using the document without reading the implementation.

```
β_D = P(No Code Access | D)
```

An empirical estimate is:

```
β_D = N(Solved by D) / N(Total Queries)
```

Where:

* **N(Solved by D)** = number of tasks solved using only document **D**
* **N(Total Queries)** = total number of tasks related to the project

---

# Interpretation

A project-level document is considered efficient when:

* **α is small**, indicating a low documentation cost.
* **β is large**, indicating a high information value.

The optimization objective is:

```
min(α)
and
max(β)
```

The pair **(α, β)** provides a quantitative basis for determining the optimal size and information density of AI-oriented project documentation.
