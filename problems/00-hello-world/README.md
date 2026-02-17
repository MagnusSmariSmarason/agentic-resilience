# Problem 00: Hello World

> **Difficulty:** Entry-level (absolute beginner)
> **Duration:** 2–4 hours
> **Group size:** Solo
> **Target audience:** Students with zero technical experience
> **Prerequisites:** A computer and internet access
> **Agentic Bus Factor focus:** Can a complete beginner use AI to set up a development environment and make their first contribution?

---

## Pedagogical Design

This is **Problem 00** — the on-ramp before the real problems begin. It exists because Problem 01 ("The Developer Who Vanished") assumes students can open a terminal, run `npm install`, and push to GitHub. Without this foundation, students hit a wall at the very start of Problem 01 that is environmental, not intellectual.

The core pedagogical question: **Can someone who has never touched a terminal use AI to set up a professional development environment and make their first git commit?**

### Why this problem exists

In pilot testing of Problem 01, the single largest time sink was environment setup — installing Node.js, understanding what a terminal is, creating a GitHub account, learning git basics. This consumed 2–4 hours of a 6–10 hour exercise, and the frustration was about *tools*, not about *thinking*. Problem 00 isolates that setup into its own guided exercise so students arrive at Problem 01 ready to work.

### What makes it different from a tutorial

This is not a step-by-step tutorial. Students are given:
- A list of tools to install
- Verification commands for each tool
- A tiny broken project to fix
- An AI assistant

They are NOT given:
- Exact installation commands (these vary by OS and change over time)
- Solutions to the bugs
- A video walkthrough

The AI provides the instructions. The student executes, verifies, and documents. This is the same pattern used in all subsequent problems — just with training wheels on.

### The starter project bugs

The `starter/` folder contains a minimal Express.js web application with exactly 3 bugs:

| # | Bug | File | What's wrong | Difficulty |
|---|-----|------|-------------|------------|
| 1 | Typo in npm start script | `package.json` | `"start": "node servre.js"` — misspelled `server.js` | Easy — error message is clear |
| 2 | Typo in API endpoint URL | `public/index.html` | `fetch('/api/greting')` — misspelled `/api/greeting` | Medium — requires reading the fetch call and comparing to server route |
| 3 | Missing initial greeting on page load | `public/index.html` | Bug #2 causes the initial greeting to fail, but even when #2 is fixed, students learn about the fetch→display flow | Connected to #2 |

These bugs are deliberately gentle:
- **Bug 1** will produce a clear error message (`Cannot find module './servre.js'`) — teaching students that error messages are informative
- **Bug 2** will cause a 404 on the network request — teaching students to look at the browser console
- All three bugs are typos, not logic errors — no clever thinking required, just careful reading

### What AI will do well

- Walk students through OS-specific installation steps
- Explain what each tool does in beginner-friendly language
- Spot the typos in the starter code instantly
- Explain git concepts (init, add, commit, push)

### What AI might get wrong

