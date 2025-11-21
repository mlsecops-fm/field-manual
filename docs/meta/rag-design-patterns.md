# RAG Design Patterns: Comparative Retrieval (Source vs Reference)

## Purpose

This document defines the *comparative retrieval pattern* used within the MLSecOps Field Manual. It provides a generic, safe, public-facing explanation of how multi-corpus RAG can be used to perform structured comparison between user-authored materials (SOURCE) and trusted references (REFERENCE).

This pattern is conceptual and does not expose private lab details.

---

## 1. Problem

MLSecOps practitioners often need to evaluate:

- architectures
- pipelines
- agents
- inference servers
- MLOps deployments
- documentation
- security controls

against:

- industry best practices
- threat models
- MITRE ATLAS
- OWASP ML/LLM standards
- NIST AI RMF
- reference architectures

This requires a repeatable comparison method.

---

## 2. The Comparative Retrieval Pattern

### 2.1 Intent

Enable the LLM to:

- contrast a user system with canonical references
- identify alignment and divergence
- reveal coverage gaps
- produce actionable hardening steps

### 2.2 Structure

```
+------------------+       +--------------------+
|  SOURCE CORPUS   |       |  REFERENCE CORPUS  |
|  (User docs,     |       |  (Books, standards,|
|   architecture,  |       |   whitepapers,     |
|   pipelines)     |       |   threat models)   |
+--------+---------+       +---------+----------+
         |                           |
         |  Retrieve top-k           |  Retrieve top-k
         v                           v
+------------------+       +--------------------+
|  SOURCE CHUNKS   |       |  REFERENCE CHUNKS  |
+--------+---------+       +---------+----------+
         |                           |
         +-------------+-------------+
                       |
                       v
              +--------+--------+
              |  LLM SYNTHESIS  |
              |  (Comparative   |
              |   Analysis)     |
              +--------+--------+
                       |
                       v
              +--------+--------+
              |  STRUCTURED     |
              |  OUTPUT         |
              |  - Alignment    |
              |  - Gaps         |
              |  - Risks        |
              |  - Recommendations
              +-----------------+
```

**SOURCE CORPUS** - User-authored materials (architecture, pipelines, plans).

**REFERENCE CORPUS** - Trusted external sources (books, standards, whitepapers).

**COMPARATIVE RETRIEVAL** - Retrieve top-k SOURCE chunks and top-k REFERENCE chunks, keeping them separate.

**COMPARATIVE SYNTHESIS** - Use a prompt that requires alignment, gaps, risks, and recommendations. This forces the model into an analytical role.

---

## 3. Behavior

### 3.1 Retrieval

Identifies the most relevant:

- source components
- reference patterns
- threat techniques
- controls

### 3.2 Synthesis

Structured reasoning:

```
## Alignment
...

## Gaps
...

## Risks
...

## Recommendations
...
```

### 3.3 Outcomes

- Transparent evaluations
- Reproducible analyses
- Clear threat mappings
- Actionable system hardening
- Separation of personal vs public materials

---

## 4. Applications in the Field Manual

### 4.1 Threat Mapping

Compare agent design against MITRE ATLAS techniques.

### 4.2 Pipeline Hardening

Compare ingestion pipeline against OWASP ML / OpenSSF controls.

### 4.3 Service Alignment

Compare inference server against model serving patterns.

### 4.4 Curriculum Planning

Compare learning plan against canonical MLOps/ML curricula.

---

## 5. Why This Pattern Matters

- Prevents hallucinated comparisons
- Avoids mixed-corpus confusion
- Supports educational modules
- Provides structure for MLSecOps analysis
- Enables safe synthetic demonstrations via demo_rag

---

## 6. Summary

The **Source vs Reference Comparative Retrieval Pattern** transforms RAG into a structured analysis engine capable of supporting:

- MLSecOps threat assessments
- Pipeline hardening
- Compliance alignment
- Architecture evaluations
- Educational modules

It is a foundational pattern for the Field Manual's teaching model.

---

**Last Updated:** 2025-11-21
