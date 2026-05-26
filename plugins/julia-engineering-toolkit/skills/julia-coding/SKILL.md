---
name: julia-coding
description: Implement, review, refactor, or explain Julia code; set up Julia projects and packages; choose Julia libraries; and follow idiomatic Julia package, module, testing, and Pkg workflows. Use when the user wants help writing Julia, structuring a Julia package, managing Project.toml and Manifest.toml environments, selecting packages, or reviewing Julia-specific code.
---

# Julia Coding

Use this skill for Julia implementation and review work. Prefer official Julia and Pkg documentation for language, package-manager, code-loading, style, performance, testing, logging, and profiling behavior.

Read `../../references/julia-official-workflow.md` for substantial Julia work. Read `../../references/analysis-workflow-handoff.md` before handing off to governed workflow skills.

## Workflow

1. Identify whether the task is script, notebook, package, package selection, data science, ML, debugging, testing, or performance cleanup.
2. Inspect `Project.toml`, `Manifest.toml`, `src/`, `test/`, notebooks, and scripts before changing conventions.
3. Use project-local environments with `julia --project=.` or `Pkg.activate(".")`.
4. For packages, prefer standard layout: `src/PackageName.jl` and `test/runtests.jl`.
5. Write functions rather than top-level scripts for reusable or performance-sensitive code.
6. Prefer generic methods over overly concrete type restrictions unless the API needs them.
7. Avoid type piracy, unnecessary macros, global mutable state, and broad imports in package code.
8. Add docstrings for public functions, types, and modules when touching public API.
9. Use `Test`, `Pkg.test`, JuliaFormatter, Aqua, and JET when configured and relevant.

## Julia Commands

Prefer these shapes when relevant:

```bash
julia --project=. -e 'using Pkg; Pkg.instantiate()'
julia --project=. -e 'using Pkg; Pkg.test()'
julia --project=. -e 'using JuliaFormatter; format(".")'
julia --project=. -e 'using Aqua; Aqua.test_all(YourPackage)'
julia --project=. -e 'using JET; JET.test_package(YourPackage)'
```

## Required Handoff

After the Julia-specific pass, hand off once to `analysis-engineering-workflow` using `../../references/analysis-workflow-handoff.md`. Skip only if the workflow is already active in the current task.
