# Low-Code ML And Analytics UI Patterns

## App Shell

Use a three-panel layout for serious workflow tools:

- Left: project navigation, search, node palette, templates.
- Center: workflow canvas, dashboard, notebook-like builder, or data workspace.
- Right: properties, schema, config, explainability, or selected artifact details.
- Bottom: logs, run timeline, data preview, validation messages, metrics.

Panels should be resizable, collapsible, keyboard reachable, and stable across routes.

## Node Canvas

- Left-to-right flow for data pipelines unless the domain has a stronger convention.
- Use typed ports and validate connections before commit.
- Use consistent node anatomy: icon, name, status, type, primary metadata, ports.
- Status states: idle, dirty, queued, running, success, warning, error, stale.
- Offer minimap, zoom controls, fit-to-view, grid snapping, alignment, grouping, and search.
- Support undo/redo for graph edits and parameter changes.

## Beginner And Expert Modes

- Beginner: templates, guided wizard, sample datasets, inline recommendations, safe defaults.
- Expert: code escape hatches, keyboard shortcuts, advanced parameter tabs, direct schema editing, import/export, versioned configs.
- Do not fork the whole product into two separate apps. Prefer progressive disclosure and saved user preferences.

## Execution Feedback

- Show stage-level progress, not only spinners.
- Make long operations cancellable.
- Stream intermediate results where useful: logs, loss curves, row counts, validation summaries.
- Localize errors to the failed node, field, dataset, or model artifact.
- Provide retry, duplicate-and-edit, and rollback paths.

## ML And AI Trust

- Show dataset lineage and schema assumptions.
- Separate validation metrics from test metrics.
- Warn about target leakage and missing split definitions.
- Include model card fields: intended use, limitations, training data, metrics, fairness notes, owner, version, deployment status.
- Human oversight should be visible when outputs affect users or decisions.

## Onboarding

- Empty canvas should suggest importing data, starting from template, or opening a sample workflow.
- Interactive tutorials should use real controls, not only passive overlays.
- Include 3 to 5 sample projects that demonstrate common tasks.
