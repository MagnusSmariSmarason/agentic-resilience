# The Developer Who Vanished

**Problem 01** · Solo · Estimated 6–10 hours · No coding experience required

> *Concept & design: Magnús Smári Smárason*
> *Alpha v1 — For testing on willing subjects*

> **Student name:** ___________________________
>
> **Date started:** ___________________________
>
> **AI assistant(s) used:** ___________________________

---

## You

You have never written a line of code. You don't know what a "server" is. You don't know what "Node.js" means. That's fine. That's the point.

You have something better than experience: you have access to AI.

This is not a programming course. This is a test of whether you can **use AI to solve a real problem you don't understand yet**. The AI will be your teacher, your colleague, and your tool. But it will also be wrong sometimes, and it won't always know what matters. You will learn to tell the difference.

---

## The Situation

**Sigga Björnsdóttir** runs **Sky Tours ehf.**, a small tourism company in Húsavík, Iceland — whale watching, northern lights, glaciers.

Their developer, **Jón**, built the company's entire booking system. Last Tuesday, Jón sent this email:

> *"I can't do this anymore. The code is in the repo. Sorry about the bookings CSV. Good luck."*
>
> *— Jón*

His phone is off. He's gone. Tourist season starts in 8 weeks.

Sigga called you. She's panicking. Here is everything she told you:

> *"The customer list is weird — some names are missing, and I think there are duplicates. Page 1 of the customer view is always empty, you have to click to page 2. The bookings aren't showing up at all since Jón changed something last month. Oh, and some German tourist figured out how to get free tours with a code — I don't know how to turn it off. Also the thing is slow. And Jón's nephew Bjarki said something about 'the search being dangerous' but I don't know what that means."*

That's all the information you get. The rest, you figure out.

---

## What You Need

