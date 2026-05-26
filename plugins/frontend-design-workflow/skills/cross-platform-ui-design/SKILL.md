---
name: cross-platform-ui-design
description: Design and adapt frontend UI/UX for web, Windows, macOS, Linux, Electron, Tauri, Qt, SwiftUI, AppKit, WinUI, WPF, .NET MAUI, and cross-platform product surfaces. Use when a user asks for desktop app design, platform conventions, responsive/adaptive behavior, native menus, window layouts, keyboard shortcuts, system theming, offline states, or converting a web UI concept into a desktop or cross-platform app.
---

# Cross-Platform UI Design

Use this skill when the same product experience must work across web and desktop platforms, or when a native desktop interface needs frontend design judgment.

## Workflow

1. Identify target platforms, implementation shell, input methods, window constraints, offline expectations, and OS integration requirements.
2. Preserve the product's core interaction model, then adapt platform affordances: menus, title bars, shortcuts, file dialogs, notifications, drag/drop, clipboard, and deep links.
3. Respect platform conventions without duplicating every native app detail. The product should feel coherent across platforms and credible inside each platform.
4. Design responsive and adaptive layouts for browser widths, desktop window resizing, high DPI, touch screens, external monitors, and reduced-motion/high-contrast modes.
5. Define state coverage: first launch, signed out, offline, syncing, update available, permissions denied, unsaved changes, long-running task, empty project, error recovery.
6. Plan verification with real browser and desktop shell screenshots when possible.

## Platform Heuristics

- Web: strong responsive behavior, URL/routing, browser accessibility, loading states, and keyboard/focus paths.
- macOS: menu bar conventions, document/window model, Command-key shortcuts, vibrancy only when appropriate, sidebar and toolbar discipline.
- Windows: clear command surfaces, WinUI-style density where relevant, Alt-key/menu accessibility, high contrast, snap layouts, and taskbar integration.
- Electron/Tauri: isolate native bridge/IPC, avoid blocking renderer work, handle update and permission states visibly.
- Cross-platform apps: keep shared tokens and components, but allow platform-specific wrappers for menus, dialogs, shortcuts, notifications, and filesystem flows.

## References

- `../../references/cross-platform-ui-reference.md` for platform patterns and verification checks.
- `../../references/frontend-quality-gates.md` for quality gates.
