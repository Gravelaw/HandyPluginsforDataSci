# PowerPoint Production Handoff

Use the built-in `Presentations` skill as the production engine whenever the user wants an editable `.pptx`, rendered previews, contact sheets, or slide QA.

Handoff exactly once:

- If `Presentations` is already active in the current task, do not re-trigger it.
- If the task is only strategy, outline, critique, or slide rewrite, no production handoff is needed.
- If actual PowerPoint creation/editing is requested, apply this layer's strategy first, then invoke `Presentations`.

Production expectations:

- Use editable PowerPoint output, not flat screenshots.
- Render previews and inspect contact sheets before final handoff.
- Keep final deliverables separate from scratch files.
- Preserve template fidelity when the user supplies a source deck.
- Use verified brand assets; do not invent logos or identity marks.
