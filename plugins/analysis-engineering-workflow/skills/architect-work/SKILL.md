---
name: architect-work
description: Architect Python and Julia software, ML pipelines, analytics projects, AI systems, and system designs using ISO/IEC/IEEE 42010 architecture description, SEI ATAM quality tradeoff analysis, ISO/IEC 25010 quality attributes, NIST SSDF secure design, NIST AI RMF AI risk review, and NASA/JPL critical-code discipline. Use when choosing module boundaries, data contracts, package structure, model workflow design, storage layout, APIs, interfaces, deployment, or execution strategy.
---

# Architect Work

Use this skill after planning and before non-trivial implementation.

For substantial work, read `../../references/governed-engineering-framework.md`.

## Architecture Checks

1. Read the existing project structure and dependency files first.
2. Define the system of interest, stakeholders, concerns, context, and architecture views.
3. Choose the smallest design that satisfies the current task and the relevant quality scenarios.
4. Define boundaries: ingestion, validation, features, modeling, evaluation, serving, reporting, orchestration, operations, and external systems.
5. Define contracts: schemas, shapes, units, model inputs/outputs, configuration, file paths, APIs, trust boundaries, and failure behavior.
6. Use ATAM thinking: record risks, non-risks, sensitivity points, and tradeoff points.
7. Prefer standard project layouts: `src/`, `tests/`, `notebooks/`, `scripts/`, `data/`, `models/`, and `artifacts/`.
8. Avoid framework sprawl. Add dependencies only when they remove real complexity.
9. Account for reproducibility: seeds, environment files, deterministic splits, version capture, dataset lineage, and artifact provenance.
10. Account for observability: clear logs, metrics, warnings, saved evaluation artifacts, health checks, and rollback signals.
11. Invoke `framework-compliance-review` before implementation when the design is public-facing, security-sensitive, AI/ML-critical, system-level, or expensive to change.

## Decision Record

For meaningful architecture choices, state:

- Selected approach
- Alternatives considered
- Why this is enough
- Validation plan
- Quality attribute scenarios
- Risks and tradeoffs
- Expected extension points
