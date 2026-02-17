# Agentic Resilience

**Problem-Based Learning with AI**

> *Part of the Sovereign AI: Governance & Systems Architecture programme*
> *University of Akureyri (UNAK), Iceland*

---

## The Idea

Everyone can use ChatGPT. That's the baseline. The question this programme asks is harder:

**Can you use AI to solve a problem you don't understand, catch its mistakes, and take responsibility for the result?**

Agentic Resilience is a set of problem-based learning exercises where students are dropped into realistic, messy scenarios with nothing but an AI assistant. There are no tutorials, no step-by-step instructions, no instructors walking them through it. The AI is the tutor. The student is the operator.

The exercises test judgment, not technical skill. A student who catches an AI hallucination and documents it scores higher than a student who submits a perfect deliverable they can't explain.

---

## The Problems

Each problem is self-contained: a scenario, a set of files, and a mission briefing. Students use AI for everything — and log every interaction.

| # | Problem | What happens | Duration |
|---|---------|-------------|----------|
| **00** | [**Hello World**](problems/00-hello-world/) | Set up a dev environment from scratch using AI. Fix a tiny broken website. Make your first git commit. | 2–4 hrs |
| **01** | [**The Developer Who Vanished**](problems/01-the-developer-who-vanished/) | A developer disappeared, leaving behind a broken, insecure Node.js application. Take it over. Find the vulnerabilities. Fix what matters. Document everything. | 6–10 hrs |

Problem 00 is the on-ramp. Problem 01 is the real thing.

Both are available in **English** and **Icelandic**.

> More problems are in development — covering research ethics, data science, event logistics, and AI governance.

---

## How It Works

### For students

1. Open the mission briefing for your assigned problem
2. Open your AI assistant (ChatGPT, Claude, Gemini — any free-tier tool works)
3. Follow the mission. Use AI for everything. Log every interaction.
4. Submit your work: a GitHub repository, a completed mission briefing with logs, and a retrospective

The mission briefings tell you everything you need to know. Start there.

### For instructors

Each problem folder contains:
- `PROBLEM-XX-MISSION-BRIEFING.md` — the student-facing assignment (self-contained)
- `README.md` — instructor reference with the full issue catalogue, what AI will miss, facilitation notes, and assessment guidance
- `is/` — Icelandic translation

Assessment rubrics and templates are in [`assessment/`](assessment/).

The methodology behind the exercises is documented in [`docs/`](docs/).

---

## What Makes This Different

**AI is required, not forbidden.** Students are expected to use AI for every step. The challenge is not "can you do it without AI" — it's "can you orchestrate AI through ambiguity and own the result."

**Process over product.** The AI Interaction Log is weighted more heavily than the final deliverable. A perfect report with no log demonstrates nothing. A messy report with an honest log of mistakes, corrections, and judgment calls demonstrates exactly the skills we're building.

**Messy is the point.** Every dataset is dirty, every scenario has contradictions, every file has surprises. Real work is messy. The ability to impose order on chaos — with AI help — is the skill.

**The AI will be wrong.** This is a certainty, not a possibility. Every problem contains issues that current AI tools consistently miss. Students must catch what the AI misses. When they do, they document it. When they don't, they document that too.

---

## Philosophy

These exercises are built on three principles from the [Agentic Resilience Manifesto](manifesto/MANIFESTO.md):

1. **Epistemic Independence** — AI is a sparring partner, never an oracle
2. **Portability** — Knowledge lives in open formats, not locked inside any tool
3. **Judgment over Eloquence** — Evidence and honest reasoning outweigh polished output

The theoretical foundations draw from Barrows' Problem-Based Learning, Kolb's Experiential Learning, Dewey's pragmatist philosophy, and research on the Einstellung effect. See [`docs/THEORETICAL-FOUNDATIONS.md`](docs/THEORETICAL-FOUNDATIONS.md) for the full framework.

---

## Quick Start

**Students:** Start with [Problem 00: Hello World](problems/00-hello-world/PROBLEM-00-MISSION-BRIEFING.md). Then move to [Problem 01](problems/01-the-developer-who-vanished/PROBLEM-01-MISSION-BRIEFING.md).

**Problem 01 codebase:** Students fork [MagnusSmariSmarason/skycrm](https://github.com/MagnusSmariSmarason/skycrm) — the deliberately broken application they must fix.

**Problem 00 starter:** Students use the [hello-world-starter](https://github.com/MagnusSmariSmarason/hello-world-starter) template to create their first repository.

---

## Repository Structure

```
agentic-resilience/
├── README.md                               You are here
├── problems/
│   ├── 00-hello-world/                     The on-ramp
│   │   ├── PROBLEM-00-MISSION-BRIEFING.md  Student briefing (EN)
│   │   ├── is/VERKEFNI-00-VERKEFNISLYSING.md  Student briefing (IS)
│   │   └── starter/                        Tiny broken web app
│   └── 01-the-developer-who-vanished/      The flagship problem
│       ├── PROBLEM-01-MISSION-BRIEFING.md  Student briefing (EN)
│       ├── is/VERKEFNI-01-VERKEFNISLYSING.md  Student briefing (IS)
│       └── skycrm/                         The broken codebase
├── docs/                                   Methodology and theory
├── assessment/                             Rubrics and templates
├── manifesto/                              The Agentic Resilience Manifesto
└── LICENSE                                 CC BY-SA 4.0
```

---

## Author

**Magnús Smári Smárason**
University of Akureyri, Iceland

## License

This work is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Code files (skycrm, starter) are MIT licensed.

You are free to share and adapt this material for any purpose, including commercial use, as long as you give appropriate credit and share under the same license.

---

*"When AI handles the doing, humans must own the deciding."*
