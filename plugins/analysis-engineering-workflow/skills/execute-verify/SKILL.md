---
name: execute-verify
description: Execute and verify Python, Julia, ML, data analysis, data science, AI engineering, and system support code after changes using risk-based evidence gates. Use to run tests, linters, type checks, import checks, notebooks, package checks, security checks, scripts, reproducibility smoke tests, and compliance-style readiness checks.
---

# Execute Verify

Use this skill after implementation or environment changes.

## Verification Ladder

Run the smallest relevant check first, then broaden:

1. Syntax or import checks for touched files.
2. Focused tests for changed behavior.
3. Linters and format checks.
4. Type/static checks where configured.
5. Package or project tests.
6. Security, dependency, or policy checks when NIST SSDF or OWASP gates apply.
7. Data/ML checks: schema validation, leakage checks, deterministic split checks, metric reproduction, model artifact load, and drift/monitoring smoke checks.
8. End-to-end smoke commands, notebooks, or sample pipelines.
9. Record evidence for the selected gate: command, result, artifact, and residual risk.

## Python Commands

Prefer:

```bash
.venv/bin/python -m pytest
.venv/bin/python -m ruff check .
.venv/bin/python -m mypy src
.venv/bin/python scripts/check_python_environment.py
```

## Julia Commands

Prefer:

```bash
julia --project=. -e 'using Pkg; Pkg.test()'
julia --project=. scripts/check_julia_environment.jl
julia --project=. -e 'using JuliaFormatter; format(".", verbose=true)'
```

## Failure Rule

If a check fails and the cause is not obvious, invoke `debug-test-failures`. Capture the command, relevant output, first suspected cause, next smallest reproduction, and which framework gate remains blocked.
