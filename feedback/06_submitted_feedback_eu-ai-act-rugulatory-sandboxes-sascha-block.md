# Do you represent an organisation (e.g., think tank or civil society/consumer organisation) or act in your personal capacity (e.g., independent expert or from a downstream provider)?

x 	Answer: Organisation

# Sector(s) of activity

x 	Answer: 	
- Information technology
- Public administration
- Healthcare

# Describe the activities of your organisation or yourself

I am Sascha Block, an IT architect working in the German statutory health insurance domain (Mobil Krankenkasse, a public-law corporation). My work focuses on interoperable, secure and auditable digital infrastructures in highly regulated settings, including the telematic infrastructure and services such as ePrescription and electronic patient records, where health protection and data protection must be treated as complementary goals.

In parallel, through INZTITUT GmbH, I work on governance-oriented approaches for requirements engineering, compliance-by-design and production-relevant prototyping. This includes open, versioned artefacts and machine-readable requirements as a practical way to reduce ambiguity, improve accountability and support regulatory learning across organisations and implementation cycles.

#  QuestionPlease share below your feedback on the draft implementing act on AI regulatory sandboxes, referring to specific articles, where possible.

This feedback focuses on the draft implementing act as a learning-oriented framework for AI regulatory sandboxes under Regulation (EU) 2024/1689. The draft rightly emphasises avoiding fragmentation and ensuring consistent implementation across the Union (Recital (2)) and refers to uniform application, common interpretation and mutual recognition of results (Recital (4)).

1) Procedural clarity is strong, but operational reference points remain implicit
The draft establishes common rules for participation and supervision (Article 1; Article 2) and provides mechanisms for documentation and exit reporting (Article 6; Recital (21)). These are essential foundations for transparency and regulatory learning.
However, mutual recognition and “anti-fragmentation” objectives require not only procedure, but also shared operational artefacts that make sandbox outcomes comparable and transferable across authorities and contexts.

2) Interoperability as an operational requirement (not only a governance objective)
Given Recital (2) and (4), it would strengthen the framework to require a minimal, versioned set of interoperability assumptions: documented interfaces, identity/access handling across organisational boundaries, and explicit links to relevant standards/infrastructures. Without this, heterogeneous sandbox implementations risk reducing interoperability and increasing repeated operational/security overhead.

3) Production relevance / transition to deployment
The draft supports real-world testing “where appropriate” (Recital (1), (20)) and recognises the sandbox as pre-market instrument. This would benefit from an explicit requirement to document production relevance: which sandbox characteristics intentionally match downstream production contexts, and which deviations exist (with rationale and impact on findings). Otherwise, results may remain locally valid but hard to reuse across deployment contexts.

4) Data governance, including lifecycle and reversibility
Association of data protection supervision is acknowledged (Recital (10)) and confidentiality obligations are noted (Recital (11)).
Operationally, sandboxes need clearer expectations for: data sources and permitted uses, traceability of data flows, retention/deletion, handling of changing legal/factual conditions, and—where AI learning effects are involved—documented mechanisms to address requests to exclude previously used data from influencing system behaviour (“unlearning” / reversibility), at least at the level of process and traceability.

5) Security-by-design baseline and AI-specific security testing (where applicable)
To support comparability and reduce repeated remediation across multiple sandboxes, a shared security-by-design baseline (principles + minimum controls, versioned) would be helpful, complemented by context-appropriate AI security testing (e.g., prompt injection resilience for LLM-based systems) where relevant to the sandbox project type.

6) Transparency, explainability, and bias/fairness governance as repeatable learning artefacts
For sandboxes to function as trust-building learning instruments, participants and overseers benefit from a versioned transparency concept (scope, boundaries, data categories, constraints, disclosures linked to sandbox baseline versions), a documented explainability/limitations approach proportionate to risk/system type, and repeatable bias/fairness assessment + mitigation guidance as part of the sandbox learnings.

Reference (public annex)
A structured, versioned annex of requirements and traceability is maintained here for transparency and iterative refinement:
[EU AI Act – Regulatory Sandboxes](https://github.com/rock-the-prototype/eu-ai-act-regulatory-sandboxes/)

## Do you agree that we may publish your identity with your contribution in case all contributions are made publicly available?

If you represent one or more organisations: All contributions to this consultation may be made publicly available. You can choose whether you would like respondent details to be made public or to remain anonymous. Only organisation details may be published: The type of respondent that you responded to this consultation as, the name of the organisation on whose behalf you reply as well as its size, its presence in or outside the EU and your contribution may be published as received. Your name will not be published. Please do not include any personal data in the contribution itself if you want to remain anonymous.

	Answer
Yes.

## Do you agree that we may contact you in the event of follow-up questions or if we want to learn more about your responses?
	Answer
Yes