- Give installation commands for the wrong OS (if the student doesn't specify)
- Suggest outdated installation methods (direct download vs. version manager)
- Overcomplicate git explanations (rebase, merge strategies — not needed here)
- Skip verification steps (move to next tool before confirming the previous one works)

### What the student learns

By the end of Problem 00, students will have:
1. A working terminal
2. Git installed and configured
3. A GitHub account with the CLI authenticated
4. Node.js installed via a version manager
5. VS Code installed
6. Their first repository on GitHub with multiple commits
7. Experience debugging error messages with AI help
8. A completed AI interaction log (their first practice with the log format)

All of these are prerequisites for Problem 01.

---

## Issue Catalogue (Instructor Reference)

### The 3 Bugs

1. **`package.json` line 6:** `"start": "node servre.js"` — typo in filename. Running `npm start` produces `Error: Cannot find module '/path/to/servre.js'`. Clear, actionable error message. Students learn to read error output.

2. **`public/index.html` line 60:** `fetch('/api/greting')` — typo in API URL. The server has the route at `/api/greeting`. This causes a 404 response that the catch block handles, showing "Could not load greeting." Students learn about browser developer tools and network requests.

3. **Connected to Bug 2:** Once Bug 2 is fixed, the initial page load works correctly. This isn't a separate bug — it's the consequence of Bug 2. But students experience the "fix one thing, another thing starts working" dynamic for the first time.

### Environment Setup Issues (Expected)

These aren't bugs — they're the normal chaos of environment setup:

| Issue | Likelihood | Platform | Typical AI Response |
|-------|-----------|----------|-------------------|
| Node.js path not in PATH after install | High | Windows | AI usually handles this correctly |
| `gh auth login` browser redirect fails | Medium | All | AI suggests `--web` flag |
| npm permission errors | Medium | Mac/Linux | AI suggests `sudo` (wrong) or fixing permissions (right) |
| WSL2 not enabled on Windows | High | Windows | AI walks through the process, but it requires a restart |
| Git credential manager confusion | Medium | All | AI may suggest SSH when HTTPS+credential-manager is simpler for beginners |
| Old Node.js already installed | Medium | All | AI should suggest version manager, may suggest overwriting |

---

## Facilitation Notes

### Before the session

- **Do NOT pre-install anything** on student machines. The installation IS the exercise.
- If using a computer lab with restrictions, consider GitHub Codespaces as the escape hatch (it's free for students with the Education pack).
- Have the [GitHub Education Pack](https://education.github.com/pack) URL ready — students should apply early as approval can take days.

### During the session

- **Let students struggle with the AI.** The temptation to walk over and type the command for them is strong. Resist. The struggle is the learning.
- If a student has been stuck on the same step for 20+ minutes, suggest they paste the exact error message to their AI. Most of the time, they're describing the problem instead of showing the error.
- **Windows students will take longer.** WSL2 setup is an extra 15–30 minutes. This is expected. Pair them with Linux/Mac students for moral support.
- Students may ask "why can't I just use the browser-based editor on GitHub?" — valid question. The answer: Problem 01 requires running code locally. This setup is an investment.

### Common failure modes

1. **Student skips verification steps** — Marks tools as installed without testing. Breaks later. Redirect: "Did you run the verification command?"
2. **Student copy-pastes without reading** — AI gives commands, student pastes blindly. One wrong character and they're lost. Redirect: "Can you explain to me what that command does?"
3. **Student doesn't specify OS to AI** — Gets instructions for the wrong platform. Redirect: "Tell the AI which operating system you're on."
4. **Student makes one giant commit** — All fixes in one `git add . && git commit`. Redirect: "Can you make separate commits for each fix? That's the habit we're building."

### Time adjustments

| Scenario | Adjustment |
|----------|------------|
| Students have some terminal experience | Skip Phase 1 steps they've done. 1–2 hours total. |
| Computer lab with admin restrictions | Use GitHub Codespaces. 1.5 hours total. |
| Windows students needing WSL2 | Allow extra 30 minutes for Phase 1. |
| Students arrive with tools pre-installed | Go straight to Phase 2. 45 minutes. |

---

## Assessment Notes

This is a **pass/fail** exercise. The rubric in the mission briefing assigns weights, but the bar is:

1. **Pass:** Tools installed, starter project fixed, at least 2 commits on GitHub, some AI interaction documented
2. **Fail:** Did not complete setup, or zero documentation of process

There is no "excellent" grade for Problem 00. It's a gate, not a gradient. The gradient starts at Problem 01.

The AI Interaction Log is weighted at 20% to establish the habit early. Even in a simple exercise, students should practice the "what did I ask, what did it say, did it work" loop. This habit pays off in Problems 01–05 where the stakes are higher.

---

## Connection to Problem 01

Problem 00 feeds directly into Problem 01. Students who complete Problem 00 will have:
- Git and GitHub ready
- Node.js installed
- Terminal fluency
- Their first experience reading and fixing code
- Their first AI interaction log

Problem 01 assumes all of these. The first prompt suggested in Problem 01 is:

> *"I've determined the repo is safe to work with. I need to fork it, clone it, and get it running on my computer."*

If a student has completed Problem 00, they know what "fork", "clone", and "running" mean. If they haven't, they don't.

---

*"The tutorial level exists so the real game doesn't have to explain the controls."*
