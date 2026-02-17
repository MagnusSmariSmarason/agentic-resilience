# AGENTS.md — Agentic Resilience Repository

> This repository practices what it preaches. This file enables any AI coding agent to understand, navigate, and contribute to this project.

## Project Overview

**Agentic Resilience** is a problem-based AI training methodology built around the Agentic Bus Factor principle. It contains documentation, workshop problem modules, assessment rubrics, facilitation guides, and tool-agnostic context examples.

This is a **documentation-heavy, content-driven repository**. There is no application to build or deploy. The "product" is the methodology itself — markdown documents, starter codebases for workshop exercises, and templates.

## Repository Structure

- `docs/` — Core methodology documents (theory, framework, measurement)
- `manifesto/` — The Agentic Resilience Manifesto
- `problems/` — Self-contained workshop problem modules, each with its own README
- `assessment/` — Rubrics and templates for evaluating workshop participants
- `facilitation/` — Guides, schedules, and scripts for workshop facilitators
- `context-examples/` — Examples of tool-specific and tool-agnostic context files

## Conventions

- All documentation is in **Markdown** (.md)
- File names use **UPPERCASE-KEBAB-CASE** for primary documents (e.g., `METHODOLOGY.md`)
- File names use **lowercase-kebab-case** for supporting files (e.g., `facilitator-notes.md`)
- Each problem module is a self-contained directory with its own `README.md`
- Assessment rubrics use Markdown tables with 4-level scales (Benchmark → Developing → Proficient → Exemplary)
- Cross-references between documents use relative links

## Key Concepts (Domain Vocabulary)

- **Agentic Bus Factor**: Extension of the traditional bus factor to AI tools and providers — measures how many tool/provider failures a project can survive
- **Einstellung Effect**: Cognitive bias where familiar solutions block discovery of better alternatives
- **PBL**: Problem-Based Learning — pedagogical approach where learning is driven by authentic problems
- **Deep Documentation**: Documentation designed to serve both humans and AI agents for onboarding
- **Epistemic Independence**: Ability to evaluate and explain AI-generated outputs rather than accepting them uncritically

## Content Guidelines

- Write for a smart colleague joining cold — no assumed context
- Ground claims in cited research where possible
- Problems should be tool-agnostic and adaptable to multiple tech stacks
- Assessment criteria should evaluate judgment and process, not just output
- All content should be portable — no proprietary formats or platform dependencies

## Quality Checks

- Every problem module must include: README, starter files, rubric, facilitator notes, adaptation guide
- Every rubric must use the 4-level scale consistently
- Cross-links between documents must resolve correctly
- No tool-specific assumptions in core methodology (tool-specific content goes in `context-examples/`)
