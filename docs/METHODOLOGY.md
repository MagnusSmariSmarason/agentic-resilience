# Problem-Based AI Training: Complete Methodology

> This is the core methodology document for the Agentic Resilience framework. It provides the full theoretical foundation, design framework, assessment strategy, and implementation guidance.

---

## Document Map

This methodology is structured in six parts:

| Part | Title | What It Covers |
|------|-------|---------------|
| I | Theoretical Foundations | PBL research, Kolb, Dewey, Vygotsky, Einstellung effect, Agentic Bus Factor |
| II | Workshop Design Framework | Backwards design, scaffolding, ill-structured problem design, modular architecture |
| III | Assessment Strategy | Five-layer assessment, rubrics, AI-augmented work evaluation, peer assessment |
| IV | Problem Modules | Four concrete workshop problems with full implementation details |
| V | Facilitation Guide | Five principles, common situations, Einstellung debriefing |
| VI | Integration | Sample three-day schedule, competency framework alignment |

For the full content of each part, see the linked documents below. This file provides the executive summary and connects the pieces.

---

## Part I: Theoretical Foundations

**Full document**: [THEORETICAL-FOUNDATIONS.md](THEORETICAL-FOUNDATIONS.md)

Problem-based learning (PBL) outperforms traditional instruction in technical education, with meta-analyses showing effect sizes of d+ = 0.652 for academic achievement and 1.081 for critical thinking. The methodology integrates three theoretical pillars: Kolb's Experiential Learning Cycle (all four stages are non-negotiable in every session), Dewey's pragmatist philosophy (knowledge through inquiry), and Vygotsky's Zone of Proximal Development (scaffolding fades based on demonstrated competence, not fixed schedules).

The **Einstellung effect** — the tendency to apply familiar solutions when better alternatives exist — is the primary cognitive barrier targeted. Research shows it reduces expert problem-solving ability by up to three standard deviations. Every problem module is designed to trigger, surface, and break these fixation patterns.

The **Agentic Bus Factor** extends the traditional software engineering bus factor to AI tools and providers. It operates as a design principle throughout: problems embed dependency resilience, rubrics evaluate portability, and participants learn to recognise tool lock-in.

**Full concept document**: [AGENTIC-BUS-FACTOR.md](AGENTIC-BUS-FACTOR.md)

---

## Part II: Workshop Design Framework

Every workshop uses **Understanding by Design** (Wiggins & McTighe) as its curriculum architecture:

**Stage 1 — Desired Results**: Transfer goals (what participants do independently in novel contexts), enduring understandings (big ideas that persist), and essential questions (open-ended, recurring).

**Stage 2 — Assessment Evidence**: Detailed in Part III.

**Stage 3 — Learning Plan**: Each session follows Kolb's full cycle, coded using UbD's Transfer/Meaning-making/Acquisition framework.

**Scaffolding varies by audience** while problems remain the same:
- Undergraduates: conceptual and strategic scaffolding
- Postgraduates: strategic and metacognitive scaffolding
- Working professionals: process scaffolding with workplace bridges
- Educators: metacognitive scaffolding focused on pedagogical transfer

**Mixed groups** use tiered challenge design (Core → Extension → Expert) where all tiers are substantive.

All problems operate at **Jonassen's types 6–11** (troubleshooting through dilemmas): multiple valid solutions, incomplete information, competing stakeholder perspectives, and uncertainty about which principles apply.

---

## Part III: Assessment Strategy

**Full rubrics**: See [assessment/rubrics/](../assessment/rubrics/)
**Templates**: See [assessment/templates/](../assessment/templates/)

Five assessment layers:

1. **Competency baseline** (pre-workshop): SFIA 9 mapping via diagnostic task
2. **Process assessment** (during): AI interaction logs, decision justification journals, facilitator observation
3. **Product assessment** (end): Stegeman code quality rubric + Agentic Bus Factor rubric
4. **AI-augmented work** (throughout): Prompt quality, output critique, oral defence, reflection portfolio
5. **Peer and self-assessment** (formative + summative): Calibrated, structured, growth-oriented

The philosophy: **assess judgment, not output.** In an era where AI produces correct answers in seconds, assessment targets what humans contribute — decision-making, process quality, and resilience thinking.

---

## Part IV: Problem Modules

**Full problem descriptions**: See [problems/](../problems/)

| Module | Name | Focus | Duration |
|--------|------|-------|----------|
| 01 | [The Developer Who Vanished](../problems/01-the-developer-who-vanished/) | Knowledge resilience, documentation, handoff | 4–6 hours |
| 02 | [The Tool That Disappeared](../problems/02-the-tool-that-disappeared/) | Tool migration, context portability | 3–4 hours |
| 03 | [Solve It Without Your Hammer](../problems/03-solve-it-without-your-hammer/) | Einstellung-breaking constraints | 30–45 min each |
| 04 | [Documentation as Survival Kit](../problems/04-documentation-as-survival-kit/) | Human + AI agent onboarding | 2–3 hours |

Each module is self-contained with scenario, tiered challenges, Einstellung targeting, assessment criteria, facilitator notes, and adaptation guides.

---

## Part V: Facilitation

**Full guide**: See [facilitation/guides/core-principles.md](../facilitation/guides/core-principles.md)
**Schedules**: See [facilitation/schedules/](../facilitation/schedules/)

Five facilitation principles:
1. Task-centred, not topic-centred
2. Productive failure before instruction
3. Metacognitive prompting at every transition
4. AI as collaborative tool, not oracle
5. The handoff test as the ultimate assessment

---

## Part VI: Integration and Alignment

**Sample schedule**: See [facilitation/schedules/three-day-intensive.md](../facilitation/schedules/three-day-intensive.md)

Workshop outcomes align with:
- **UNESCO AI Competency Framework for Students** (2024)
- **SFIA 9** — particularly Machine Learning, Software Engineering, and Security
- **AAC&U VALUE rubrics** (used by 2,000+ institutions)
- **AI Assessment Scale (AIAS)** — Levels 4–5 (AI Collaboration and Exploration)

---

## Core vs. Customisable Elements

| Element | Status | Notes |
|---------|--------|-------|
| Theoretical foundations | **CORE** | Preserve — defines the methodology's identity |
| Agentic Bus Factor principle | **CORE** | Must be woven throughout, not bolted on |
| Assessment philosophy (judgment over output) | **CORE** | Non-negotiable |
| Five facilitation principles | **CORE** | These define the facilitator's role |
| Problem modules | **ADAPT** | Swap technology, domain, difficulty as needed |
| Specific tech stacks | **ADAPT** | Problems work in any language/framework |
| Timing and scheduling | **ADAPT** | Fit to your context |
| Scaffolding intensity | **ADAPT** | Calibrate to your audience |
| Delivery format (in-person/remote) | **ADAPT** | All modules work in both formats |

---

*Methodology developed by Magnus Smári Smárason, 2026*
*Veritas in Praxi*
