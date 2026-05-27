---
name: technical-playbook-deck
description: Create or redesign detailed technical PowerPoint playbooks, engineering deep dives, architecture manuals, implementation guides, system reviews, appendix-heavy analysis decks, and long-form technical narratives. Use when an intelligent reader must learn the subject, system, evidence, edge cases, and implementation tradeoffs from the deck.
---

# Technical Playbook Deck

Use this skill for detailed technical decks that teach a subject broadly enough to make a smart reader operationally competent. Technical is not "training": it covers the system, concepts, minute details, evidence, implementation, risks, and references; training narrows onto one or a few concepts and drills them deeply.

Read `../../references/technical-playbook-design.md` for substantial work. Read `../../references/powerpoint-production-handoff.md` before creating a PPTX.

## Workflow

1. Define audience, use mode, domain, and expected depth: live walkthrough, self-read playbook, review gate, handoff manual, or technical appendix.
2. Build a claim spine with one sentence headline per slide.
3. Lock a domain visual system before slide creation: palette, typography, icon family, diagram grammar, image style, source/footer pattern, and chapter rhythm.
4. Choose proof objects for every content slide: architecture diagram, workflow, state machine, table, chart, code snippet, screenshot, benchmark, source figure, research diagram, or validation matrix.
5. If the topic has known source figures, screenshots, standards diagrams, research visuals, or field images, use verified/open/user-provided assets directly when allowed; otherwise recreate the concept as an original editable diagram and cite the source.
6. Design chapters: context, concept model, system architecture, workflow, implementation, verification, operations, failure modes, decisions, appendix.
7. If producing `.pptx`, invoke the `Presentations` skill once after this strategy is set.

## Blocking Gates

- No bland text-and-shape-only decks: decks over 8 slides need a visible domain theme plus images/screenshots/source figures or rich editable diagrams.
- No generic theme: finance, mining, metals, software, healthcare, energy, education, and other domains must look materially different.
- No decorative diagrams: every node, arrow, icon, and callout must encode information.
- No misaligned arrows/connectors: use centered connectors, consistent spacing, and rendered QA.
- No unsourced external figures: record source, license/permission assumption, and citation.
