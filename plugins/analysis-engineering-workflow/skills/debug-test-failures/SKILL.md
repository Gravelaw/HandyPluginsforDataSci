---
name: debug-test-failures
description: Debug Python and Julia test failures, runtime errors, package install errors, notebook failures, model training failures, data pipeline errors, verification gate failures, and compliance-style check failures. Use when commands fail during setup, execution, testing, linting, type checking, package precompilation, security checks, reproducibility checks, or framework-gated review.
---

# Debug Test Failures

Use this skill when a command fails.

## Debug Loop

1. Capture the exact failing command and the smallest relevant output.
2. Reproduce with the narrowest command possible.
3. Classify the failure: environment, dependency, syntax, type, logic, data, resource, network, or flaky external service.
4. Classify the blocked gate: quality, security, architecture, reproducibility, AI/ML, deployment, operations, or lifecycle evidence.
5. Inspect the implicated code, design contract, data contract, or dependency metadata.
6. Form one hypothesis at a time.
7. Apply the smallest fix.
8. Rerun the narrow failing command.
9. Rerun the broader verification command after the narrow check passes.
10. Update residual risk if the fix changes a quality attribute tradeoff.

## Environment Failures

- For Python 3.13, suspect packages without compatible wheels before assuming user error.
- For Julia 1.12, suspect packages with strict compatibility bounds before forcing resolver changes.
- Prefer optional requirement groups over weakening the whole environment.

## Output Shape

Report:

- Failing command
- Root cause or best current hypothesis
- Fix applied
- Verification rerun
- Gate unblocked or still blocked
- Remaining issue, if any
