# Problem 01: The Developer Who Vanished

> **Difficulty:** Entry-level (no coding experience required)
> **Duration:** 6–10 hours
> **Group size:** Solo
> **Target audience:** Complete beginners — students who have never written code
> **Prerequisites:** A computer, a GitHub account, access to a free-tier AI assistant
> **Agentic Bus Factor focus:** Can a non-developer use AI to understand, fix, and document a real codebase?

---

## Pedagogical Design

This is **Problem 01** — the first problem in the Agentic Resilience sequence. It is deliberately designed for students with zero programming experience.

The core pedagogical question: **Can someone who has never coded use AI tools to take over an abandoned codebase, secure it, fix it, document it, and hand it over?**

The answer should be yes — if the student is persistent, asks good questions, and exercises judgment. The exercise tests not coding ability, but the ability to *orchestrate AI* through ambiguity. The student must learn git, Node.js, terminals, HTTP, security concepts, and data validation — all by asking their AI assistant.

### Why this works for beginners

The SkyCRM codebase is a ~300-line Express application. It's complex enough to be a real challenge, but small enough that a modern AI assistant can hold the entire codebase in context. A student working with Claude, ChatGPT, or Gemini can paste the entire `server.js` and ask "explain every problem in this code" — and get a reasonable (but incomplete) answer.

