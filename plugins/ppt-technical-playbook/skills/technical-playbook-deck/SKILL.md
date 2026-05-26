---
name: technical-playbook-deck
description: Create or redesign detailed technical PowerPoint playbooks, engineering deep dives, architecture manuals, implementation guides, system reviews, appendix-heavy analysis decks, and long-form technical narratives.
---

# Technical Playbook Deck

Use this skill for detailed technical PowerPoint decks where the audience must understand systems, evidence, implementation, operations, and tradeoffs.

Read `../../references/technical-playbook-design.md` for substantial work. Read `../../references/powerpoint-production-handoff.md` before creating a PPTX.

## Workflow

1. Define audience and use mode: live walkthrough, self-read playbook, review gate, handoff manual, or technical appendix.
2. Build a claim spine with sentence headlines. Each slide needs one claim.
3. Choose proof objects: architecture diagram, workflow, state machine, table, chart, code snippet, screenshot, log, benchmark, or validation matrix.
4. Design chapters: context, system model, method, implementation, verification, operations, risks, decisions, appendix.
5. Lock a technical theme: readable grid, restrained palette, consistent icon stroke, direct labels, source footers, and code styling.
6. Create dense material only when it belongs in a reference appendix; keep live-talk slides cleaner.
7. If producing `.pptx`, invoke the `Presentations` skill once after this strategy is set.

## Required Slide Components

- Title or section marker with technical scope.
- Assertion headline.
- Visual evidence area.
- Callouts for risk, decision, or implication.
- Footer/source when evidence is external.
- Appendix page markers for deep details.

## Reject

- Decorative diagrams that do not encode information.
- Unlabeled charts, screenshots, or architecture boxes.
- More than one primary claim per slide.
- Tables too small to read.
- Color-only status encoding.
