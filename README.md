# HandyPluginsforDataSci

HandyPluginsforDataSci is a community bundle of Codex plugins and skills for data science, analysis engineering, frontend design, and presentation workflows.

The bundle is authored by Akshay Jain and is intended to be useful for researchers, data scientists, ML engineers, AI engineers, analysts, and builders who want reusable Codex workflow guidance.

## What Is Included

### Plugins

- `analysis-engineering-workflow`: Governed planning, architecture, implementation, verification, review, and debugging workflows for Python, Julia, ML, data, and AI engineering projects.
- `python-engineering-toolkit`: Python coding, debugging, data science, ML, and AI engineering support.
- `julia-engineering-toolkit`: Julia coding, debugging, data science, ML, and package workflow support.
- `frontend-design-workflow`: Broad UI/UX and frontend design support for web, desktop, cross-platform apps, accessibility, architecture, implementation, and visual QA.
- `ppt-technical-playbook`: Detailed technical PowerPoint playbooks, diagrams, and technical deck review.
- `ppt-executive-briefing`: Executive summaries, board decks, pitch decks, and leadership deck review.
- `ppt-training-studio`: Training decks, workshops, learner activities, and instructional design review.

FYI: `python-engineering-toolkit` and `julia-engineering-toolkit` both hand off final planning/review/verification workflows to `analysis-engineering-workflow`. Install `analysis-engineering-workflow` alongside either language toolkit for the intended end-to-end experience.

### Standalone Skill

- `lowcode-ml-ui-patterns`: Low-code/no-code ML, analytics, workflow-builder, node-canvas, and data-science UI patterns.

## Repository Layout

```text
.
├── plugins/
│   ├── analysis-engineering-workflow/
│   ├── frontend-design-workflow/
│   ├── julia-engineering-toolkit/
│   ├── ppt-executive-briefing/
│   ├── ppt-technical-playbook/
│   ├── ppt-training-studio/
│   └── python-engineering-toolkit/
├── skills/
│   └── lowcode-ml-ui-patterns/
├── marketplace.json
├── CITATION.cff
└── LICENSE
```

## Installation Notes

For Codex plugin use, point Codex at `marketplace.json` or copy the desired plugin folder from `plugins/` into your local plugin directory.

For standalone skill use, copy `skills/lowcode-ml-ui-patterns` into your Codex skills directory.

## Citation

If this bundle supports academic or industrial research, please cite it using the metadata in `CITATION.cff`.

Suggested citation:

> Jain, A. (2026). HandyPluginsforDataSci: Codex plugins and skills for data science, frontend design, and presentation workflows. GitHub. https://github.com/Gravelaw/HandyPluginsforDataSci

## License

This project is released under the Apache License 2.0. See `LICENSE`.
