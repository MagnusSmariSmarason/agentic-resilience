# Hello World

**Problem 00** · Solo · Estimated 2–4 hours · No experience required

> *Concept & design: Magnús Smári Smárason*
> *Alpha v1 — For testing on willing subjects*

> **Student name:** ___________________________
>
> **Date started:** ___________________________
>
> **AI assistant(s) used:** ___________________________

---

## You

You have never used a terminal. You have never written code. You might not know what GitHub is. That is completely fine.

This is not a test. This is a setup guide disguised as a mission. By the end, you will have a working development environment, a GitHub account with your first repository, and your first commit. You will have done all of it with AI as your guide.

Think of this as the tutorial level. The real missions start after this.

---

## The Situation

You have enrolled in a programme that requires you to work with code, data, and AI tools. Before you can do any of that, you need to set up your machine.

This sounds boring. It is the single most common reason people give up on technical work — they can't get past the setup. Today, AI changes that. You will use an AI assistant to walk you through every step, and by the end you will have a working setup that carries you through the rest of the programme.

You will also fix a tiny broken website. Nothing scary — just enough to prove the tools work and you know how to use them.

---

## What You Need

1. **A computer** (Mac, Windows, or Linux)
2. **An internet connection**
3. **An AI assistant** — any of these will work, all have free tiers:
   - [ChatGPT](https://chat.openai.com) (free tier)
   - [Claude](https://claude.ai) (free tier)
   - [Gemini](https://gemini.google.com) (free tier)
   - [GitHub Copilot](https://github.com/features/copilot) (free for students)
   - Or any other AI coding assistant

That's it. Everything else, we install together.

---

## Step 0: Meet Your AI

Before installing anything, let's make sure you and your AI understand each other.

Open your AI assistant and type exactly this:

> *"I am a university student with no programming experience. I need to set up my computer for software development. I am on [Mac/Windows/Linux]. I need to install: Git, Node.js, and Visual Studio Code. I also need to create a GitHub account. Please walk me through each step, one at a time, in plain language. After each step, I will tell you what happened before we move to the next one."*

**Replace `[Mac/Windows/Linux]` with your actual operating system.** If you don't know which one you have, ask the AI: *"How do I find out what operating system my computer is running?"*

This is your first AI interaction. Write it down in the log at the bottom of this document.

### Your First Interaction

| Field | Your Entry |
|-------|-----------|
| **What I asked** | |
| **What the AI said** (summary) | |
| **Did it work?** | |
| **What I learned** | |

---

## Your Mission

### Phase 1: Set Up Your Tools (60–90 minutes)

Follow your AI's instructions to install these tools. After each one, verify it works.

#### 1. Visual Studio Code (VS Code)

VS Code is a text editor for code. It's free and used by most developers worldwide.

- Ask your AI: *"How do I install Visual Studio Code on [my operating system]?"*
- Download and install it
- Open it. You should see a welcome screen.

**Verify:** Open VS Code. Can you see a window with a dark theme and a welcome tab?

#### 2. A Terminal

A terminal is a text-based way to talk to your computer. You type commands, it does things.

- **Mac:** You already have one. Ask your AI: *"How do I open the terminal on Mac?"* (It's called Terminal, and lives in Applications > Utilities. VS Code also has one built in.)
- **Windows:** Ask your AI: *"How do I set up Windows Terminal with WSL2?"* This gives you a Linux environment inside Windows, which is how professional developers work on Windows.
- **Linux:** You already have one. Ask your AI: *"How do I open the terminal on [your Linux distribution]?"*

**Verify:** Open your terminal. Type `echo "hello"` and press Enter. You should see `hello` printed back.

#### 3. Git

Git is a tool that tracks changes to files. Think of it as "undo history" for your entire project, shared with the world.

- Ask your AI: *"How do I install Git on [my operating system]?"*
- After installing, configure it:
  ```
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  ```

**Verify:** In your terminal, type `git --version`. You should see something like `git version 2.43.0` (the number doesn't matter, as long as it shows a version).

#### 4. GitHub Account

GitHub is where developers store and share code. Think of it as "Google Drive for code, with superpowers."

- Go to [github.com](https://github.com) and create a free account
- **Important:** If you're a student, apply for the [GitHub Education pack](https://education.github.com/pack) — it gives you free access to many tools including GitHub Copilot

After creating your account, install the GitHub CLI (command-line tool):

- Ask your AI: *"How do I install and set up the GitHub CLI (gh) on [my operating system]?"*
- Then authenticate: `gh auth login` and follow the prompts

**Verify:** In your terminal, type `gh auth status`. You should see your username and that you're logged in.

#### 5. Node.js

Node.js lets you run JavaScript on your computer (not just in a browser). Many web applications use it.

- Ask your AI: *"What is the best way to install Node.js in 2026? Should I use nvm, fnm, or install it directly?"*
- Follow the AI's recommendation. (Most will suggest `fnm` or `nvm` — these let you manage multiple versions easily.)
- Install **Node.js 22** (the current LTS — Long Term Support — version)

**Verify:** In your terminal, type `node --version`. You should see `v22.x.x` (some version starting with 22). Also type `npm --version` — you should see a version number.

#### The Checkpoint

Fill in this table to confirm everything is working:

| Tool | Command to verify | Expected output | Your result | Working? (Y/N) |
|------|------------------|-----------------|-------------|-----------------|
| VS Code | Open the application | Welcome screen appears | | |
| Terminal | `echo "hello"` | Prints `hello` | | |
| Git | `git --version` | A version number | | |
| GitHub CLI | `gh auth status` | Your username, logged in | | |
| Node.js | `node --version` | `v22.x.x` | | |
| npm | `npm --version` | A version number | | |

**If anything isn't working:** Don't panic. Copy the exact error message and paste it to your AI: *"I tried [command] and got this error: [error]. What's wrong and how do I fix it?"* This is exactly how developers debug problems. The error message is the clue.

---

### Phase 2: Your First Repository (30–45 minutes)

Now you'll create your first project and push it to GitHub.

#### 1. Get the starter files

The starter project is in the `starter/` folder of this problem. It contains a tiny broken website. Your job is to fix it.

Copy the `starter/` folder to your own workspace:

```
cp -r starter/ ~/hello-world
cd ~/hello-world
```

Or ask your AI: *"How do I copy a folder to my home directory?"*

#### 2. Look at what you have

Open the `hello-world` folder in VS Code:

```
code ~/hello-world
```

You should see three files:
- `package.json` — describes the project and its dependencies
- `server.js` — the server that runs the website
- `public/index.html` — the web page itself

**Read each file.** Ask your AI: *"Explain this file to me line by line: [paste file contents]"*

#### 3. Try to run it

In your terminal (make sure you're in the `hello-world` folder):

```
npm install
npm start
```

Open your browser and go to: `http://localhost:3000`

Something is wrong. The page doesn't look right. **That's intentional.**

#### 4. Find and fix the bugs

There are exactly **3 small problems** in the starter files. They are not security vulnerabilities or complex issues — they are beginner-level mistakes that your AI can help you find and fix.

Ask your AI: *"I'm running a simple Node.js web app. Here's my server.js: [paste it]. Here's my index.html: [paste it]. The page isn't working correctly. Can you spot what's wrong?"*

**For each bug you find:**
1. Understand what's wrong (ask the AI to explain)
2. Fix it
3. Verify the fix works (refresh the browser)
4. Save the file

#### 5. Make your first commits

After fixing each bug, save your work with git:

```
git init
git add .
git commit -m "fix: [describe what you fixed]"
```

Ask your AI: *"What does git init do? What does git add do? What does git commit do?"*

**Make separate commits for each fix.** Not one big commit at the end. This is a habit you'll use for the rest of the programme.

#### 6. Push to GitHub

Create a repository on GitHub and push your work:

```
gh repo create hello-world --public --source=. --push
```

Or ask your AI: *"How do I create a new GitHub repository and push my local code to it?"*

**Verify:** Go to `github.com/[your-username]/hello-world` in your browser. You should see your files and your commit history.

---

### Phase 3: Prove It Works (15–30 minutes)

Take a screenshot of each of the following and include them in your submission (or describe what you see):

1. **Your terminal** showing `node --version` and `npm --version`
2. **The fixed website** running in your browser at `localhost:3000`
3. **Your GitHub repository** showing your commits

---

## Rules

### 1. Use AI for everything

You are **expected** to use AI for every step. Asking "what is a terminal?" is not a stupid question — it is the assignment. Asking "explain this error message" is not cheating — it's how you learn.

### 2. Keep a log

Every time you ask your AI something, write it down. What you asked, what it said, whether it helped. This log is the most important part of your submission.

### 3. The AI will be wrong

Even in a simple setup exercise, AI will occasionally give you outdated instructions, wrong paths, or commands that don't work on your specific system. When this happens, write it down. It's not a failure — it's a learning moment.

### 4. You own the decisions

If the AI suggests something you don't understand, ask it to explain. Don't blindly copy-paste commands into your terminal without knowing what they do. You are the operator.

### 5. Error messages are clues, not walls

Every error message is telling you something specific. Copy it. Paste it to your AI. Ask what it means. This is the single most important debugging skill in all of software development.

### 6. There is no time pressure

This is the setup mission. Take as long as you need. If something takes 4 hours instead of 2, that's fine. If you need to come back tomorrow, that's fine. The only failure is not finishing.

---

## Your Work

### Setup Log

> Document what you installed and any issues you encountered.

| Step | Tool | What happened | Issues? | How you resolved them |
|------|------|--------------|---------|----------------------|
| 1 | VS Code | | | |
| 2 | Terminal | | | |
| 3 | Git | | | |
| 4 | GitHub + CLI | | | |
| 5 | Node.js | | | |

### Bug Fix Log

> Document the 3 bugs you found and fixed.

| # | What was wrong | How you found it | How you fixed it | Commit message |
|---|---------------|-----------------|-----------------|----------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

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

*(Copy this template for each significant interaction. Aim for 5+ entries.)*

### Decision Journal

> For each decision you made (even small ones), record it here.

#### Decision 1

| Field | Your Entry |
|-------|-----------|
| **What was the decision?** | |
| **What options did you consider?** | |
| **What did the AI recommend?** | |
| **What did you choose and why?** | |

*(Copy this template for each decision. Aim for 3+ entries.)*

### Times the AI Was Wrong

> Even in a simple exercise, the AI may give you outdated or incorrect instructions. Document them here.

| # | What the AI said | Why it was wrong | How you figured it out |
|---|-----------------|------------------|----------------------|
| 1 | | | |
| 2 | | | |

---

## What You Submit

1. **A GitHub repository** (`hello-world`) with your fixed code and commit history
2. **This completed mission briefing** with all logs filled in
3. **Screenshots** (or descriptions) of your working setup
4. **A short retrospective** (below)

---

## Retrospective

> Write 100–200 words. Be honest.

**What was the hardest part of setting up your environment?**

> _______________________________________________________________
>
> _______________________________________________________________

**Where did the AI help most?**

> _______________________________________________________________
>
> _______________________________________________________________

**Was there a moment where you felt lost? What did you do?**

> _______________________________________________________________
>
> _______________________________________________________________

**Do you feel ready to take on a bigger challenge?**

> _______________________________________________________________
>
> _______________________________________________________________

---

## Evaluation

| Criterion | Weight | What we're looking for |
|-----------|--------|----------------------|
| **Working setup** | 30% | All tools installed and verified. The checkpoint table is complete. |
| **Fixed starter project** | 20% | All 3 bugs found and fixed. Website works. |
| **Git & GitHub** | 20% | Repository exists. Multiple commits (not one). Code is pushed. |
| **AI Interaction Log** | 20% | Honest, detailed log of AI interactions. Shows learning. |
| **Retrospective** | 10% | Thoughtful reflection on the experience. |

Notice: **AI Interaction Log** is weighted as heavily as the technical work. A working setup with no log is worth less than a messy setup with a detailed, honest log of how you got there.

---

## Hints

You get three. Each one is for when you're truly stuck.

1. **"The AI speaks your operating system's language."** — Always tell the AI which operating system you're using. Instructions for Mac, Windows, and Linux are often completely different. If the AI gives you a command that doesn't work, it might be giving you instructions for the wrong system.

2. **"Read the error, don't fear the error."** — When something fails, the error message almost always tells you exactly what went wrong. Copy the entire error message and paste it to your AI. Don't try to summarize it yourself — the details matter.

3. **"The three bugs are not hiding."** — The bugs in the starter project are visible. One is in the HTML, one is in the server, and one is in the configuration. You don't need to be clever to find them. Just read the code carefully (with your AI) and try to understand what each line does.

---

## Before You Start

Open your AI assistant and type:

> *"I am a complete beginner. I have never used a terminal or written code. I need to set up my computer for software development. I am on [Mac/Windows/Linux]. Can you walk me through installing Visual Studio Code, Git, Node.js, and the GitHub CLI? Please go one step at a time and wait for me to confirm each step works before moving on."*

Then follow the instructions. When something doesn't make sense, ask again. When something breaks, paste the error message and ask what went wrong.

You've got this.

---

## A Note on Frustration

This is a setup exercise, but that doesn't mean it will be easy. Environment setup is genuinely one of the hardest parts of software development — not because it's intellectually difficult, but because every computer is slightly different and things break in unpredictable ways.

If you spend 30 minutes debugging why Node.js won't install, that's not a failure. That's a rite of passage that every developer has gone through. The difference is that you have AI to help you through it.

If something takes longer than expected, take a break. Come back. Ask the AI again with more detail. You will get through it.

And once you do — once your terminal shows `v22.x.x` and your code is on GitHub and your website loads in the browser — you'll have done something that most people never do. You'll have set up a professional development environment from scratch.

The rest of the programme builds on this. Everything that follows assumes you can open a terminal, run a command, and push to GitHub. This mission gives you those foundations.

Go.

---

*"When AI handles the doing, humans must own the deciding."*
*— Agentic Resilience Manifesto*
