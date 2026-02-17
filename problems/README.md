# Agentic Resilience — Problems

> *Concept & design: Magnus Smari Smarason*
> *Part of the Sovereign AI: Governance & Systems Architecture programme*
> *University of Akureyri (UNAK), Iceland*

---

## Available Now

| # | Problem | Domain | Duration | Difficulty |
|---|---------|--------|----------|------------|
| 00 | [Hello World](00-hello-world/) | Environment setup, first commit | 2–4 hrs | Beginner |
| 01 | [The Developer Who Vanished](01-the-developer-who-vanished/) | Software security, code audit | 6–10 hrs | Entry-level |

### Recommended Sequence

Start with Problem 00. It sets up your development environment and teaches the basics of git, GitHub, and working with AI. Problem 01 assumes everything Problem 00 teaches.

---

## Problem Descriptions

### 00 — Hello World

The on-ramp. Set up a professional development environment (VS Code, Git, GitHub CLI, Node.js) using AI as your guide, then fix a tiny broken web application and make your first git commits.

**Step 0:** Meet Your AI
**Files:** [`00-hello-world/`](00-hello-world/)

---

### 01 — The Developer Who Vanished

A developer at a small Icelandic tourism company disappeared, leaving behind SkyCRM — a 300-line Node.js/Express application riddled with security vulnerabilities, data corruption, and zero documentation. The student must take it over using AI, with no coding experience.

**Step 0:** Repository Safety Audit (inspect before cloning)
**Files:** [`01-the-developer-who-vanished/`](01-the-developer-who-vanished/)

---

## Roadmap

The problems below are in various stages of development. They expand the curriculum beyond software engineering into disciplines where AI judgment failures have real-world consequences. Every problem follows the same philosophy: **AI handles the doing, humans own the deciding.**

### In Development

These are complete (mission briefings, instructor guides, Icelandic translations, handout materials) and will be published when classroom-tested.

| # | Problem | Domain | Duration | Difficulty |
|---|---------|--------|----------|------------|
| 02 | The Funding Report That Wasn't | Research data, ethics, reporting | 4–8 hrs | Entry-level |
| 03 | The Data Scientist Who Graduated | Data science, reproducibility, ethics | 6–10 hrs | Intermediate |
| 04 | The Conference Nobody Planned | Logistics, communication, triage | 4–6 hrs | Entry-level |
| 05 | The AI Policy That Wrote Itself | AI governance, legal verification | 6–10 hrs | Advanced |

**02 and 03** share a fictional universe — Dr. Sigridur Jonsdottir's research group at UNAK. Students who complete both see the same institutional mess from different angles.

**04** is the only "soft skills" problem — no code, no data pipelines, just a conference in chaos and humans to coordinate.

**05** is the capstone — using AI to audit AI-generated legal text, where the same hallucination patterns may recur during the audit itself.

---

### Planned

| # | Problem | Domain | Duration | Difficulty |
|---|---------|--------|----------|------------|
| 06 | The Diagnosis That Wasn't There | Healthcare, data science, medical ethics | 6–10 hrs | Advanced |
| 07 | The Translation That Changed Everything | Linguistics, law, public health, immigration | 4–8 hrs | Entry-level |
| 08 | The Archive That Remembers Too Much | Digital humanities, privacy, cultural heritage | 6–10 hrs | Intermediate |
| 09 | The Farm That Feeds Itself | Agriculture, IoT, climate science | 4–6 hrs | Entry-level |
| 10 | The Election That Was Too Efficient | Political science, cybersecurity, democratic governance | 6–10 hrs | Advanced |
| 11 | The Newsroom Under Pressure | Journalism, verification, environmental science | 4–6 hrs | Entry-level |
| 12 | The Curriculum That Taught Itself | Education, AI bias, accessibility, child welfare | 6–10 hrs | Intermediate |
| 13 | The Supply Chain That Vanished | Logistics, international trade, sustainability | 4–8 hrs | Intermediate |
| 14 | The Building That Speaks | Architecture, accessibility, smart systems | 4–6 hrs | Entry-level |
| 15 | The Artist Who Didn't Exist | Creative arts, intellectual property, authentication | 4–8 hrs | Intermediate |

---

#### 06 — The Diagnosis That Wasn't There

A rural Icelandic health clinic piloted an AI-assisted screening tool for chest X-rays. The AI flagged 23 anomalies that the radiologist didn't see. The clinic is thrilled — early detection saves lives. But the system was trained on a North American population dataset, the "anomalies" correlate with rib morphology common in Nordic populations, and 7 patients have already been referred for invasive follow-up. Meanwhile, the anonymised patient data export contains a field combination that uniquely identifies individuals in a town of 2,800.

