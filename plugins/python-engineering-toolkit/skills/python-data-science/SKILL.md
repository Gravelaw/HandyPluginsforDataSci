---
name: python-data-science
description: Build, review, or debug Python data analysis, data science, ML engineering, AI engineering, notebooks, feature pipelines, evaluation workflows, visualizations, and reproducible experiment code. Use when the task involves pandas, Polars, NumPy, scikit-learn, statsmodels, PyTorch, transformers, datasets, metrics, features, reports, or notebooks.
---

# Python Data Science

Use this skill for Python analytics, ML, and AI work. Prefer official Python docs for runtime behavior and upstream package docs for package APIs.

Read `../../references/python-official-workflow.md` and `../../references/analysis-workflow-handoff.md` for substantial work.

## Workflow

1. Identify the data contract: source, schema, dtypes, keys, timestamps, units, target, privacy class, and update cadence.
2. Preserve raw data. Write derived artifacts to controlled folders such as `data/interim/`, `data/processed/`, `models/`, or `artifacts/`.
3. Choose the smallest reliable stack: NumPy/pandas/Polars, scikit-learn/statsmodels, PyTorch/transformers, DuckDB/Arrow, or plotting libraries already present.
4. Prevent leakage: split before target-aware transforms, keep validation/test untouched, and document feature provenance.
5. Record reproducibility evidence: random seeds, package versions, data snapshot, metric definitions, and command/notebook path.
6. Move reusable notebook logic into modules or scripts.
7. Verify with data checks, metric smoke tests, model artifact load tests, and focused unit tests when possible.

## Review Checks

- Are joins validated for cardinality and missing keys?
- Are nulls, outliers, and type coercions explicit?
- Are train/validation/test boundaries preserved?
- Are model metrics compared to a baseline?
- Are charts labeled with units and data source?
- Are large files, secrets, credentials, and raw sensitive data kept out of source control?

## Required Handoff

After the Python data-science pass, hand off once to `analysis-engineering-workflow`. Use `framework-compliance-review` for AI/ML risk, data correctness, privacy, security, public-release, or production deployment concerns.
