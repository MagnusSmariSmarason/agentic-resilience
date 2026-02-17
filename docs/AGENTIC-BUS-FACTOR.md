# The Agentic Bus Factor

> *Bus factor: how many people need to get hit by a bus before a project is in trouble?*
> *Now apply that to your AI tooling.*

---

## The Concept

The traditional **bus factor** measures knowledge concentration risk in software teams — the minimum number of people who must be removed before a project stalls. Studies of 133 popular GitHub projects found that 65% have a bus factor of 2 or less, and 46% have a bus factor of exactly 1.

The **Agentic Bus Factor** extends this to AI tools, providers, and workflows:

> If Claude Code disappears tomorrow, can Cursor pick up your project? Can Codex, OpenCode, Antigravity? If the answer is no, your agentic bus factor is 1.

This isn't about model equivalence — these tools aren't interchangeable. The point is your project should be **portable**, even if your tool preference isn't.

## What Doesn't Count

Not five similar CLI tools — that's a bus factor of 1.5 wearing a trenchcoat. Same labs, same APIs, different login screens. That's not redundancy.

## What Does Count

Real agentic bus factor is measured in **layers of independence**:

### 1. Intelligence Providers
Can you switch between Anthropic, OpenAI, Google, DeepSeek, Mistral? Not just theoretically — have you tested it?

### 2. Local Capability
Your models, your hardware. A spare tyre, not a second engine — but a spare tyre gets you home.

### 3. Human Legibility
Can a developer onboard from your docs alone? No Slack messages, no "ask Sarah," no tribal knowledge.

### 4. Architectural Portability
Is your project structure tool-agnostic? Or is your institutional knowledge readable by one tool only?

## The Measurement Framework

| Dimension | What It Measures | Critical Threshold |
|-----------|------------------|--------------------|
| **Tool diversity** | Number of AI tools the team can effectively use | 1 = critical lock-in |
| **Context portability** | % of context files in tool-agnostic formats | <50% = high risk |
| **Provider independence** | Hours to switch LLM providers | >48h = fragile |
| **Documentation completeness** | Docs serve both humans AND AI agents | Missing either = gap |
| **Local fallback capability** | Can operate with local models if cloud unavailable | No = single point of failure |
| **Knowledge distribution** | Bus factor applied to AI tooling expertise | 1 = critical |
| **API abstraction level** | AI integrations behind abstraction layers | Direct API calls = locked in |
| **Recovery time objective** | Time to migrate to different AI coding tool | >1 week = unacceptable |

## The Current Landscape

We're watching tool-specific context files emerge:

- `CLAUDE.md` — Claude Code
- `.cursorrules` — Cursor
- `.windsurfrules` — Windsurf
- `AGENTS.md` — OpenAI Codex (now adopted by 60,000+ projects via Linux Foundation)

Not malicious — just how ecosystems form. But your institutional knowledge ends up readable by one tool only.

## The Strongest Resilience Layer

The simplest: **docs written for a smart colleague joining cold.**

Plain markdown. If a human can onboard from it, any capable model can too.

## The Goal

The goal isn't a magic number. It's a discipline: **no single tool, provider, or platform should be a fatal dependency.**

Pricing changes. APIs deprecate. Companies pivot. That's not an apocalypse scenario. That's just tech.

## Conscious Tradeoffs

Your own stack is also a dependency — there's no perfect resilience, only conscious tradeoffs. The difference is **choosing** your dependencies rather than inheriting them.

---

## Self-Assessment Checklist

Use this to evaluate your current agentic bus factor:

- [ ] Can a new team member get the project running from documentation alone?
- [ ] Can a different AI coding tool understand your project from your docs?
- [ ] Are your AI integrations behind an abstraction layer?
- [ ] Do you have a tested fallback if your primary LLM provider goes down?
- [ ] Is your project context stored in a portable format (not just tool-specific)?
- [ ] Have you actually tested switching tools, or just assumed you could?
- [ ] Do at least two people on the team understand the AI tooling setup?
- [ ] Can you run critical workflows with local models if needed?

**Score: Count your checkmarks.**
- 7–8: Resilient by design
- 5–6: Reasonable but with gaps
- 3–4: Fragile — one disruption away from trouble
- 0–2: Agentic bus factor of 1 — address this now

---

*Concept by Magnus Smári Smárason, 2026*
