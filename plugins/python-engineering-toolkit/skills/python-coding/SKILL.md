---
name: python-coding
description: Implement, review, refactor, or explain Python code for software engineering, data science, ML, AI engineering, APIs, packages, scripts, notebooks, tests, and tooling. Use when the user asks for Python code, Python project structure, Python package management, Python type/lint/test setup, or Python library selection.
---

# Python Coding

Use this skill for Python implementation and review work. Prefer official Python documentation and Python Packaging guidance for language, environment, packaging, testing, logging, debugging, typing, and profiling behavior.

Read `../../references/python-official-workflow.md` for substantial Python work. Read `../../references/analysis-workflow-handoff.md` before handing off to governed workflow skills.

## Workflow

1. Identify the task shape: script, notebook, package, API/service, data pipeline, ML/AI workflow, test suite, or tooling.
2. Inspect existing project files before changing conventions: `pyproject.toml`, `requirements/`, `src/`, `tests/`, `notebooks/`, `scripts/`, and lockfiles.
3. Use a project-local environment, normally `.venv`, and run tools through the environment's Python.
4. Prefer `src/` layout for reusable code and keep notebooks exploratory.
5. Make functions explicit about inputs, outputs, errors, units, schemas, and side effects.
6. Add or update focused tests for changed behavior.
7. Use existing dependencies where possible; add packages only when they remove real complexity.
8. For package choices or volatile ecosystem questions, browse current upstream docs before recommending.

## Python Commands

Prefer these shapes when relevant:

```bash
python3 -m venv .venv
.venv/bin/python -m pip install -r requirements/all.txt
.venv/bin/python -m pytest
.venv/bin/python -m unittest
.venv/bin/python -m ruff check .
.venv/bin/python -m mypy src
```

## Quality Bar

- Keep code idiomatic, typed where useful, and testable.
- Use `logging` for reusable code instead of print-driven diagnostics.
- Avoid hidden global state, import-time side effects, unsafe deserialization, shell injection, and mutable default arguments.
- Validate data boundaries: shape, dtype, missingness, identifiers, timestamps, units, and leakage risks.
- For ML/AI, record seeds, splits, metrics, model artifact paths, and dependency versions.

## Required Handoff

After the Python-specific pass, hand off once to `analysis-engineering-workflow` using `../../references/analysis-workflow-handoff.md`. Skip only if the workflow is already active in the current task.
