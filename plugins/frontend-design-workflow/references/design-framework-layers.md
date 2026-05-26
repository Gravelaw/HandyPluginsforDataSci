# Frontend Design Framework Layers

Use this model to decide which concerns matter for a given frontend task. Do not force every layer into every answer.

## Layer 1: Foundational Theory

- Nielsen heuristics: system status, real-world language, control/freedom, consistency, error prevention, recognition over recall, efficiency, minimalist design, error recovery, help.
- Gestalt principles: proximity, similarity, continuity, closure, figure/ground, common region.
- Cognitive Load Theory: reduce extraneous load, preserve productive learning, do not pretend intrinsic complexity is simple when the domain is complex.
- Norman principles: affordances, signifiers, feedback, constraints, mapping, conceptual model.
- Fitts and Hick: keep frequent actions easy to hit and avoid option overload.

## Layer 2: UX Design Strategy

- User-centered design: context, requirements, design, evaluation, iteration.
- Progressive disclosure: basic path first, advanced options when needed.
- Dual-audience design: beginner guidance plus expert efficiency.
- Information architecture: app shell, navigation, search, breadcrumbs, panels, object model.
- Emotional design: trust through clarity, responsiveness, respectful copy, and visible progress.
- Responsive/adaptive design: prioritize desktop productivity but do not let tablet and narrow layouts break.

## Layer 3: Compliance And Standards

- Default accessibility target: WCAG 2.2 AA for modern web products unless the user names another target.
- Consider EU Accessibility Act exposure for covered EU products and services.
- Include ADA/Section 508 risk where US public or government-adjacent access matters.
- Use privacy-by-design for consent, data scope, export/delete, data minimization, and transparent AI/ML behavior.

## Layer 4: Frontend Architecture

- Match the repo first. Only introduce a methodology if it reduces complexity.
- Feature-Sliced Design is useful for domain-heavy apps with many workflows.
- Atomic Design is useful inside component libraries.
- Design tokens should cover color, typography, spacing, radius, elevation, motion, density, and theme.
- Component libraries should define primitives, navigation, feedback, data display, charts, panels, overlays, and canvas components.

## Layer 5: Domain-Specific Patterns

- Web apps need robust responsive behavior, browser accessibility, URL/routing models, loading states, and resilience across input methods.
- Desktop apps need platform-appropriate windowing, menus, keyboard shortcuts, file/open/save flows, notifications, offline behavior, density, and OS conventions.
- Operational apps need compact layouts, restrained ornament, predictable controls, and fast scanning.
- Consumer apps can use more brand-forward imagery, motion, and editorial hierarchy, but still need robust accessibility and performance.

## Layer 6: Engineering And Performance

- Web performance: Core Web Vitals, bundle size, responsive latency, and layout stability.
- Desktop performance: launch time, memory use, idle CPU/GPU, resize responsiveness, offline cache behavior, and update safety.
- Verify with real browsers and screenshots, not static inspection alone.
- Use virtualization, code splitting, Web Workers, and bounded rendering for large canvases, tables, and charts.
- Threat model frontend security: XSS, CSP, CSRF, token handling, OAuth redirects, untrusted datasets, unsafe HTML, and deserialization.
