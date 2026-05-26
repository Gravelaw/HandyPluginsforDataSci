# Frontend Quality Gates

Choose gates based on risk and the repo's tooling.

## Static And Build

- TypeScript or type check where configured.
- Lint and format checks.
- Production build.
- Bundle analysis when adding large dependencies.
- Desktop packaging smoke check when the target is Electron, Tauri, Qt, SwiftUI, WinUI, WPF, or .NET MAUI.

## Interaction

- Unit tests for pure transformation logic and state machines.
- Component tests for forms, menus, dialogs, tables, and canvas controls.
- End-to-end tests for primary flows, destructive actions, auth-sensitive routes, and long-running operation feedback.

## Accessibility

- Keyboard-only smoke test.
- Automated axe or equivalent where available.
- Focus trap checks for modals, drawers, popovers, command palettes, and context menus.
- Screen-reader sanity path for custom widgets, chart summaries, and canvas outlines.

## Visual And Responsive

- Screenshot desktop and mobile breakpoints.
- For desktop apps, screenshot common window sizes, minimum supported window size, high DPI scaling, native dark/light modes, and platform menu/dialog states.
- Check loading, empty, error, success, long content, dark mode, and reduced motion.
- Watch for clipping, overlap, text overflow, scroll traps, layout shift, and hidden focus.
- For canvas/WebGL/charts, verify nonblank rendering and primary controls at multiple viewport sizes.

## Performance

- Keep Core Web Vitals in mind: LCP under 2.5s, INP under 200ms, CLS under 0.1 as target thresholds.
- Use virtualization for large lists, tables, canvases, and logs.
- Use Web Workers or server-side jobs for expensive processing.
- Code split heavy editors, charting suites, and workflow builders when they are not needed on first load.
- For desktop apps, watch launch time, renderer memory growth, idle CPU, background task behavior, GPU-heavy effects, and update/download flows.
