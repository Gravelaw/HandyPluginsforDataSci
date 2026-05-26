# Accessibility And Compliance Checklist

This is engineering guidance, not legal advice.

## Baseline

- Default to WCAG 2.2 AA for public-facing modern web work.
- Use semantic HTML first; add ARIA only to fill semantic gaps.
- Every interactive element needs a name, role, state, focus style, keyboard path, and disabled/loading/error behavior.
- Test with keyboard only before relying on automated tools.

## WCAG 2.2 Hotspots

- Focus must remain visible and not be hidden under sticky headers, drawers, toasts, or panels.
- Dragging operations need non-drag alternatives.
- Target sizes need enough hit area unless an exception clearly applies.
- Help mechanisms should appear in a consistent place when provided.
- Avoid redundant re-entry for information already provided in the same process.

## Canvas And Workflow UIs

- Provide keyboard add, select, move, connect, disconnect, delete, and configure operations.
- Give nodes, ports, and edges accessible names and visible focus states.
- Announce execution state changes without flooding live regions.
- Provide a textual workflow summary or outline for screen reader and audit paths.
- Invalid connections should explain the incompatible types or missing prerequisites.

## Data Visualization

- Do not rely on color alone; pair hue with labels, icons, patterns, or shape.
- Label axes, units, legends, and time ranges.
- Provide table equivalents or summaries for critical charts.
- Ensure tooltips are keyboard reachable or duplicate information in the DOM.

## Privacy, Consent, And AI Transparency

- Consent must be explicit, granular, reversible, and symmetric in accept/decline effort.
- Request sensitive data access just in time.
- Surface data scope, retention, export, and deletion controls.
- For ML/AI outputs, show assumptions, confidence, limitations, human review paths, and model/data lineage where relevant.

## Review Output

For each finding, include severity, impacted users, evidence, recommended fix, and verification method.
