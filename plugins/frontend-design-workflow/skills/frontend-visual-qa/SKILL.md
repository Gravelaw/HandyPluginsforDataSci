---
name: frontend-visual-qa
description: Verify frontend visual quality, responsive behavior, interaction states, accessibility smoke checks, and canvas rendering after implementation. Use when asked to test UI polish, inspect screenshots, run Playwright, check mobile/desktop layout, detect overlaps, verify generated visuals, or validate frontend build quality.
---

# Frontend Visual QA

Use this skill after building or changing frontend UI. Prefer real browser verification over code inspection alone.

## Verification Workflow

1. Start or reuse the app dev server. Capture the URL and relevant route.
2. Run deterministic checks first: lint, typecheck, tests, build, and known accessibility tooling when available.
3. Use Playwright or the project's browser test stack to inspect desktop and mobile viewports.
4. Capture screenshots for key states: default, empty, loading, error, long content, modal/drawer open, dark/light theme, and narrow viewport.
5. Check for text clipping, overlaps, layout jumps, invisible focus, offscreen menus, low contrast, disabled controls without explanation, and scroll traps.
6. For canvas, WebGL, charts, maps, or generated media, perform a nonblank pixel check and verify controls do not obscure the primary scene.
7. If issues are found, fix and rerun the smallest check that proves the fix before broader checks.

## Output Shape

Report what was verified, where screenshots or artifacts live if generated, any failures, and residual risk. Keep screenshots and browser observations tied to viewport sizes.

## References

- `../../references/frontend-quality-gates.md` for checklists and acceptance criteria.
- `../../references/accessibility-compliance-checklist.md` for accessibility smoke checks.
