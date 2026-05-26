---
name: frontend-accessibility-review
description: Review frontend UI, code, prototypes, or designs for accessibility, inclusive interaction, and related compliance risks. Use when asked to audit WCAG, keyboard navigation, screen reader behavior, focus management, color contrast, drag-and-drop alternatives, forms, charts, dashboards, EU Accessibility Act exposure, Section 508, ADA risk, or privacy/transparency UX.
---

# Frontend Accessibility Review

Use this skill in a review stance. Findings come first, ordered by severity, with concrete locations when code is available.

## Review Method

1. Identify the target standard and product context. Default to WCAG 2.2 AA for modern public web apps unless the user specifies another bar.
2. Inspect semantics, names, roles, states, keyboard order, focus visibility, focus trapping, escape paths, and screen-reader announcements.
3. Check perceivability: contrast, text resizing, motion reduction, chart alternatives, labels, error text, non-color encodings, and responsive zoom.
4. Check operability: all pointer-only, drag-only, hover-only, gesture-only, and canvas operations need keyboard or non-drag alternatives.
5. Check understandability: predictable navigation, form instructions, validation timing, consistent help, and recoverable destructive actions.
6. Check robustness: semantic HTML first, ARIA only when needed, stable ids, live-region restraint, and tested behavior in assistive tech paths.
7. For data or AI products, review privacy, consent, transparency, model-output explanation, human oversight, and confidence/fairness presentation.

## Output Shape

- Findings first with severity, file/line or screen reference, user impact, and suggested fix.
- Then residual risks and tests that were or were not run.
- Keep legal phrasing cautious: identify compliance risk, not legal advice.

## References

- `../../references/accessibility-compliance-checklist.md` for standards-backed checks.
- `../../references/source-research-summary.md` for source dates and official references.