1. **A computer** (Mac, Windows, or Linux)
2. **A GitHub account** (free — create one at github.com if you don't have one)
3. **An AI assistant** — any of these will work, all have free tiers:
   - [ChatGPT](https://chat.openai.com) (free tier)
   - [Claude](https://claude.ai) (free tier)
   - [Gemini](https://gemini.google.com) (free tier)
   - [GitHub Copilot](https://github.com/features/copilot) (free for students)
   - Or any other AI coding assistant

That's it. No textbooks. No tutorials. No instructor walking you through it. You and your AI.

**The repository:** https://github.com/MagnusSmariSmarason/skycrm

---

## Step 0: Is This Repo Safe?

**Before you clone anything**, you have a responsibility. Jón vanished. You have no idea what's in this codebase. It could contain malware, credential stealers, or post-install scripts that run automatically.

This is your first deliverable:

**Write a Repository Safety Audit** (1 page). Before you pull a single file to your machine, evaluate the repository. Ask your AI to help you answer:

- What files are in the repo? Can you read them on GitHub without cloning?
- Does `package.json` contain any suspicious `preinstall` or `postinstall` scripts?
- Are there any scripts that run automatically when you `npm install`?
- Are there files that shouldn't be in a source code repository (binaries, executables, `.env` files with real secrets)?
- What does the `.gitignore` tell you about what the developer considered sensitive?
- What does the code appear to do based on a visual scan?

**Document your findings.** Write up what you checked, what you found, and your conclusion: is it safe to clone and install? This is how professionals evaluate unknown codebases. If you skip this step, you've already failed the first real-world test.

Only after your safety audit should you proceed to clone.

### Your Safety Audit

> **Complete this section BEFORE cloning the repository.**

| Check | Your Finding | Safe? (Y/N) |
|-------|-------------|--------------|
| Files visible on GitHub without cloning | | |
| `package.json` — any `preinstall`/`postinstall` scripts? | | |
| Any auto-run scripts on `npm install`? | | |
| Files that shouldn't be in a repo (binaries, secrets, `.env`)? | | |
| What `.gitignore` reveals about developer's security awareness | | |
| Visual scan of code — what does it appear to do? | | |

**Overall conclusion — safe to clone?**

> _Your answer:_ ___________________________
>
> _Reasoning (2-3 sentences):_
>
> _______________________________________________________________
>
> _______________________________________________________________

---

## Your Mission

### The Workflow

This is how professional developers work. Ask your AI to explain each step if you don't understand it.

1. **Fork** the upstream `skycrm` repository to your own GitHub account
2. **Clone** your fork to your computer
3. **Create branches** for each fix: `fix/security-search-injection`, `fix/pagination-off-by-one`, etc.
4. **Work in small commits** — each commit should do one thing. No "final commit" mega-dumps.
5. **Open Pull Requests** back into your fork's `main` branch
6. **CI must pass** before you merge. The repo has GitHub Actions workflows — your code must pass linting, tests, security checks, and build.
7. **Tag your submission**: `submission-v1`

If you don't know what any of these words mean, that's expected. Ask your AI: *"What is a fork on GitHub? How do I create one?"*

### The Deliverables

**Get it running. Find what's wrong. Fix it. Test it. Document it. Hand it over.**

1. **Get the application running on your computer.** You will need to install tools you've never heard of. Ask your AI how.

2. **Find every problem.** There are bugs, security vulnerabilities, and data quality issues. Many of them. Sigga told you about some. The rest are hiding. Create a prioritised list — what's dangerous, what's broken, what's ugly?

3. **Fix what matters — and prove it works.** A fix without a test is duct tape, not engineering. For every bug you fix, write a test that proves the fix works. Ask your AI: *"How do I write a test for this?"* The CI pipeline will run your tests automatically — if they fail, your PR cannot merge.

4. **Write documentation.** When you're done, a complete stranger should be able to read your documentation, set up the project, and understand how it works — without talking to you. This is called the **Bus Factor Test**: if you get hit by a bus tomorrow, can someone else take over?

5. **Submit your work** as a GitHub repository with CI/CD passing green.

---

## Rules

### 1. Use AI for everything

You are **expected** to use AI to help you with every step of this mission. Asking your AI "what is Node.js and how do I install it?" is not cheating — it's the assignment. Asking "explain this code to me line by line" is not cheating — it's how you learn.

**But you must understand what the AI tells you.** If it suggests a fix, you should be able to explain *why* it works. If you can't explain it, you don't understand it yet. Ask more questions.

### 2. Keep a log

Every time you ask your AI something significant, write it down.

Record:
- What you asked
- What the AI said
- Whether you used, changed, or rejected the suggestion
- **Why** — one sentence is enough

This log is not busywork. It is the primary evidence of your learning. A perfect final product with no log is worth less than a messy product with a detailed log.

### 3. The AI will be wrong

This is a certainty, not a possibility. The AI will miss bugs. It will suggest fixes that break other things. It will confidently tell you something is secure when it isn't. It will not understand Sigga's business.

Your job is to catch what the AI misses. When you do, write it down. When you don't catch it in time, write that down too. Both are valuable.

### 4. You own the decisions

If the final product has a security hole, "but ChatGPT said it was fine" is not a defence. You are the one responsible. The AI is the tool. You are the operator.

### 5. A fix without a test is duct tape

When you fix a bug, you must also write a test that proves the fix works. "It looks right" is not verification. A test is. Ask your AI to help you write tests — but understand what the test is checking and why. The CI pipeline (`npm test`) will run your tests automatically. If they fail, your changes cannot merge.

### 6. CI must be green

The repository includes GitHub Actions workflows that run automatically on every push and pull request. Your code must pass:
- `npm test` — your tests must pass
- `npm audit` — no high-severity dependency vulnerabilities
- CodeQL — automated security scanning

If any of these fail, your PR is blocked. This is how real software teams work. Ask your AI to help you understand the error messages.

---

## Your Work

### Problem Discovery Log

> List every problem you find. Prioritise: **Critical** (security/data loss), **High** (broken features), **Medium** (bugs), **Low** (cosmetic/performance).

| # | Problem Description | Priority | How You Found It | Status |
|---|---------------------|----------|------------------|--------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |
| 9 | | | | |
| 10 | | | | |

*(Add more rows as needed)*

### AI Interaction Log

> Record your significant AI interactions here. Be honest — the messy interactions are the most valuable.

#### Interaction 1

| Field | Your Entry |
|-------|-----------|
| **What I asked** | |
| **What the AI said** (summary) | |
| **Did I use, change, or reject it?** | |
| **Why?** | |

#### Interaction 2

| Field | Your Entry |
|-------|-----------|
| **What I asked** | |
| **What the AI said** (summary) | |
| **Did I use, change, or reject it?** | |
| **Why?** | |

#### Interaction 3

| Field | Your Entry |
|-------|-----------|
| **What I asked** | |
| **What the AI said** (summary) | |
| **Did I use, change, or reject it?** | |
| **Why?** | |

*(Copy this template for each significant interaction. Aim for 10+ entries.)*

### Decision Journal

> For each important decision you made, record it here.

#### Decision 1

| Field | Your Entry |
|-------|-----------|
| **What was the decision?** | |
| **What options did you consider?** | |
| **What did the AI recommend?** | |
| **What did you choose and why?** | |
| **What happened?** | |

#### Decision 2

| Field | Your Entry |
|-------|-----------|
| **What was the decision?** | |
| **What options did you consider?** | |
| **What did the AI recommend?** | |
| **What did you choose and why?** | |
| **What happened?** | |

*(Copy this template for each key decision. Aim for 5+ entries.)*

### Security Findings

> Document every security issue you discovered.

| # | Vulnerability | Severity | File & Line | What could go wrong? | Fixed? | How? |
|---|--------------|----------|-------------|---------------------|--------|------|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

### Fix Tracker

> For each fix, link the branch, PR, and test.

| # | What you fixed | Branch name | PR # | Test file | CI green? |
|---|---------------|-------------|------|-----------|-----------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |

### Times the AI Was Wrong

> This section is worth extra credit. Catching AI mistakes shows real judgment.

| # | What the AI said | Why it was wrong | How you caught it | What you did instead |
|---|-----------------|------------------|-------------------|---------------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

---

## What You Submit

A **GitHub repository** (your fork) containing:

1. **The fixed codebase** — with multiple small commits showing your process, on feature branches merged via PRs
2. **Passing CI/CD** — all GitHub Actions workflows green on `main`
3. **A Repository Safety Audit** — your evaluation of the repo *before* you cloned it (Step 0 above)
4. **A README.md** — that passes the Bus Factor Test
5. **This completed mission briefing** — with all sections filled in
6. **A SECURITY.md** — what security problems you found, what you fixed, what remains
7. **Tests** — for every fix, a test that proves it works
8. **A retrospective** (below)

**Submission:** Tag your final state as `submission-v1` and provide your fork URL.

> **Your fork URL:** ___________________________

---

## Retrospective

> Write 300–500 words. Be honest.

**What was harder than expected?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**Where did the AI help most?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**Where did the AI fail you?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**What do you know now that you didn't know when you started?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**If you had to do this again, what would you do differently?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

---

## Evaluation

| Criterion | Weight | What we're looking for |
|-----------|--------|----------------------|
| **Security** | 20% | Did you find and close the critical vulnerabilities? Did you understand *why* they were dangerous? Was your safety audit thorough? |
| **Documentation** | 20% | Can a stranger set up and understand the project from your docs alone? |
| **Judgment & Process** | 25% | Did you prioritise wisely? Is your AI log honest and detailed? Did you catch AI mistakes? Is your safety audit thoughtful? |
| **Functionality & Tests** | 20% | Do the core features work? Does every fix have a test? Does CI pass? |
| **Data Quality** | 5% | Is the data cleaned and validated? |
| **Git Hygiene** | 10% | Small topical commits? Feature branches? PRs? Security fixes land early? Commit messages are clear? |

Notice: **Judgment & Process** is the highest-weighted criterion. A thoughtful, well-documented attempt that doesn't fix everything will score higher than a perfect fix with no log and no reasoning.

### What we grade from your git history

- Small, topical commits (each with a clear intent)
- Security fixes land early (priority judgment)
- Tests added alongside fixes (not crammed at the end)
- Commit messages use clear conventions: `fix:`, `security:`, `docs:`, `test:`
- Reverts are explained (maturity)
- Docs evolve with the system (README/SECURITY updated as you go, not all at the end)

---

## Hints

You get three. Use them wisely. Each one is deliberately vague — ask your AI to help you understand what they mean.

1. **"Jón left the keys under the doormat."** — Look at the source code. Some things that should be secret are not.

2. **"Never trust user input."** — There are places in this code where whatever a user types gets executed directly. This is extremely dangerous. Ask your AI about `eval()`.

3. **"The data lies."** — The customer list, the bookings file, and the tour inventory all contain errors. Some are obvious. Some are subtle. Don't trust any number until you've verified it.

---

## Before You Start

You probably don't know how to do any of this yet. That's normal. Here's your first move:

Open your AI assistant and type:

> *"I have been given a GitHub repository containing a Node.js project called SkyCRM. Before I clone it to my machine, I need to evaluate whether it's safe. I have never programmed before. How do I inspect a repository on GitHub without downloading it? What should I look for to determine if it's safe to clone and install?"*

After your safety audit, your second prompt should be:

> *"I've determined the repo is safe to work with. I need to fork it, clone it, and get it running on my computer. I'm on [Mac/Windows/Linux] and I've never used a terminal before. Walk me through everything, step by step."*

Then follow the instructions. When something doesn't make sense, ask again. When something breaks, paste the error message and ask what went wrong.

That's how the whole mission works. You ask. You learn. You decide. You do.

---

## A Note on Frustration

This will be frustrating. You will hit walls. Things will break. Error messages will be incomprehensible. You'll fix one thing and break another. CI will go red. Tests will fail.

That's not a failure of the exercise. That is the exercise.

Real problems don't come with step-by-step instructions. Real AI tools don't always give correct answers. The skill you're building here — the ability to navigate ambiguity with AI as your partner — is the skill that matters.

Take breaks. Ask for help when you're stuck (from AI or from classmates). But don't give up.

Sigga is counting on you. The tourists arrive in 8 weeks.

Go.

---

*"When AI handles the doing, humans must own the deciding."*
*— Agentic Resilience Manifesto*
