---
name: implement-work
description: Implement scoped Python and Julia code changes for ML engineering, data analysis, data science, AI engineering, tooling, tests, documentation, and system support code while preserving governed engineering review evidence. Use after planning, architecture, and relevant framework gates are clear and the task requires file edits.
---

# Implement Work

Use this skill to make the change.

## Implementation Rules

1. Inspect the relevant files immediately before editing.
2. Preserve user changes and avoid unrelated refactors.
3. Prefer existing patterns and standard libraries before new abstractions.
4. Keep functions small, typed where useful, and explicit about inputs and outputs.
5. Preserve architecture decisions, contracts, and framework gate evidence from planning or review.
6. Validate data boundaries: schema, shape, dtype, missing values, units, and target leakage.
7. Implement security defaults from NIST SSDF and OWASP where applicable: input validation, least privilege, safe secrets handling, safe deserialization, dependency hygiene, and useful logs.
8. Apply NASA/JPL discipline to critical paths: bounded loops, narrow scope, checked errors, assertions, and automated checks.
9. Add focused tests or smoke checks for changed behavior and risk claims.
10. Keep notebooks exploratory. Move reusable logic into scripts or modules.
11. Use `apply_patch` for manual edits.
12. Keep comments sparse and useful.
13. After editing, invoke `execute-verify` for checks.

## Package Choices

Use mature packages for core domain logic:

- Python: NumPy, pandas, Polars, scikit-learn, PyTorch, transformers, statsmodels, PyArrow, DuckDB, pytest, ruff.
- Julia: DataFrames, CSV, Arrow, MLJ, Flux, GLM, StatsBase, Plots, Aqua, JET, JuliaFormatter.
