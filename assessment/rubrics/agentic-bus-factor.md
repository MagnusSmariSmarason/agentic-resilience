# Assessment Rubric: Agentic Bus Factor

> Used across all problem modules. Evaluates how resilient the deliverable is against tool, provider, and knowledge concentration risks.

---

## Scoring Scale

| Level | Label | Description |
|-------|-------|-------------|
| 1 | **Benchmark** | Meets minimum expectations; significant resilience gaps |
| 2 | **Developing** | Shows awareness of portability; implementation incomplete |
| 3 | **Proficient** | Solid resilience practices; minor gaps remain |
| 4 | **Exemplary** | Resilient by design; serves as a model for others |

---

## Criteria

### 1. Documentation Portability

| 1 — Benchmark | 2 — Developing | 3 — Proficient | 4 — Exemplary |
|----------------|-----------------|-----------------|----------------|
| README exists but is tool-specific or incomplete | README works for humans; no AI agent context provided | Documentation serves both humans and at least one AI tool format | Includes AGENTS.md, README, and ADRs; portable across tools; enables cold onboarding for both humans and AI agents |

### 2. Dependency Resilience

| 1 — Benchmark | 2 — Developing | 3 — Proficient | 4 — Exemplary |
|----------------|-----------------|-----------------|----------------|
| Hard-coded to single provider or tool; no abstraction | Some abstraction present but significant lock-in points remain | Abstraction layers present; switching providers requires modest effort | Architecture explicitly designed for provider independence; fallback strategies documented and tested |

### 3. Knowledge Distribution

| 1 — Benchmark | 2 — Developing | 3 — Proficient | 4 — Exemplary |
|----------------|-----------------|-----------------|----------------|
| Only the author can maintain this code | One other person could maintain with effort and verbal guidance | Team documentation enables any current team member to maintain | Documentation and code quality enable a stranger (human or AI) to maintain without the author |

### 4. Security Practices

| 1 — Benchmark | 2 — Developing | 3 — Proficient | 4 — Exemplary |
|----------------|-----------------|-----------------|----------------|
| Credentials in code; no input validation; known vulnerabilities | Basic security measures; some gaps in coverage | OWASP Top 10 addressed; secrets managed properly; dependencies audited | Security-by-design; threat model documented; dependency audit automated; secrets rotation planned |

### 5. Context File Quality

| 1 — Benchmark | 2 — Developing | 3 — Proficient | 4 — Exemplary |
|----------------|-----------------|-----------------|----------------|
| No context files, or only tool-specific formats | Tool-specific context file exists (e.g., CLAUDE.md only) | Portable context file (AGENTS.md) present with basic project information | AGENTS.md with complete build commands, conventions, domain vocabulary, and boundaries; validated against multiple tools |

### 6. Recovery Readiness

| 1 — Benchmark | 2 — Developing | 3 — Proficient | 4 — Exemplary |
|----------------|-----------------|-----------------|----------------|
| No consideration of tool failure scenarios | Awareness of risk but no documented fallback plan | Fallback plan documented; alternative tools identified | Migration playbook exists; fallback tested; Recovery Time Objective defined and met |

---

## Scoring

**Total possible: 24 points** (6 criteria × 4 points each)

| Score | Rating | Interpretation |
|-------|--------|----------------|
| 20–24 | Resilient | This project survives tool and provider changes |
| 15–19 | Solid | Good practices with addressable gaps |
| 10–14 | Fragile | Significant dependencies that need attention |
| 6–9 | Critical | Agentic bus factor of 1 — one disruption from trouble |

---

## How to Use This Rubric

**Self-assessment**: Teams rate themselves at the start and end of a workshop. The gap reveals growth.

**Peer assessment**: Teams assess each other's deliverables, particularly during handoff tests. The receiving team is the best judge of knowledge distribution.

**Facilitator assessment**: Used for summative evaluation. Focus on the handoff test results as the strongest signal — did the documentation actually work?

**Organisational assessment**: Use the 8-dimension framework in [docs/AGENTIC-BUS-FACTOR.md](../../docs/AGENTIC-BUS-FACTOR.md) for broader evaluation beyond individual projects.
