# Validation rules for requirements

This file defines validation rules for the machine-readable requirements in:

- `requirements/requirements.ai-act-sandbox.dsl.json`

The goal is to ensure:
- syntactic consistency,
- low ambiguity,
- atomicity (single intent per requirement),
- and a consistent testability structure via acceptance criteria and verification data.

---

## 1. Syntax validation

### 1.1 Requirement object structure (mandatory fields)

A requirement MUST include:
- `id` (string)
- `type` (string; e.g., `AFO`)
- `status` (string; e.g., `draft`)
- `structure.subject` (string)
- `structure.modal_verb` (string)
- `structure.action` (string)
- `acceptance_criteria` (array; MAY be empty during early drafts, but SHOULD exist)

[Detailed information within DSL Core standard specificarion](https://github.com/rock-the-prototype/dsl-core)

### 1.2 Naming conventions

**Requirement IDs**
- MUST match: `^AIACT-SBX-REQ-\d{3}$`
- MUST be unique within the file.

**Acceptance criteria IDs**
- MUST match: `^AIACT-SBX-REQ-\d{3}-AC-\d{2}$`
- MUST be unique within the requirement.

### 1.3 Modal verbs

- `structure.modal_verb` MUST be one of: `MUST`, `SHOULD`, `MAY`.
- For baseline requirements in this repository, `MUST` is preferred unless explicitly scoped otherwise.

### 1.4 Acceptance criteria structure

Each acceptance criterion MUST include:
- `id` (string)
- `statement` (string)
- `verification_method` (string)
- `verification_artefacts` (array of strings; MAY be empty only if the method is self-evident, but SHOULD exist)

### 1.5 Verification method vocabulary

`verification_method` MUST be one of:
- `Inspection` (document/config review)
- `Review` (structured peer review)
- `Test` (execution-based verification)
- `Audit` (trace/log evidence against criteria)
- `Analysis` (reasoned assessment, e.g. threat modeling)

---

## 2. Ambiguity validation

A requirement SHOULD be rewritten if it contains ambiguous language that prevents consistent interpretation.

### 2.1 Ambiguity indicators (avoid)

Avoid vague adjectives or undefined qualifiers, such as:
- “appropriate”, “sufficient”, “robust”, “effective”, “meaningful”, “adequate”
- “where possible”, “as needed”, “relevant” (unless explicitly defined)

### 2.2 Required clarity properties

Each requirement SHOULD make clear:
- *what* must exist or be provided (object/result),
- *scope* (within sandbox context),
- and *observable anchors* (what could be inspected or audited).

If “relevant to the sandbox context” is used, the requirement SHOULD include acceptance criteria that operationalise relevance via a register, inventory, or documented applicability decision.

### 2.3 Acceptance criteria clarity test

For each acceptance criterion statement, reviewers SHOULD be able to answer:
- “Would two independent reviewers reach the same conclusion using the same artefacts?”

If not, add clarifying constraints in the statement or specify artefacts/method.

---

## 3. Atomicity validation

Atomicity means: **one requirement expresses one core intent**.

### 3.1 Non-atomic patterns (avoid)

A requirement is likely non-atomic if it includes:
- multiple actions joined by “and/or” that can be satisfied independently,
- multiple distinct objects (e.g. “data and identity and monitoring”),
- multiple lifecycle stages (e.g. “define, implement, operate”) in one sentence.

### 3.2 Atomicity rules

Each `structure.action` SHOULD:
- contain exactly one primary verb phrase (e.g. “define …”, “support …”, “maintain …”),
- target one primary object (e.g. “interfaces”, “data flows”, “baseline”).

If multiple aspects are needed, split into multiple REQs.

### 3.3 Acceptance criteria atomicity

Each acceptance criterion SHOULD:
- validate one condition,
- reference one main artefact type,
- avoid bundling multiple checks into one statement.

---

## 4. Consistency checks across the file

### 4.1 Subject consistency

All requirements in this file MUST use the same subject string:
- `EU AI Act regulatory sandbox framework`

If a requirement needs a different subject, it belongs in a different requirements set.

### 4.2 Cross-reference consistency

If a requirement introduces a registry/log/baseline concept, acceptance criteria SHOULD reference:
- existence of the artefact,
- completeness expectations (at minimum: scope statement),
- and traceability linkages (IDs, version identifiers, references).

### 4.3 Traceability readiness

Requirements SHOULD be linkable to sources via:
- `requirements.mapping.md` (REQ-ID → repo sources).

---

## 5. Validation outcomes (recommended statuses)

For automated or manual validation, each requirement MAY be assigned:
- `validation.syntax`: `pass|fail`
- `validation.ambiguity`: `pass|needs-review`
- `validation.atomicity`: `pass|needs-split`

(These fields are optional and can be maintained in a separate validation report artefact.)
