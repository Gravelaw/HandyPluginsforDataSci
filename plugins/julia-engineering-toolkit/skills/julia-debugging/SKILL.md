---
name: julia-debugging
description: Diagnose, reproduce, and fix Julia errors, stack traces, package-loading failures, logging issues, type-instability problems, test failures, Pkg/environment issues, notebook failures, model failures, and performance regressions.
---

# Julia Debugging

Use this skill to debug Julia code systematically. Prefer official Julia and Pkg documentation for language behavior, package loading, stack traces, logging, profiling, performance, tests, and environments.

Read `../../references/julia-official-workflow.md` and `../../references/analysis-workflow-handoff.md` for substantial work.

## Debug Loop

1. Capture the exact failing command and smallest useful output.
2. Reproduce with the narrowest command possible.
3. Confirm Julia version, active project, `Project.toml`, `Manifest.toml`, imports, and package versions.
4. Classify the failure: exception, wrong result, package/environment, precompilation, type stability, allocation/performance, notebook, model/data, or external dependency.
5. Start with the exception type and first useful project-owned stack frame.
6. Form one hypothesis at a time.
7. Apply the smallest fix.
8. Rerun the narrow failing command.
9. Rerun broader verification after the narrow check passes.

## Standard Surfaces

- Stack traces and minimal examples for correctness bugs.
- `Pkg.status()`, `Pkg.instantiate()`, and active-project checks for environment failures.
- `Test`, `@test_throws`, and `@test_logs` for behavior and log assertions.
- `@debug`, `@info`, `JULIA_DEBUG`, and `Logging` for runtime state.
- `@code_warntype`, allocation checks, `Profile`, JET, and BenchmarkTools for type/performance questions.

## Common Failure Modes

- `UndefVarError`: missing import, scope issue, renamed API, or Unicode lookalike.
- `MethodError`: wrong argument types, missing module qualification, or API mismatch.
- Package load/precompile failure: wrong active environment, stale manifest, missing dependency, or compatibility bounds.
- Slow code: global state, type instability, abstract containers, allocation-heavy hot paths, or top-level loops.

## Required Handoff

If a failure blocks validation, hand off once to `debug-test-failures` from `analysis-engineering-workflow`. If the root cause changes architecture, security, data, or AI/ML risk, hand off to `framework-compliance-review` before finalizing.
