# Technical Playbook Design Reference

Keep this reference lean. Do not bulk-load external source pages because a source URL exists; browse only topic-specific sources needed for evidence, images, diagrams, or citations.

## Technical Deck Purpose

Technical playbooks help an intelligent person learn a subject, system, or implementation with enough detail to reason about it later. They are broader than training decks: cover mental model, architecture, mechanics, evidence, edge cases, operations, tradeoffs, and appendix detail.

Use assertion-evidence discipline: every slide has a sentence claim and a visual proof object. A slide without a proof object is a memo page, not a strong technical slide.

## Required Design Brief

Before creating slides, define:

- Domain: finance, metals, mining, software, healthcare, energy, education, public sector, etc.
- Theme: palette, typography, background texture or surface, icon style, chart style, diagram grammar, footer/source style.
- Proof object mix: diagrams, screenshots, source figures, research flow charts, charts, tables, code/logs, images.
- Asset plan: which assets are user-provided, official/open-source, generated, or recreated as editable diagrams.
- Citation plan: where source notes and image/figure attribution appear.

## Domain Theme Examples

- Software/platform: grid surfaces, code/terminal snippets, architecture layers, product screenshots, blue/green accent, crisp line icons.
- Finance: high-contrast tables/charts, KPI bridges, disclosure footers, restrained navy/green palette, market or portfolio visual motifs.
- Metals/mining: charcoal/copper/ore accents, terrain or process imagery, flow maps, material lifecycle diagrams, safety/risk markers.
- Healthcare/science: clean whites, clinical blues, protocol diagrams, pathway visuals, evidence/source markers.
- Energy/industrial: dark graphite, signal colors, asset maps, plant/process diagrams, reliability and risk iconography.

## Source Figures And Images

- Prefer user-provided, official, open-license, public-domain, or otherwise permitted figures.
- If a useful figure is copyrighted or unclear, recreate the concept as an original editable diagram and cite the source as conceptual inspiration.
- Use real screenshots, charts, maps, product UI, research flow charts, equipment/process images, or standards diagrams when they materially improve understanding.
- Record source, URL/path, date accessed, license/permission assumption, and slide placement.

## Diagram And Shape Quality

- Use grids and explicit anchor points. Arrows must connect to the center or intended edge of shapes.
- Keep connector style consistent within a diagram.
- Align sibling nodes; equalize gaps; avoid accidental diagonals.
- Directly label flows and boundaries. Do not force readers to infer meaning from color alone.
- Use icons as semantic labels, not confetti.

## QA Gates

- Every core slide has a claim and a proof object.
- The deck has a domain-specific visual system; it cannot look like a generic SaaS template.
- A deck longer than 8 slides has at least one strong visual asset class beyond generic boxes: sourced/recreated figures, screenshots, photos, charts, maps, or rich diagrams.
- Technical labels are accurate and survive thumbnail view.
- Tables are readable or moved to appendix.
- Important images/figures have attribution or citation notes.
- Accessibility: sufficient contrast, readable type, no color-only encoding, and alt/narration support for important visuals.
