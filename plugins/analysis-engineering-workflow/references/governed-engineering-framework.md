# Governed Engineering Analysis Framework

This plugin uses a tailored framework for software, data, ML, AI, and system design reviews. It is not a certification claim. It is a practical review model grounded in published standards and review methods.

## Framework Stack

1. Lifecycle governance: use ISO/IEC/IEEE 12207:2026 for software life cycle processes and ISO/IEC/IEEE 15288:2023 for system life cycle thinking.
2. Architecture description: use ISO/IEC/IEEE 42010 concepts: stakeholders, concerns, system of interest, architecture views, viewpoints, rationale, and correspondences.
3. Architecture evaluation: use SEI ATAM to expose risks, non-risks, sensitivity points, and tradeoff points against quality attribute scenarios.
4. Product quality: use ISO/IEC 25010 as the quality vocabulary for functional suitability, performance efficiency, compatibility, usability/interaction capability, reliability, security, maintainability, portability, flexibility, and safety.
5. Secure development: use NIST SP 800-218 SSDF for secure SDLC practices. Use OWASP ASVS for web/API verification detail and OWASP SAMM for security program maturity when relevant.
6. AI risk: use NIST AI RMF for AI/ML systems: govern, map, measure, and manage trustworthiness risks.
7. Engineering discipline: use NASA/JPL Power of Ten as a critical-code checklist for bounded control flow, limited scope, checked errors, assertions, and automated analysis.
8. Review conduct: use IEEE software review concepts: management review, technical review, inspection, walkthrough, and audit. Choose the lightest review type that matches the risk.

## Source Anchors

- ISO/IEC/IEEE 12207:2026: https://www.iso.org/standard/90219.html
- ISO/IEC/IEEE 15288:2023: https://www.iso.org/standard/81702.html
- ISO/IEC/IEEE 42010:2022: https://www.iso.org/standard/74393.html
- ISO/IEC 25010:2023: https://www.iso.org/standard/78176.html
- SEI Architecture Tradeoff Analysis Method: https://www.sei.cmu.edu/library/architecture-tradeoff-analysis-method-collection/
- NIST SP 800-218 SSDF: https://csrc.nist.gov/pubs/sp/800/218/final
- NIST AI RMF: https://www.nist.gov/itl/ai-risk-management-framework
- OWASP ASVS: https://owasp.org/www-project-application-security-verification-standard/
- OWASP SAMM: https://owasp.org/www-project-samm/
- NASA/JPL Power of Ten: https://spinroot.com/gerard/pdf/P10.pdf

## Review Modes

- Advisory: improve clarity, maintainability, and delivery odds.
- Gate: decide if work is ready to implement, merge, deploy, or publish.
- Adversarial: actively try to invalidate the design using failure scenarios, misuse cases, threat modeling, scale pressure, operational faults, bad data, ambiguous ownership, and compliance gaps.

Default to adversarial mode for security-sensitive, AI/ML, data-critical, regulated, hardware-integrated, safety-relevant, or public-release work.

## Required Review Evidence

- System of interest and scope.
- Stakeholders and concerns.
- Quality attribute scenarios with stimulus, environment, response, and measure.
- Decisions and rationale.
- Interfaces and data contracts.
- Threat model and trust boundaries when security matters.
- Lifecycle phase and exit criteria.
- Verification plan and residual risks.

## Role Lens

- Enterprise architect: strategy alignment, portfolio fit, governance, standards, cost, vendor and platform risk.
- System architect: interfaces, hardware/software boundaries, constraints, reliability, safety, operations, and integration.
- Software architect: module boundaries, APIs, data flow, quality attributes, evolution, and technical debt.
- Security architect: threat model, secure-by-design practices, abuse cases, secrets, identity, authorization, supply chain, and logging.
- Data/ML/AI lead: dataset lineage, leakage, evaluation, reproducibility, model risk, monitoring, drift, fairness, and rollback.
- Tech lead: implementation feasibility, developer workflow, tests, maintainability, and incremental delivery.
- QA/SRE/release lead: verification, observability, deployability, rollback, incident handling, and service-level expectations.
- Product/business owner: user value, constraints, acceptance criteria, privacy expectations, and business risk.

## Finding Format

Findings should be precise:

- Severity: P0 critical, P1 high, P2 medium, P3 low.
- Framework anchor: for example `ISO 42010 concern gap`, `ATAM tradeoff risk`, `NIST SSDF practice gap`, `ISO 25010 maintainability`, `NIST AI RMF measurement gap`.
- Evidence: file, design section, command output, data sample, diagram, or missing artifact.
- Impact: what can fail and for whom.
- Recommendation: smallest useful fix or next review gate.
