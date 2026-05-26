---
name: plan-work
description: Plan coding, ML, data analysis, data science, AI engineering, and system design tasks before implementation using a governed review framework. Use when a task is broad, risky, cross-file, experimental, data-dependent, security-sensitive, architecture-relevant, or likely to need staged execution and validation.
---

# Plan Work

Use this skill to turn an ambiguous or multi-step request into an executable plan.

For substantial work, read `../../references/governed-engineering-framework.md` and choose the relevant lifecycle, architecture, quality, security, AI, and review gates.

## Workflow

1. Restate the goal in one or two concrete sentences.
2. Identify constraints: runtime, data availability, privacy, compute budget, language, package manager, and user deadlines.
3. Identify lifecycle phase and exit criteria using ISO/IEC/IEEE 12207 or system-style 15288 thinking.
4. Inspect existing files before proposing structure.
5. Define stakeholders, concerns, and system of interest when architecture matters.
6. Define success criteria: tests, import checks, metric thresholds, plots, artifacts, reproducibility outputs, quality attribute scenarios, or gate evidence.
7. List risks: data leakage, package compatibility, hidden state, long-running jobs, credentials, non-determinism, threat model gaps, missing observability, and destructive commands.
8. Split the work into small steps with one active step at a time.
9. Name when to invoke the next workflow skill: `architect-work`, `framework-compliance-review`, `implement-work`, `execute-verify`, or `debug-test-failures`.

## Output Shape

Prefer a short plan with:

- Goal
- Assumptions
- Steps
- Validation
- Framework gates
- Risks or open questions

Do not over-plan tiny tasks. For simple edits, proceed directly after a quick mental plan.
