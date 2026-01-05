# Alignment with the draft implementing act on AI regulatory sandboxes

This document summarises how selected structural and operational aspects relevant to AI regulatory sandboxes are reflected in the draft implementing act, based on the common requirements outlined in [feedback/01-common-requirements.md`](https://github.com/rock-the-prototype/eu-ai-act-regulatory-sandboxes/blob/main/feedback/01-common-requirements.md).

The observations below are descriptive and do not constitute legal or normative assessments.

---

## Aspects clearly addressed

### Procedural establishment and supervision

The draft implementing act sets out the intention and core elements for establishing a procedural framework for the establishment and operation of AI regulatory sandboxes.
This includes provisions on:
- designation and responsibilities of competent authorities,
- application and selection procedures,
- time-limited participation,
- and regulatory supervision during sandbox operation.

These elements support transparency, predictability, and legal certainty for participating organisations.

---

### Controlled environments and regulatory learning

AI regulatory sandboxes are explicitly framed as controlled environments operating under regulatory supervision. The possibility to conduct activities under real-world conditions, where appropriate, is foreseen.

This supports the objective of enabling regulatory learning while maintaining oversight and safeguards.

---

## Aspects partially addressed

### Interoperability

The draft acknowledges the importance of coordination and information exchange across sandbox initiatives. However, interoperability is primarily addressed at a governance level.

Operational aspects such as:
- technical interoperability assumptions,
- interface consistency,
- or transferability of sandbox outcomes across regulatory layers

remain largely dependent on implementation choices by competent authorities.

---

### Production relevance and transition to deployment

The draft enables experimentation prior to market placement, including under real-world conditions. At the same time, it does not explicitly address the relationship between sandbox configurations and later production environments.

As a result, the degree to which sandbox findings remain applicable to downstream deployment contexts may vary between implementations. This variability increases fragmentation across sandbox environments, limits interoperability, and raises the effort required to ensure robust and secure operation, as comparable issues must be addressed repeatedly across multiple sandbox instances rather than within a shared reference environment.

---

### Data governance

The draft refers to compliance with applicable legal frameworks, including data protection, and foresees the involvement of relevant supervisory authorities.

However, data governance is addressed at a high level. Aspects such as data lifecycle management, traceability of data flows within sandbox environments, and handling of changing legal or factual conditions are not operationally specified.

---

### Transparency and participant-facing disclosure
The draft foresees documentation and reporting obligations as part of sandbox operation. However, transparency is primarily reflected through procedural documentation rather than through explicit operational artefacts intended for participant-facing disclosure.

Aspects such as:

- a consolidated transparency concept,
- defined disclosure content and format,
- and linkage of disclosures to sandbox baseline versions are not operationally specified and remain dependent on implementation choices.

---

## Explainability and limitations (where applicable)
While the draft supports sandbox activities under regulatory supervision, it does not operationalise explainability as a sandbox design baseline.

Aspects such as:

- a system- and risk-context appropriate explainability approach,
- explicit documentation of explainability limitations,
- and traceability of explainability artefacts to sandbox baselines remain largely dependent on implementation choices.

---

## Aspects not explicitly addressed

### Operational definition of AI regulatory sandboxes

While the purpose and intended function of AI regulatory sandboxes are described, the draft does not provide a consolidated operational or technical definition of what constitutes a sandbox in practice.

Minimum structural, technical, or organisational characteristics that would distinguish regulatory sandboxes from other forms of large-scale pilot environments or testbeds are not specified.

---

### Versioning and auditability of sandbox configurations

Although documentation and reporting obligations are foreseen, the draft does not explicitly address the versioning and auditability of sandbox configurations, assumptions, and rule sets over time.

The absence of explicit reference points in this area may limit comparability and reproducibility of regulatory insights across sandbox initiatives.

---

### Bias and fairness governance (where applicable)
The draft does not explicitly establish a shared baseline for assessing, documenting, and mitigating bias/fairness risks within sandbox activities.

Common reference points for:

- bias/fairness assessment scope and methods,
- mitigation planning and residual risk documentation,
- and participant-facing interpretation guidance
are not specified as part of the sandbox framework.

### AI-specific security testing (where applicable)
The draft references safeguards and risk considerations but does not define AI-specific security testing expectations (e.g., prompt injection or tool misuse scenarios for instruction-following/LLM-based components).

As a result, AI-specific testing coverage and evidence practices may vary between sandbox implementations.

---

## Summary observation

Overall, the draft implementing act outlines the intention to establish a procedural framework aligned with the objectives of AI regulatory sandboxes as defined in Regulation (EU) 2024/1689.

At the same time, several structural and operational aspects relevant to comparability, interoperability, and long-term regulatory learning remain dependent on subsequent implementation choices by competent authorities. Without shared operational reference points, this may lead to fragmented sandbox environments, reduced interoperability between implementations, and increased effort to ensure robustness and security across multiple sandbox instances. Such fragmentation risks limiting the effectiveness of AI regulatory sandboxes as instruments for transferable regulatory learning and transition towards compliant deployment.

### Limited transparency and explainability artefacts
If sandbox operation lacks an explicit transparency concept and participant-facing disclosures, accountability and informed participation may become difficult to ensure across implementations.

Similarly, where explainability approaches and their limitations are not documented in a comparable way, the ability to interpret and compare sandbox outcomes may vary significantly between sandbox instances.

### Non-comparable handling of bias and fairness
If bias/fairness assessment and mitigation guidance remain implicit, sandboxes may produce outcomes that are difficult to compare across jurisdictions, sectors, or cycles.

This can reduce the cumulative value of regulatory learning, as results may depend strongly on locally chosen assessment and documentation practices.

### AI-specific attack surface and false confidence (where applicable)
Where LLM-based components are used without structured AI-specific security testing, sandbox environments risk generating findings that underestimate relevant attack patterns.

This may increase the likelihood that downstream deployment contexts encounter issues that were not systematically addressed during sandbox activities.
