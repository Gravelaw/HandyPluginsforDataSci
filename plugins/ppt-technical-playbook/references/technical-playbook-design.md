# Technical Playbook Design Reference

## Source Anchors

- Microsoft PowerPoint Help: https://support.microsoft.com/en-us/powerpoint
- Microsoft Create templates: https://create.microsoft.com/en-us/powerpoint-templates
- PowerPoint accessibility: https://support.microsoft.com/en-us/office/make-your-powerpoint-presentations-accessible-to-people-with-disabilities-6f7772b2-2f33-4bd2-8ca7-dae3b2b3ef25
- PowerPoint insert shapes, icons, charts, SmartArt, video: https://support.microsoft.com/en-us/office/quick-tips-add-and-format-in-powerpoint-4ce97df7-f8fa-454c-8441-2d3be0c54711
- Harvard slide checklist: https://hsph.harvard.edu/research/health-communication/resources/slide-checklist/
- Harvard Catalyst slides guidance: https://catalyst.harvard.edu/writing-communication-center/visualize-science/slides/
- Assertion-evidence approach: https://writing.engr.psu.edu/AE_Classroom_Teaching_Slides_Notes.pdf
- WCAG 2.2 contrast: https://www.w3.org/TR/WCAG22/

## Technical Deck Framework

- Selected frameworks: assertion-evidence for scientific/engineering slides, Gestalt grouping for visual hierarchy, WCAG accessibility for readable output, and appendix-heavy consulting/report grammar for traceable detail.
- Use assertion-evidence for core technical slides: sentence headline plus visual proof.
- Use playbook hierarchy: purpose, architecture, workflow, implementation steps, operations, failure modes, validation, appendix.
- Use appendix-heavy grammar for detail: page markers, readable tables, traceable references, source notes, and index slides.
- Keep one claim per slide. If a slide needs two claims, split it or make one an appendix detail.
- Prefer diagrams, sequence flows, state machines, system maps, code snippets, charts, tables, screenshots, and callouts over prose blocks.
- Give each technical artifact a caption: what it shows, what changed, why it matters.
- Apply Gestalt proximity, similarity, alignment, and continuity: related items sit together, repeated element types look alike, connectors clarify flow, and whitespace separates conceptual groups.

## Design System

- Theme: restrained professional palette with one accent for action, one for risk, one for evidence.
- Typography: readable sans serif; use monospace only for code, commands, IDs, and logs.
- Layout: stable grid, generous margins, predictable section/chapter rhythm.
- Charts: label directly, show units, avoid decorative 3D, include source and date.
- Icons: use as wayfinding or concept anchors, not decoration. Keep stroke style consistent.
- Smart graphics: use for process, hierarchy, lifecycle, and dependency maps when they reduce reading load.
- Video: use only for demos or process evidence; include poster frame, duration, and fallback explanation.

## QA Gates

- Every slide has a claim and proof object.
- Technical labels are accurate and survive thumbnail view.
- Diagrams are not decorative; each element has meaning.
- Tables are readable and appendix-bound when dense.
- Accessibility: alt text for important images, sufficient contrast, no color-only encoding.
