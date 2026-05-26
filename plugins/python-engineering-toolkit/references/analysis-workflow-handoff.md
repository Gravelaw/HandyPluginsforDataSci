# Analysis Workflow Handoff

Language-specific skills run first. The governed `analysis-engineering-workflow` plugin runs after the language pass when the task needs planning, architecture, implementation, verification, review, or debugging.

Use exactly one handoff per task phase:

- Broad or ambiguous request: call `plan-work`.
- Design or package structure decision: call `architect-work`.
- Readiness, compliance-style, security, AI/ML, or architecture check: call `framework-compliance-review` or `review-architecture`.
- Code edit after design is clear: call `implement-work`.
- Checks after edits or environment setup: call `execute-verify`.
- Failed command, test, import, install, model run, or notebook: call `debug-test-failures`.
- Final inspection after execution: call `post-execution-review`.

Do not duplicate the handoff if one of these workflow skills is already active or already completed in the current turn. Record the handoff status in working notes as `analysis handoff: done` or `analysis handoff: skipped, already active`.

No additional MCP server or API integration is required for this plugin. Use the available shell, filesystem tools, web browsing for current docs, and the installed workflow skills.