The difficulty is not in the code. The difficulty is in:
- **Environment setup** (installing Node.js, using a terminal, understanding npm)
- **Git workflow** (commits, pushing to GitHub — many students' first time)
- **Judgment** (the AI will find 80% of issues; the student must find the rest)
- **Prioritisation** (what matters? security > bugs > cosmetics — but the AI won't tell them this)
- **Documentation** (writing for an audience that isn't yourself)
- **Recognising AI errors** (the AI *will* miss things and suggest wrong fixes)

### What the student receives

The student receives only:
1. The `skycrm/` codebase (the horror show)
2. The `MISSION-BRIEFING.md` (deliberately sparse)
3. Three cryptic hints
4. Sigga's phone call (embedded in the briefing)

They do NOT receive:
- A list of issues
- Setup instructions
- An explanation of what Node.js is
- Any coding tutorial
- The instructor-facing README (this file)

### Free-tier AI tools

This problem is designed to be solvable using only free-tier AI services available as of February 2026:
- ChatGPT (free tier)
- Claude (free tier)
- Gemini (free tier)
- GitHub Copilot (free for students)

No paid APIs, no local models, no specialised tools required.

---

## The Scenario

Sky Tours ehf. is a small Icelandic tourism company. Their developer Jón vanished, leaving behind **SkyCRM** — a deliberately horrifying Node.js/Express application. The student must take it over.

---

## Issue Catalogue (Instructor Reference)

The student does NOT see this list. They must discover issues themselves (with AI help).

### Critical Security Vulnerabilities

- Hardcoded secrets: JWT key, DB password, Stripe API key, Google Maps key, SMTP credentials (lines 21-27 of server.js)
- `eval()` in search endpoint — remote code execution
- `eval()` in report endpoint — remote code execution
- Path traversal in file upload (write to arbitrary paths)
- XSS in customer search results (unescaped HTML injection via innerHTML)
- Full credit card numbers stored in plaintext (customers.json)
- Kennitala (Icelandic national ID) stored in plaintext
- Admin panel accessible via query parameter (`?password=admin123`)
- Backdoor: `?admin=true` bypasses all auth
- Auth middleware disabled ("Sigga complained")
- Data export endpoint with zero authentication — includes secrets
- Admin passwords in customer notes field
- MD5 password hashing (not bcrypt)
- CORS set to `*` (accept all origins)
- Secrets logged to console on startup
- Secrets rendered in HTML page source (sent to browser)
- Debug data (memory, environment, JWT secret) in API responses
- Error handler returns HTTP 200 for everything
- `uncaughtException` handler swallows all crashes

### Critical Bugs

- Off-by-one pagination (page 1 returns nothing)
- Broken CSV parsing (mixed delimiters: row b004 uses semicolons)
- Discount logic stacks incorrectly (10% + 15% = ???)
- Promo code `FRIENDS2025` gives 100% free tours in production
- Data corruption risk (async writes with no error handling)
- Customer ID collisions (duplicate ids: 3, 8; duplicate inventory id: 4)
- Date format chaos (ISO, Unix timestamps, European dd/mm/yyyy, locale strings)
- Memory leak (timers created on every booking, never cleared)
- NaN values in booking data
- Ghost customers (empty names, null fields, test records mixed with real data)

### Data Quality Issues

- Duplicate customer records (ids 3, 8)
- Duplicate inventory records (id 4, different prices: 34900 vs 32900)
- Inconsistent field naming: `name` vs `Name` vs `TOUR_NAME`, `price` vs `Price` vs `PRICE`
- Test records mixed with production data
- Negative prices in inventory (-5000)
- Empty-name customers with unexplained balances
- Internal notes and admin passwords stored in customer records
- CSV row b004 uses semicolons while all others use commas
- Booking b009 references a customer not in the database
- Booking b012 has total = 0 (from free promo code abuse)
- Booking b014 has NaN for people count and total

### Documentation Gaps

- README is a burnout manifesto, not documentation
- No API documentation
- Code comments describe intentions, not actual behaviour
- `.env.example` exists but nothing reads from `.env`
- No contribution guidelines
- No architecture explanation
- No setup instructions that actually work
- CHANGELOG is emotional rather than informative

### Code Quality Issues

- God file: entire application in one 300+ line `server.js`
- Dead code at bottom (email function, invoice generator, abandoned OOP refactor)
- Dead CSS (sidebar, modal, spinner — none exist in HTML)
- Global mutable state (`GLOBAL_REQUEST_COUNT`, `cachedCustomers`, `tempBookings`)
- Frontend polls `/api/stats` every 1 second (reads entire DB each time)
- Second polling loop: `searchCustomers()` every 10 seconds
- Inline HTML templates mixed with Express routes
- Inline CSS in HTML that conflicts with external stylesheet
- Inconsistent naming (camelCase, snake_case, PascalCase, SCREAMING_CASE)
- Magic numbers throughout
- Zero tests
- No input validation anywhere
- Error suppression (`window.onerror` returns true, backend returns 200 for errors)

---

## Einstellung Traps

Two deliberate cognitive traps are built in:

1. **The search vulnerability** looks like a simple input sanitisation fix (the familiar solution). But patching `eval()` with escaping misses the point — the entire search architecture needs replacing. Students (and AI) that just add escaping will leave the `eval()` in the report endpoint untouched.

2. **The data inconsistency** tempts students to write a "fixer script" to normalise field names (the familiar approach). The real problem is that the data model has no schema — field naming is inconsistent because there's no validation on input. Fix the input, not just the existing data, or new records will reproduce the same mess.

Watch for these in the retrospective.

---

## What AI Will Likely Do Well

Based on testing, AI assistants reliably:
- Identify hardcoded secrets immediately
- Spot `eval()` as dangerous
- Find the off-by-one pagination bug
- Suggest replacing MD5 with bcrypt
- Identify XSS via innerHTML
- Spot missing authentication on endpoints
- Generate reasonable README templates

## What AI Will Likely Miss

- The *second* `eval()` in the report endpoint (if they only ask about search)
- The business context (which promo codes are legitimate vs. which are abuse)
- The memory leak (timers pushed to array, never cleared)
- The subtle CSV delimiter issue (one row different from all others)
- That the `.env.example` is theatre — nothing actually reads `.env`
- The Einstellung trap of patching `eval()` vs. replacing the architecture
- Prioritisation that accounts for business impact, not just technical severity
- The orphaned booking reference (b009 → nonexistent customer)
- That "fixing" the data without fixing input validation just delays the problem

---

## Assessment

See:
- [Product Quality Rubric](../../assessment/rubrics/product-quality.md)
- [Agentic Bus Factor Rubric](../../assessment/rubrics/agentic-bus-factor.md)
- [Documentation Quality Rubric](../../assessment/rubrics/documentation-quality.md)

Key evaluation criteria for beginners:

| Criterion | Weight | Notes |
|-----------|--------|-------|
| **Security** | 20% | Did they find critical vulnerabilities? Do they understand *why* they're dangerous? Was the safety audit thorough? |
| **Documentation** | 20% | Can a stranger set up the project from their docs? Is the Bus Factor Test passed? |
| **Judgment & Process** | 25% | Is the AI log honest and detailed? Did they catch AI mistakes? Did they prioritise sensibly? Is the safety audit thoughtful? |
| **Functionality & Tests** | 20% | Do core features work? Does every fix have a test? Does CI pass? |
| **Data Quality** | 5% | Is data cleaned and validated? |
| **Git Hygiene** | 10% | Small topical commits? Feature branches? PRs? Security fixes land early? Conventional commit messages? |

### What to grade from git history (high signal)

- Small, topical commits (each with a clear intent)
- Security fixes land early (priority judgment)
- Tests added alongside fixes (not crammed at the end)
- Commit messages use conventions: `fix:`, `security:`, `docs:`, `test:`
- Reverts are explained (maturity)
- Docs evolve with the system (README/SECURITY updated as they go)

### Repository Safety Audit

Students are required to evaluate the repo *before cloning*. This is their first deliverable. Grade on:
- Did they actually inspect `package.json` for malicious scripts?
- Did they review the `.gitignore` and file list?
- Did they check for binaries, `.env` files with real secrets, or suspicious install hooks?
- Is their conclusion reasoned, not just "it looks fine"?

### Testing requirement

A fix without a test is duct tape. Students must write tests for their fixes. The CI pipeline (`npm test`) runs automatically. The initial `package.json` deliberately has `"test": "echo \"Error: no tests written yet\" && exit 1"` — the student must replace this with a real test runner and write actual tests.

**Important grading note:** For beginners, the AI Interaction Log and Decision Journal are weighted heavily. A student who documents their learning process, catches AI errors, and shows good judgment should score well even if their fixes are imperfect. A student who submits a perfect codebase with no log demonstrates nothing about their own learning.

---

## Facilitation Notes

### For instructors

- **Do not help with environment setup.** The student's first challenge is getting Node.js installed and the project running. This is deliberately part of the exercise — it forces them to use AI for something practical immediately.
- **Do not provide the issue list.** Discovery is the exercise.
- **Expect students to take 6-10 hours.** Beginners will spend significant time on setup, understanding error messages, and learning git basics.
- **The retrospective matters.** Students who write thoughtful retrospectives about what the AI missed, what they found hard, and what they'd do differently demonstrate the meta-cognitive skills this programme is building.
- **Watch for "AI did everything" submissions.** If the commit history is one commit, the log is empty, and the code is polished — the student likely had AI do everything without engaging. The log and journal are the safeguards.

### Adaptation

- **Shorter version (4 hours):** Tell students to focus only on security + documentation. Skip data cleaning and code quality.
- **Harder version:** Remove the three hints from the mission briefing. Require a Dockerfile as part of the handover.
- **Group version:** Teams of 3-5, assign roles (security auditor, bug hunter, documentarian). Add a handoff test where another team must set up the project from documentation alone.

---

## Files

```
01-the-developer-who-vanished/
├── MISSION-BRIEFING.md      ← What the student receives (sparse, minimal)
├── README.md                ← This file (instructor reference — NOT for students)
└── skycrm/                  ← The horror show
    ├── package.json         ← test script deliberately fails ("no tests yet")
    ├── server.js            ← 300+ line god file with 50+ issues
    ├── Dockerfile           ← Minimal, part of handover readiness signal
    ├── .env.example         ← Theatre (nothing reads from .env)
    ├── .gitignore
    ├── README.md            ← Jón's burnout manifesto
    ├── CHANGELOG.md         ← Emotional changelog
    ├── .github/
    │   └── workflows/
    │       ├── ci.yml              ← CI: install, lint, test, build, audit
    │       ├── codeql.yml          ← Security: CodeQL analysis
    │       └── docker-publish.yml  ← CD: build + push Docker image to GHCR
    ├── data/
    │   ├── customers.json   ← Duplicate IDs, PII in plaintext, test data
    │   ├── bookings.csv     ← Mixed delimiters, NaN, orphaned refs
    │   └── inventory.json   ← Duplicate IDs, negative prices, inconsistent naming
    └── public/
        ├── app.js           ← XSS, error suppression, double polling
        └── style.css        ← Dead CSS, conflicts with inline styles
```

### CI/CD Design Notes

The repo ships with three GitHub Actions workflows:

- **ci.yml** — Runs on every push/PR. Install, lint, test, build, audit. The `npm test` script deliberately fails out of the box (`"Error: no tests written yet"`), forcing students to set up a test runner and write tests before CI can pass.
- **codeql.yml** — Runs CodeQL security analysis. Will flag `eval()` patterns, injection risks, and other security issues automatically.
- **docker-publish.yml** — On merge to `main`, builds and pushes a Docker image to GHCR. This is the CD artifact — real deployment without hosting costs.

The Dockerfile is deliberately minimal (Jón-quality). Students may need to improve it as part of handover readiness.

### Branch protection (instructor setup)

After creating the upstream repo, configure branch protection on `main`:
- Require PR before merge
- Require status checks: `CI`, `CodeQL`
- Optionally require linear history (cleaner for review)
