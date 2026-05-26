---
name: python-debugging
description: Diagnose, reproduce, and fix Python exceptions, test failures, import errors, virtual environment issues, dependency conflicts, notebook failures, model training failures, data pipeline errors, logging issues, type-check failures, and performance regressions.
---

# Python Debugging

Use this skill when Python code, tests, installs, imports, notebooks, or model/data commands fail.

Read `../../references/python-official-workflow.md` and `../../references/analysis-workflow-handoff.md` for substantial work.

## Debug Loop

1. Capture the exact command and smallest useful error output.
2. Reproduce with the narrowest command possible.
3. Classify the failure: syntax, import, environment, dependency, type, data, logic, resource, network, performance, or flaky external service.
4. Inspect the active interpreter, virtual environment, `pyproject.toml`, requirements, imports, and changed files.
5. Form one hypothesis at a time.
6. Apply the smallest fix.
7. Rerun the narrow failing command.
8. Rerun broader verification only after the narrow check passes.

## Standard Surfaces

- Tracebacks and first project-owned stack frame for correctness bugs.
- `python -m unittest` or `pytest` for test reproduction.
- `python -m pdb` when step-through inspection is useful.
- `logging`, warnings, and focused assertions for runtime state.
- `profile`/`cProfile`, `timeit`, and `tracemalloc` for performance and allocation questions.
- `pip check`, import smoke tests, and dependency metadata for environment failures.

## Required Handoff

If a failure blocks validation, hand off once to `debug-test-failures` from `analysis-engineering-workflow`. If the root cause changes architecture, security, data, or AI/ML risk, hand off to `framework-compliance-review` before finalizing.
