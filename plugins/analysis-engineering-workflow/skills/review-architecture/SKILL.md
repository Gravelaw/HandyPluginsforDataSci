---
name: review-architecture
description: Review planned or implemented architecture for software engineering, ML, analytics, data science, AI systems, hardware-integrated systems, and enterprise/system designs using ISO/IEC/IEEE 42010, SEI ATAM, ISO/IEC 25010, NIST SSDF, OWASP ASVS/SAMM, NIST AI RMF, and NASA/JPL Power of Ten. Use before implementation, before large refactors, before publishing, or when assessing maintainability, testability, reproducibility, security, safety, and compliance-style readiness.
---

# Review Architecture

Use this skill as an architecture review gate.

Read `../../references/governed-engineering-framework.md` for substantial reviews. Default to adversarial mode when the design touches security, AI/ML, data correctness, safety, hardware, public APIs, or production operations.

## Review Focus

Prioritize findings over praise:

1. ISO 42010 gaps: missing stakeholders, concerns, architecture views, rationale, interfaces, or correspondences.
2. ATAM risks: quality attribute scenarios that fail, sensitivity points, tradeoff points, and unstated assumptions.
3. ISO 25010 quality gaps: functional suitability, performance, compatibility, interaction/usability, reliability, security, maintainability, portability, flexibility, or safety.
4. Correctness and data leakage risks.
5. Broken or missing contracts between data, model, API, UI, hardware, and operations layers.
6. Hidden state, global configuration, and irreproducible execution.
7. Excess coupling, oversized modules, and abstractions without payoff.
8. Package compatibility, supply-chain, deployment, and rollback risks.
9. Security and privacy: credentials, unsafe deserialization, untrusted files, PII, shell execution, network calls, trust boundaries, and authorization.
10. AI/ML risk: dataset lineage, evaluation validity, drift, monitoring, explainability, fairness, model rollback, prompt/data injection, and human oversight.
11. Test strategy: unit, integration, property, notebook, smoke, adversarial, load, and operational checks.
12. Performance and scale: memory growth, unbounded loops, batching, streaming, and parallelism.

## Output Shape

Lead with issues ordered by severity. Include a framework anchor for each issue. End with open questions, residual risks, and a gate decision: pass, pass with conditions, or block.
