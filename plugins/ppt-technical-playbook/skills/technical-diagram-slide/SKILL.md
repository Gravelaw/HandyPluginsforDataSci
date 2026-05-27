---
name: technical-diagram-slide
description: Design technical PowerPoint diagram slides including architecture diagrams, data flows, process maps, sequence flows, state machines, deployment views, API flows, workflows, implementation graphics, source-figure recreations, and research flow charts.
---

# Technical Diagram Slide

Use this skill when a PowerPoint deck needs an accurate visual explanation, not a decorative graphic.

Read `../../references/technical-playbook-design.md` when building a substantial diagram system.

## Diagram Workflow

1. Classify the diagram: architecture, data flow, sequence, state, deployment, workflow, lifecycle, dependency, risk map, or source-figure recreation.
2. Define the audience question: what should the viewer understand in 10 seconds?
3. Choose one visual grammar: swimlanes, layers, timeline, nodes/edges, stack, state machine, matrix, step flow, system boundary map, or annotated screenshot.
4. Encode meaning consistently: color for domain/status, line style for dependency, icon for component type, shape for state or artifact.
5. Center arrows and connectors on shape anchors; keep connector routing orthogonal or curved consistently; avoid arrows that appear to hit whitespace.
6. Label directly. Avoid legends unless there are many repeated symbols.
7. Add a short caption explaining the implication.
8. For editable PowerPoint, use native shapes, connectors, icons, charts, and text where possible. Use raster images only when the evidence itself is an image or screenshot.

## Quality Gates

- Every node and connector has a reason to exist.
- Directionality is obvious at thumbnail size.
- Boundaries, layers, handoffs, and trust zones are visible when relevant.
- Icons share one visual family and stroke weight.
- Complex diagrams have progressive reveal, zoom-in companion slides, or appendix details.
