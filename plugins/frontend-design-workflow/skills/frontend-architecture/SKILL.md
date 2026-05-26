---
name: frontend-architecture
description: Design frontend application architecture and design-system structure for web, desktop, and cross-platform apps. Use when choosing module boundaries, component hierarchy, routing, windows, native shell integration, feature slices, design tokens, theming, state management, canvas architecture, data visualisation libraries, or frontend package structure for React, TypeScript, Vite, Next.js, Electron, Tauri, SwiftUI, WinUI, WPF, Qt, or similar UI stacks.
---

# Frontend Architecture

Use this skill before implementation when frontend structure, design-system foundations, or shared UI contracts matter.

## Workflow

1. Inspect the existing app structure, dependencies, component library, routing model, styling system, test setup, and design tokens before proposing new structure.
2. Choose the smallest architecture that fits the product. Prefer existing conventions over introducing Feature-Sliced Design, Atomic Design, or a new state layer.
3. Separate concerns: product routes and app shell, feature workflows and command surfaces, domain entities and data contracts, shared primitives/tokens/utilities/accessibility helpers.
4. Define design-system contracts: tokens, typography, spacing, elevation, motion, icons, density, breakpoints, dark mode, and component states.
5. Pick state boundaries deliberately: server state, local UI state, canvas state, form state, undo/redo history, and long-running task status.
6. Add quality gates: type checks, unit tests for pure behavior, interaction tests, accessibility tests, visual screenshots, and bundle/performance checks.

## Architecture Heuristics

- Use Feature-Sliced Design for large, domain-heavy frontends with many workflows.
- Use Atomic Design for component library organization, not as the entire app architecture.
- Use design tokens for all color, type, spacing, radius, shadow, and motion decisions that must theme or scale.
- Use accessible headless primitives when visual freedom matters; use enterprise component systems when dense tables, forms, and governance matter.
- For node/canvas builders, isolate graph model, rendering, selection, keyboard operations, validation, and execution state.

## References

- `../../references/frontend-architecture-reference.md` for framework and library decision notes.
- `../../references/design-framework-layers.md` for how architecture fits the broader design model.
