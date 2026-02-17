# Assessment Rubric: Product Quality

> Adapted from the Stegeman Code Quality Rubric (University of Amsterdam) with additions for AI-augmented work. Used primarily with Problem 01 (The Developer Who Vanished).

---

## Scoring Scale

| Level | Label | Description |
|-------|-------|-------------|
| 1 | **Benchmark** | Meets minimum expectations; significant quality issues |
| 2 | **Developing** | Shows awareness of quality standards; inconsistent application |
| 3 | **Proficient** | Consistent quality; minor issues remain |
| 4 | **Exemplary** | Professional-grade; serves as a model |

---

## Code Quality Criteria (Adapted from Stegeman)

### Documentation

| Criterion | 1 | 2 | 3 | 4 |
|-----------|---|---|---|---|
| **Names** | Variables and functions named obscurely (`x`, `temp`, `doStuff`) | Some meaningful names; inconsistent conventions | Meaningful names throughout; consistent convention | Names reveal intent; domain vocabulary used; self-documenting at the naming level |
| **Comments** | No comments, or comments that restate the code | Comments exist but explain *what* not *why* | Comments explain *why* decisions were made; misleading comments removed | Strategic comments on complex logic; ADRs for architectural choices; clean of noise |

### Presentation

| Criterion | 1 | 2 | 3 | 4 |
|-----------|---|---|---|---|
| **Layout** | Inconsistent indentation; no visual structure | Mostly consistent; some formatting issues | Consistent style throughout; logical grouping | Formatter-enforced consistency; visual hierarchy aids comprehension |
| **Formatting** | Dead code, TODOs, debug statements left in | Some cleanup done; occasional artifacts remain | Clean of dead code; no debug artifacts; TODOs tracked in issues | Production-clean; linting enforced; no unnecessary artifacts |

### Algorithms

| Criterion | 1 | 2 | 3 | 4 |
|-----------|---|---|---|---|
| **Flow** | Convoluted control flow; deeply nested conditionals | Mostly readable; some unnecessary complexity | Clear control flow; early returns; guard clauses used | Elegant flow; complex logic decomposed into readable steps |
| **Expressions** | Overly complex expressions; magic numbers | Some simplification; magic numbers partially addressed | Expressions readable; constants named; no magic numbers | Expressions optimised for clarity; intent obvious at a glance |

### Structure

| Criterion | 1 | 2 | 3 | 4 |
|-----------|---|---|---|---|
| **Decomposition** | Monolithic functions (100+ lines); no separation | Some decomposition; functions still too large | Functions have single responsibility; reasonable size | Clean decomposition; each function does one thing well |
| **Modularisation** | Everything in one file; circular dependencies | Some file separation; unclear module boundaries | Clear module boundaries; separation of concerns | Architecture supports independent development and testing of modules |
| **Idiom** | Anti-patterns; language features misused | Basic patterns; some language-inappropriate approaches | Language-appropriate patterns; standard idioms used | Idiomatic code; leverages language strengths; follows community conventions |

---

## AI-Augmented Work Criteria

### AI Interaction Quality

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| AI used as a code generator with no critical evaluation | AI output reviewed but accepted with minimal modification | AI output critically evaluated; modifications documented with reasoning | AI used strategically; interaction log shows iterative refinement and deliberate judgment |

### Audit Trail

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| No record of AI usage | AI tools mentioned but interactions not documented | Key AI interactions logged with decisions noted | Complete audit trail: prompts, outputs, accepted/rejected/modified decisions with reasoning |

### Explainability

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| Cannot explain AI-generated code when asked | Can explain what the code does but not why this approach | Can explain both the code and the approach; identifies alternatives | Can explain the code, justify the approach, critique it, and propose improvements |

---

## Scoring

**Code quality: 36 points** (9 criteria × 4 points)
**AI-augmented work: 12 points** (3 criteria × 4 points)
**Total possible: 48 points**

| Score | Rating |
|-------|--------|
| 40–48 | Exemplary |
| 30–39 | Proficient |
| 20–29 | Developing |
| 12–19 | Benchmark |