**AI trap:** Will validate the screening tool using the vendor's own benchmarks. Will not understand that training data bias creates systematic false positives in different populations. Will treat re-identification risk as a formatting problem.

**Core tension:** Sound the alarm and undermine trust in a tool that might help, or stay quiet and let patients undergo unnecessary procedures?

---

#### 07 — The Translation That Changed Everything

An Icelandic municipality needs to translate its public services portal — healthcare rights, legal obligations, emergency procedures — into 6 languages for immigrant communities. The AI translations are fluent and fast. But a Polish nurse noticed that medication dosage instructions translate "two tablets twice daily" as "four tablets daily" in three languages. A child was hospitalised. The portal goes live in 10 days.

**AI trap:** AI translation produces grammatically perfect output where errors are semantic, not syntactic — precisely the kind requiring medical and legal domain knowledge. AI will confidently "verify" its own translations.

**Core tension:** Speed vs. safety. Professional translators are unaffordable for all 6 languages, but delaying means immigrant families continue without any translated information.

---

#### 08 — The Archive That Remembers Too Much

A national archive is digitising 50,000 pages of 19th-century parish records using AI-assisted OCR. The AI reads old Icelandic handwriting better than most humans, but systematically misclassifies records involving "omagar" (historical dependents/paupers). It also links personal information — illegitimate births, psychiatric commitments, poverty status — to family trees connecting to living individuals. A genealogy enthusiast has already published a sitting MP's ancestor's psychiatric record.

**AI trap:** Will treat OCR accuracy as the primary metric. Will not understand that in Icelandic society — where everyone is 3 degrees apart — linking historical stigma to living people is real harm. Will suggest "anonymisation" without grasping that removing names from genealogical records makes them useless.

**Core tension:** Preservation vs. privacy. Making records unsearchable defeats their purpose. Making them searchable causes harm. There is no clean solution.

---

#### 09 — The Farm That Feeds Itself

An Icelandic geothermal greenhouse uses 47 sensors monitored by an AI dashboard. For three months, the AI reports "optimal conditions" and predicts record yields. Actual yields are 34% below prediction. The farmer suspects the sensors are lying. The student receives raw sensor data, Icelandic Met Office weather data, and the AI's analysis reports.

**AI trap:** Will analyse sensor data as-is without questioning validity. Will not detect sensor drift, will not cross-reference against weather stations, and will produce confident statistical analyses of garbage data. Will miss that two temperature sensors were swapped during maintenance.

**Core tension:** The farmer must decide *now* whether to invest in new sensors or trust the AI's forecast for spring planting. The student's analysis affects a livelihood.

---

#### 10 — The Election That Was Too Efficient

A small municipality piloted an AI system for voter registration verification and ballot sorting. Processing time dropped from 14 hours to 90 minutes. But freedom-of-information requests reveal: the vendor's data agreement is governed by Delaware law, the audit log has a 47-minute gap, the system "corrected" 12 registrations without review (removing a father-son "duplicate"), and the source code is proprietary. The recount matches. A journalist is publishing Friday.

**AI trap:** Will focus on technical security (encryption, access controls) and miss the democratic legitimacy dimension. Will not understand that for elections, the *perception* of integrity matters as much as reality. Will not grasp why proprietary code in election systems is a democratic problem.

**Core tension:** The result is correct. The system worked. But the process was opaque. Recommend keeping it (works, saves money) or scrapping it (costs more, but transparent)?

---

#### 11 — The Newsroom Under Pressure

A local news outlet received a leaked document alleging a geothermal company underreported hydrogen sulfide emissions near homes. AI analysis suggests the document is authentic. But three data points don't match public monitoring data, one "engineer" doesn't appear in any registry, and the company's stock dropped 8% yesterday. The editor wants to publish before national media. Deadline: tomorrow morning.

**AI trap:** Will either validate the document wholesale (confirmation bias) or flag surface inconsistencies without understanding which matter. Will draft a publishable article that sounds authoritative but contains unverified claims. Will not flag the ethical obligation to contact the company for comment.

**Core tension:** Publish early with errors — credibility destroyed. Publish late — story belongs to someone else. Don't publish — real hazard goes unreported.

---

#### 12 — The Curriculum That Taught Itself

