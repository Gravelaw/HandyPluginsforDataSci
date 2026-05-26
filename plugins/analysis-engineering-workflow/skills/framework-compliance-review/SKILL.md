---
name: framework-compliance-review
description: Perform standards-guided and adversarial engineering reviews for software, data, ML, AI, hardware-integrated, and system designs. Use when Codex should assess architecture, implementation, test plans, readiness, or compliance-style evidence against ISO/IEC/IEEE 12207, ISO/IEC/IEEE 42010, ISO/IEC 25010, SEI ATAM, NIST SSDF, OWASP ASVS/SAMM, NIST AI RMF, NASA/JPL Power of Ten, or role-based architecture review gates.
---

# Framework Compliance Review

Use this skill for precise, standards-guided reviews. This is not a certification audit; it is an engineering assurance workflow grounded in named frameworks.

Read `../../references/governed-engineering-framework.md` when the review is substantial, security-sensitive, AI/ML-related, system-level, or intended for publication.

## Review Workflow

1. Classify the review target: concept, requirements, architecture, design, code, data/ML pipeline, AI system, deployment, operations, or release.
2. Select review mode: advisory, gate, or adversarial.
3. Identify lifecycle phase and exit criteria using ISO/IEC/IEEE 12207 or systems-style 15288 thinking.
4. Build the architecture description lens: stakeholders, concerns, system of interest, views, interfaces, rationale, and correspondences.
5. Apply ATAM: elicit quality attribute scenarios, identify sensitivity points, tradeoff points, risks, and non-risks.
6. Score quality against ISO/IEC 25010 characteristics relevant to the task.
7. Apply security gates: NIST SSDF by default, OWASP ASVS for web/API controls, OWASP SAMM for program maturity.
8. Apply NIST AI RMF for AI/ML systems: govern, map, measure, and manage risks.
9. Apply NASA/JPL Power of Ten when critical code, reliability, safety, or bounded execution matters.
10. Produce findings first, ordered by severity, with framework anchors and concrete remediation.

## Adversarial Prompts

Ask these when review mode is adversarial:

- What unstated assumption can invalidate the design?
- What input, scale, timing, dependency, or operator action breaks it?
- What trust boundary, credential, model artifact, dataset, or supply-chain element can be abused?
- What quality attribute improves only by degrading another one?
- What evidence is missing for the claimed readiness level?
- What would a system architect, enterprise architect, security architect, tech lead, SRE, and data/ML lead each reject?

## Output Shape

Lead with findings:

```text
P1 - Framework anchor - Short finding
Evidence:
Impact:
Recommendation:
```

Then include:

- Review mode and framework stack used.
- Open questions.
- Gate decision: pass, pass with conditions, or block.
- Residual risks and missing evidence.

