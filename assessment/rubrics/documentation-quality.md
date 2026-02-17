# Assessment Rubric: Documentation Quality

> Used primarily with Problem 04 (Documentation as Survival Kit) and the handoff test in Problem 01.

---

## Scoring Scale

| Level | Label |
|-------|-------|
| 1 | **Benchmark** |
| 2 | **Developing** |
| 3 | **Proficient** |
| 4 | **Exemplary** |

---

## Criteria

### 1. README Completeness

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| Project name only; no setup instructions | Basic description and partial setup instructions | Complete setup, architecture overview, and contribution guidelines | Comprehensive: purpose, setup, architecture, contributing, troubleshooting, and project context |

### 2. AGENTS.md / AI Agent Readiness

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| No agent context file | Basic file with incomplete commands | Complete build/test/lint/deploy commands and code conventions | Full AGENTS.md with commands, conventions, domain vocabulary, file structure, and boundaries |

### 3. Architecture Decision Records

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| No ADRs | 1–2 ADRs describing what was built | 3+ ADRs explaining decisions with context and rationale | ADRs cover key decisions, alternatives considered, trade-offs acknowledged, and consequences tracked |

### 4. Inline Comments

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| No comments or comments that restate code | Comments present but explain *what* not *why* | Comments explain *why* at complex decision points | Strategic comments that illuminate intent; no noise; complex logic explained with business context |

### 5. Human Onboarding Success

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| Tester cannot get project running from docs | Tester gets project running with significant difficulty (>30 min) | Tester productive within 20 minutes; minor confusion points | Tester productive within 10 minutes; completes task without questions |

### 6. AI Agent Onboarding Success

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| AI tool cannot parse project from docs | AI tool understands basic structure; fails on specifics | AI tool can complete simple tasks using documentation context | AI tool productive immediately; documentation provides sufficient context for complex tasks |

---

## Scoring

**Total possible: 24 points** (6 criteria × 4 points)

| Score | Rating |
|-------|--------|
| 20–24 | Documentation enables true independence |
| 15–19 | Solid documentation with minor gaps |
| 10–14 | Documentation exists but insufficient for cold onboarding |
| 6–9 | Documentation is a liability, not an asset |
