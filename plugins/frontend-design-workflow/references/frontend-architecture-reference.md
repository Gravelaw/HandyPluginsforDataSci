# Frontend Architecture Reference

## Choosing Structure

- Existing project conventions win by default.
- Small app: screens/routes/windows, components, hooks or controllers, utilities, styles, tests.
- Medium app: screens/routes/windows, features, entities/domain, shared UI, shared lib.
- Large domain app: Feature-Sliced Design with `app`, `pages`, `widgets`, `features`, `entities`, and `shared`, adjusted to the repo.
- Desktop app: separate shell/window lifecycle, native menu/tray/dialog integration, renderer UI, IPC boundary, persisted settings, and update flow.

## Design System Structure

Recommended categories:

- `primitives`: Button, Input, Select, Checkbox, Radio, Switch, Slider.
- `navigation`: AppShell, Sidebar, TopBar, Tabs, Breadcrumbs, CommandPalette.
- `feedback`: Toast, Alert, Progress, Skeleton, Spinner, EmptyState.
- `data-display`: Table, DataGrid, Badge, Tag, Stat, Metric, Timeline.
- `charts`: Line, Bar, Scatter, Heatmap, ConfusionMatrix, ROC, FeatureImportance.
- `canvas`: CanvasNode, CanvasEdge, NodePort, MiniMap, ToolPalette, SelectionBox.
- `panels`: PropertiesPanel, DataPreview, LogsPanel, Inspector, MetricsPanel.
- `overlays`: Dialog, Drawer, Tooltip, Popover, ContextMenu.

## Library Heuristics

- Enterprise/data-heavy apps: Carbon, Ant Design, Fluent UI, or MUI.
- Custom visual system with strong accessibility: Radix UI, React Aria, or similar headless primitives.
- Highly custom styling: Tailwind plus a disciplined token layer.
- Node workflows: React Flow / xyflow when React is available; avoid hand-rolling graph interaction unless the app has very unusual requirements.
- Charts: Recharts for simple React dashboards, Vega-Lite for grammar-driven analysis, Plotly for scientific interactivity, ECharts for large interactive datasets.
- Desktop shells: Electron for broad ecosystem compatibility, Tauri for smaller Rust-backed shells, native SwiftUI/AppKit for macOS-first apps, WinUI/WPF/.NET MAUI for Windows-first apps, Qt for cross-platform native widgets.

## State Boundaries

- Server/cache state: TanStack Query or the repo's existing data layer.
- Local UI state: component state or lightweight store.
- Canvas graph state: explicit store with undo/redo and schema versioning.
- Forms: framework or library already used by the repo.
- Execution state: finite states for idle, queued, running, canceling, succeeded, warning, failed.
- Desktop integration state: filesystem permissions, recent files, clipboard, native dialogs, notifications, auto-update, deep links, and offline sync.

## Token Requirements

Tokens should include primitive and semantic colors, type scale, line height, spacing, radius, elevation, focus rings, z-index, motion duration, motion easing, density, and breakpoints. Semantic tokens should be used in components; primitive values should stay near the token source.