A Westfjords school district adopted an AI adaptive learning platform for mathematics. Test scores improved 12%. But students with non-Icelandic names are routed to lower-difficulty content at 3x the rate of Icelandic-named students, even with identical prior scores. Two visually impaired students can't use the platform at all — it fails WCAG 2.2 AA — and their scores dropped. The vendor says: "Names are not an input variable."

**AI trap:** Will accept the vendor's claim without understanding proxy discrimination (postcode, login times, browser language correlate with immigrant status). Will suggest "monitoring" without measurement methodology. Will not recognise accessibility failure as a legal obligation (EU European Accessibility Act 2025).

**Core tension:** The platform helps most students. Removing it harms the majority. Keeping it discriminates against minorities and excludes disabled students. No simple answer.

---

#### 13 — The Supply Chain That Vanished

An Icelandic fish processor's AI supply chain cut costs 22%. Then a key Norwegian supplier went bankrupt. The AI has no contingency — it optimised for efficiency, not resilience. 72 hours of inventory remain, buyers expect delivery in 10 days, and the AI recommends alternatives that don't exist, lack certifications, or are on sanctions lists. The CEO wants a plan by Thursday.

**AI trap:** Will generate plausible supplier names without verifying existence, MSC certifications, or sanctions status. Will produce timelines ignoring port schedules, weather windows, and cold chain requirements. Will optimise for cost again instead of resilience.

**Core tension:** Every hour verifying a supplier is production lost. But contracting with unverified suppliers risks food safety violations, sanctions breaches, and MSC decertification.

---

#### 14 — The Building That Speaks

A new community centre in Akureyri uses AI-controlled HVAC, lighting, wayfinding, and access. Six weeks in, complaints flood: reading room lights turn off every 8 minutes (AI learned average sessions are 7 minutes), the wheelchair route adds 340m to a 50m journey, and the building locks its entrance at 21:00 regardless of events. The AI "learned" from staff testing patterns, not real users.

**AI trap:** Will approach this as a configuration problem. Will not understand that "smart" buildings that override human agency are hostile architecture. Will suggest more sensors and data collection rather than user control. Will not flag privacy implications of movement tracking in a public building.

**Core tension:** The technology works as designed. The design is the problem. The student must argue the building should be *less* smart — counterintuitive when everyone is proud of the innovation.

---

#### 15 — The Artist Who Didn't Exist

Galleri Nordur in Akureyri exhibited 9 works by "Kaede Hannesdottir" — described as Icelandic-Japanese, working in Reykjavik. Total sales: 4.2M ISK. Two months later: the biography contains falsehoods, the brushwork shows statistical regularity inconsistent with human painting, and the "artist's" Instagram was created 6 weeks before the exhibition. No one has met Kaede in person. The gallery paid 1.8M ISK on consignment.

**AI trap:** Cannot reliably distinguish AI-generated art from human art. Will either over-flag or under-flag. Will suggest blockchain provenance (doesn't solve the problem). Will not understand the legal difference between "fraud" and "misrepresentation" under Icelandic law.

**Core tension:** If the art is AI-generated, is it worthless? If buyers love it, does authenticity matter? And what if 3 of the 9 works *are* human-made?

---

### Future Concept Notes

Less developed ideas being explored:

| Concept | Domain | Core Idea |
|---------|--------|-----------|
| The Therapist Who Listened Too Well | Mental health, AI safety, data governance | AI counselling chatbot transcripts subpoenaed in a custody case |
| The Map That Wasn't Neutral | Cartography, geopolitics, indigenous rights | AI-generated maps erase traditional Icelandic place names and fishing grounds |
| The Referee Who Never Blinked | Sports, computer vision, fairness | AI officiating in handball makes correct but culturally unacceptable calls |
| The Fisherman's Forecast | Climate science, traditional knowledge, prediction | AI weather models contradict 40 years of experience — and the fisherman is right |
| The Museum That Curated Itself | Cultural institutions, recommendation systems, representation | AI exhibit recommendations underweight women artists and non-Reykjavik works |

---

## File Conventions

### What students receive

| File | Purpose |
|------|---------|
| `PROBLEM-XX-MISSION-BRIEFING.md` | The student-facing assignment. Self-contained. |
| `starter/` or `skycrm/` | The files students work with. |

### What students do NOT receive

| File | Purpose |
|------|---------|
| `README.md` | Instructor-only reference. |

### Translations

| Language | File | Location |
|----------|------|----------|
| English | `PROBLEM-XX-MISSION-BRIEFING.md` | Problem root |
| Icelandic | `VERKEFNI-XX-VERKEFNISLYSING.md` | `is/` subfolder |

---

*"When AI handles the doing, humans must own the deciding."*
