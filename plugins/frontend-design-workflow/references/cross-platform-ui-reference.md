# Cross-Platform UI Reference

## Scope

Use this reference for web, Windows, macOS, Linux, Electron, Tauri, Qt, SwiftUI/AppKit, WinUI, WPF, and .NET MAUI UI work.

## Shared Product Model

- Keep navigation, terminology, object model, and core flows consistent across platforms.
- Use platform-specific wrappers for menus, shortcuts, file dialogs, notifications, deep links, clipboard, tray/menu bar extras, and update prompts.
- Treat desktop window size as responsive design. Minimum window size, restored size, full-screen mode, split-screen, and high-DPI scaling all need attention.

## Desktop Interaction Checklist

- Native or credible menu structure: File, Edit, View, Window, Help where appropriate.
- Keyboard shortcuts with platform modifiers: Command on macOS, Ctrl on Windows/Linux.
- Unsaved-change prompts, recent files, open/save/export/import, and drag/drop file handling.
- System theme support: light, dark, high contrast, reduced motion.
- Offline and reconnecting states when the app can work without network.
- Permission prompts for filesystem, camera, microphone, screen capture, notifications, and local network.
- Update flow: available, downloading, ready to restart, failed update.

## Layout Patterns

- App shell: sidebar plus content for productivity apps; toolbar plus inspector for creative tools; document window for file-centric apps.
- Settings: searchable settings for large apps; platform-native preferences location when appropriate.
- Multi-window: define whether state is per window, shared globally, or document-scoped.
- Status: long tasks need progress, cancel, retry, logs/details, and background completion notifications.

## Verification

- Browser: desktop, tablet, narrow mobile, keyboard-only, zoomed text.
- Desktop: minimum supported window, common laptop size, external monitor, high DPI, dark/light, high contrast if available.
- Shell: native menus, shortcuts, dialogs, offline state, permission denial, update prompt, close/reopen state persistence.
