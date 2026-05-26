---
name: frontend-implementation
description: Implement frontend UI changes with strong design quality, accessibility, responsive behavior, platform fit, and engineering verification. Use when building or modifying React, TypeScript, CSS, Tailwind, Vite, Next.js, Electron, Tauri, desktop shells, dashboards, forms, app shells, design-system components, charts, or workflow screens.
---

# Frontend Implementation

Use this skill when the user wants a frontend built, not just described.

## Implementation Rules

1. Read the existing app before editing: package manager, component library, router, styling, tokens, tests, linting, and dev scripts.
2. Match the product category. Dashboards, ML tools, CRMs, and operational apps should be quiet, dense, and efficient; marketing pages and games can be more expressive.
3. Prefer established local components and tokens. Add new primitives only when repetition or a missing interaction justifies it.
4. Build complete UI states: default, hover, focus, disabled, loading, empty, error, success, long content, narrow viewport, and dark mode when the app supports it.
5. Use semantic HTML and accessible primitives. Never make icon-only controls without accessible names.
6. Avoid layout fragility: define stable dimensions for boards, grids, toolbars, tiles, charts, and buttons so dynamic text or state changes do not shift the page.
7. For data-heavy screens, optimize scanability: aligned columns, compact labels, predictable controls, subdued decoration, and visible status.
8. For canvas or workflow tools, separate graph data, view state, execution state, validation, keyboard alternatives, and undo/redo.

## Verification

Run the narrowest checks that prove the change: typecheck, lint, unit tests, interaction tests, build, and visual screenshots as available. If the app needs a dev server, start it and provide the URL.

## References

- `../../references/frontend-architecture-reference.md` for structure and library choices.
- `../../references/frontend-quality-gates.md` for verification gates.
- `../../references/cross-platform-ui-reference.md` for desktop and cross-platform UI specifics.
