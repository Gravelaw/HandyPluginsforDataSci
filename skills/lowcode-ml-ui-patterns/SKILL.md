---
name: lowcode-ml-ui-patterns
description: Design low-code and no-code ML, analytics, AI, workflow-builder, node-canvas, pipeline, data-science, and automation UIs. Use when planning or implementing node-based canvases, dataset previews, model training flows, experiment dashboards, dual beginner/expert modes, code escape hatches, execution feedback, explainability panels, or data visualization UX.
---

# Low-Code ML UI Patterns

This standalone global skill preserves the ML/data-science-specific material separately from the broad frontend design plugin.

## Pattern Stack

1. Start with the three-panel shell: navigation or palette on the left, canvas or main workspace in the center, properties/results on the right, with logs or data preview available below.
2. Model the primary object lifecycle: project, dataset, pipeline, node, run, artifact, model, report, deployment.
3. Use progressive disclosure: beginner templates and guided setup, basic configuration first, advanced tabs or code escape hatches for experts.
4. Make execution legible: stage progress, cancellability, node status, partial results, logs, retry, and exact failure localization.
5. Make canvas interactions accessible: keyboard add/connect/move/delete, non-drag alternatives, focus-visible nodes/ports, and textual path summaries.
6. Treat data visualization as UI, not decoration: labeled axes, legends, units, accessible color, tooltips, brushing, and text alternatives.
7. For AI/ML outputs, include transparency: model card, confidence, data lineage, assumptions, fairness caveats, and human review/override where relevant.

## References

- `references/lowcode-ml-ui-patterns.md` for the detailed pattern catalog.
- `references/accessibility-compliance-checklist.md` for canvas and chart accessibility.
