---
name: post-execution-review
description: Review work after execution for coding, ML, analytics, data science, AI engineering, and system design tasks using framework gate evidence. Use after tests, scripts, notebooks, package installs, model runs, architecture reviews, or compliance-style checks to inspect results, diffs, artifacts, residual risks, and next actions.
---

# Post Execution Review

Use this skill after commands have run.

## Review Steps

1. Inspect changed files and generated artifacts.
2. Compare results with the original success criteria.
3. Compare results with selected framework gates from `../../references/governed-engineering-framework.md`.
4. Summarize commands run and whether they passed.
5. Identify residual risks: skipped checks, long-running jobs, package resolver compromises, flaky tests, unverified assumptions, missing threat model, missing quality scenario, or missing AI/ML evidence.
6. Confirm no secrets, large raw data, caches, or transient artifacts were accidentally added.
7. Give a gate decision: pass, pass with conditions, or block.
8. Recommend the next highest-value action only when it materially helps.

## Output Shape

Keep the summary brief:

- Changed
- Verified
- Gate decision
- Residual risks
- Next action, if needed
