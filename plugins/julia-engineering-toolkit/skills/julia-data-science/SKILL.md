---
name: julia-data-science
description: Build, review, or debug Julia data analysis, data science, ML engineering, notebooks, feature pipelines, evaluation workflows, visualizations, and reproducible experiment code. Use when the task involves DataFrames, CSV, Arrow, Tables, MLJ, Flux, GLM, StatsBase, Plots, Pluto, IJulia, or Julia data/ML packages.
---

# Julia Data Science

Use this skill for Julia analytics, ML, and scientific/data workflows. Prefer official Julia and Pkg documentation for environment, code-loading, performance, testing, logging, and profiling behavior.

Read `../../references/julia-official-workflow.md` and `../../references/analysis-workflow-handoff.md` for substantial work.

## Workflow

1. Identify the data contract: source, schema, element types, keys, timestamps, units, target, privacy class, and update cadence.
2. Activate the project with `julia --project=.` and instantiate dependencies before running notebooks or scripts.
3. Preserve raw data. Write derived artifacts to controlled folders such as `data/interim/`, `data/processed/`, `models/`, or `artifacts/`.
4. Use package-local, function-based code for stable logic; keep notebooks exploratory.
5. Choose the smallest reliable stack already present: DataFrames/CSV/Arrow/Tables, DuckDB/SQLite, MLJ/Flux/GLM, StatsBase/StatsModels, Plots/StatsPlots.
6. Prevent leakage: split before target-aware transforms, keep validation/test untouched, and document feature provenance.
7. Record reproducibility evidence: random seeds, package versions, manifest status, data snapshot, metric definitions, and command/notebook path.
8. Verify with schema checks, metric smoke tests, model artifact load tests, and focused `Test` checks when possible.

## Julia-Specific Checks

- Are hot paths inside functions?
- Are column element types stable enough for the operation?
- Are joins and missing values explicit?
- Is code relying on global mutable state?
- Does the active environment match the project?
- Are large artifacts, secrets, credentials, and raw sensitive data kept out of source control?

## Required Handoff

After the Julia data-science pass, hand off once to `analysis-engineering-workflow`. Use `framework-compliance-review` for AI/ML risk, data correctness, privacy, security, public-release, or production deployment concerns.
