# 👨‍🏫 Teaching Guide — Software Testing Virtual Lab

**Course:** Software Engineering (B.Tech 6th Semester)
**Unit:** Software Testing
**Institute:** 319 | Bareilly, Uttar Pradesh
**Prepared by:** Assistant Professor, CSE / AI Department

---

## Overview

This guide explains how to deliver the Software Testing Virtual Lab across
four different formats — from a single 90-minute demo to a full-day
competitive hackathon. Each format is self-contained and uses the same
lab artifact, so no additional preparation is needed beyond reading this document.

The lab covers:
- Black Box, White Box, and Grey Box testing
- Unit, Integration, System, and Acceptance testing
- Alpha and Beta testing
- Performance and Security testing
- Tools: Jest, pytest, Cypress, Postman, Playwright, k6, OWASP ZAP
- Six tech stacks: MERN, React, Flutter, Python, JS Full Stack, REST APIs

---

## Format 1 — Classroom Demo

**Duration:** 90 minutes
**Mode:** Lecturer-led, projected on screen
**Group size:** Full class (up to 60 students)
**Room:** Any classroom with projector + internet

### When to use this format

Best for the first session on software testing. Students have no prior
experience with testing tools. This session builds vocabulary and mental
models before students touch any code.

### Session Plan

| Time | Activity | Notes |
|---|---|---|
| 0–10 min | Open the Virtual Lab on projector | Start on Virtual Lab tab, MERN stack selected |
| 10–20 min | Explain the Testing Pyramid | Switch to Test Pyramid tab, walk through each layer |
| 20–35 min | Walk through MERN testing workflow | Show the 6-step workflow card |
| 35–50 min | Live code walkthrough | Read the Jest sample test aloud, explain each line |
| 50–65 min | Switch stacks live | Change to Python, ask students: "what changed? what stayed same?" |
| 65–75 min | Show Tool Mapping Table | Students call out a stack, you filter and read the row |
| 75–85 min | Open Hands-on Ex 1 | Show the broken auth code, ask "which test would catch this?" |
| 85–90 min | Tool install instructions | Share the repo link, tell students to install Jest/pytest before next class |

### Key Questions to Ask During Demo

- "If the login page works fine but the database is not saving — which layer of the pyramid caught it?"
- "What is the difference between a bug and a failure?"
- "Why do we write more unit tests than E2E tests?"
- "What happens if we skip integration testing?"

### Learning Outcome

By end of session, every student can name the testing pyramid layers,
identify the correct tool for their stack, and read a basic unit test.

---

## Format 2 — Workshop Activity

**Duration:** 3 hours
**Mode:** Group-based — 4 students per group
**Group size:** Up to 48 students (12 groups)
**Room:** Computer lab preferred, or BYOD classroom

### When to use this format

Best for the second or third session after the classroom demo. Students
already know the theory and now apply it collaboratively.

### Group Assignment

Assign each group a different tech stack. With 12 groups:
- Groups 1–2: MERN Stack
- Groups 3–4: React Frontend
- Groups 5–6: Flutter Mobile
- Groups 7–8: Python Backend
- Groups 9–10: JS Full Stack
- Groups 11–12: REST APIs / Microservices

### Session Plan

| Time | Activity |
|---|---|
| 0–10 min | Assign groups, open lab, each group selects their stack |
| 10–40 min | Groups explore their stack's Methodology tab — fill worksheet (see below) |
| 40–85 min | Groups work through Lab Exercises 1, 2, and 3 |
| 85–105 min | Each group presents: "Our stack, our tools, one bug we found" (5 min each) |
| 105–150 min | Cross-stack comparison — class fills the Tool Mapping Table together on whiteboard |
| 150–180 min | Debrief: which stack was hardest to test? why? |

### Worksheet for Groups (print or share digitally)

```
Group Name: _______________    Tech Stack: _______________

1. What are the 3 most important things to test in your stack?
   a. _______________
   b. _______________
   c. _______________

2. Which tool do you use for unit testing? _______________
3. Which tool do you use for E2E testing? _______________
4. Write one test case (any format):
   Input: _______________
   Expected Output: _______________
   Test Type: _______________

5. In Exercise 1 — which tests failed and why?
   _______________

6. In Exercise 3 — what was the root cause of the price bug?
   _______________
```

### Learning Outcome

Students can compare testing approaches across stacks, explain why tools
differ per technology, and present a basic testing strategy to a group.

---

## Format 3 — Mini Hackathon

**Duration:** 6–8 hours (full day)
**Mode:** Competitive teams of 3–4 students
**Group size:** Up to 40 students (10 teams)
**Room:** Computer lab, all day

### When to use this format

Best at the end of the software testing unit as a capstone event. Students
have completed all theory sessions and at least one workshop. This simulates
a real industry QA sprint.

### Schedule

| Time | Activity |
|---|---|
| 9:00 AM | Teams register, choose tech stack, receive the same base project |
| 9:15 AM | Problem brief: "You are the QA team for Trekoroma's new booking feature" |
| 9:30 AM | Teams begin: write test plan, set up tools |
| 11:00 AM | Faculty secretly introduces 5 bugs per project (different per team) |
| 11:15 AM | Teams notified: "A new deployment just went live. Find the regressions." |
| 1:00 PM | Lunch break — test suites keep running |
| 2:00 PM | Submission deadline: push code + test report to GitHub |
| 2:30 PM | Teams present: bugs found, coverage achieved, tools used (7 min each) |
| 4:00 PM | Scoring and leaderboard reveal |
| 4:30 PM | Retrospective: what real QA teams do differently |

### Scoring Rubric (50 points)

| Criterion | Points |
|---|---|
| Number of bugs found (2 pts each, max 5) | 10 |
| Test coverage achieved (1 pt per 10%) | 10 |
| Quality of test cases (clarity, EP/BVA used) | 10 |
| Bug report quality (ID, steps, severity, fix) | 10 |
| Team presentation and explanation | 10 |

### The 5 Secret Bugs to Introduce (Faculty Only)

These bugs are inserted into the sample-projects/ folder by faculty
before the hackathon. Do not share with students.

```
Bug 1 (Critical):   Remove password hash check in auth — any password works
Bug 2 (High):       Discount calculation returns 0% instead of 20%
Bug 3 (Medium):     Email notification not triggered on booking confirmation
Bug 4 (Low):        Trek search returns results sorted by price desc, not asc
Bug 5 (Edge case):  Booking with past date accepted without error
```

### Learning Outcome

Students experience a real QA workflow under time pressure. They learn to
prioritise bugs by severity, write a professional bug report, and present
findings to stakeholders — exactly as in industry.

---

## Format 4 — Lab Experiment (Individual Assessment)

**Duration:** 2 hours
**Mode:** Individual, supervised
**Group size:** Full class (each student works alone)
**Room:** Computer lab

### When to use this format

Best as a formative or summative assessment. Each student gets an
individual broken codebase and must diagnose, document, and fix it alone.

### Lab Procedure

1. Distribute the broken codebase (one per student, or same for all)
2. Students must NOT share code or discuss during the session
3. Students submit at the end of 2 hours:
   - Bug report (Word/PDF)
   - Fixed code file
   - Screenshot of passing test suite
   - Screenshot of coverage report

### Invigilator Instructions

- Ensure every student's machine has Node.js + pytest installed before session
- The broken file is in `sample-projects/` — distribute via Google Classroom or USB
- Students may use the Virtual Lab and Flashcards for reference during the session
- Do not help with the bug location — only help with tool installation issues

### Student Instructions (share this)

```
Lab Experiment — Software Testing
Time: 2 hours | Individual | Open Lab (no peer discussion)

You have been given a broken codebase.
Your job is to act as a QA Engineer.

Step 1: Run the existing test suite and record which tests fail
Step 2: Read the code and identify the root cause of each failure
Step 3: Write a bug report for each bug found (template below)
Step 4: Fix the bug in the code
Step 5: Run the test suite again — all tests should now pass
Step 6: Take a screenshot of your coverage report
Step 7: Submit: bug report + fixed file + screenshots

Bug Report Template:
  Bug ID:        BUG-001
  Title:         One-line description
  Severity:      Critical / High / Medium / Low
  Steps:         1. ... 2. ... 3. ...
  Expected:      What should happen
  Actual:        What actually happens
  Root Cause:    Why it happened (code level)
  Fix Applied:   What you changed
```

### Learning Outcome

Individual competency in reading test failures, diagnosing root causes,
writing professional bug reports, and verifying fixes with a test suite.

---

## General Tips for All Formats

### Before class
- Test the lab URL works on the projector browser
- Ensure GitHub Pages is live (visit your URL yourself first)
- Have the offline HTML file as backup in case of internet issues

### During class
- Start every session with: "What could go wrong in Trekoroma today?"
  Let students guess, then show the test that catches it
- Always flip between at least two stacks to show what changes vs what stays the same
- When a test fails on screen, pause and ask "what does this tell us?" before explaining

### After class
- Share the repo link in WhatsApp group immediately after session
- Ask students to star the repo (builds their GitHub profile too)
- In the next session, start with: "Did anyone run the exercises at home? What happened?"

---

## Prerequisites for Students

| Tool | Install Command | Used For |
|---|---|---|
| Node.js (v18+) | https://nodejs.org | Jest, Cypress, Playwright |
| Python (3.10+) | https://python.org | pytest, coverage.py, Locust |
| Git | https://git-scm.com | Cloning the repo |
| Postman | https://postman.com/downloads | API testing |
| VS Code | https://code.visualstudio.com | Code editor |

All other tools install via npm or pip — see `docs/tool-setup.md`.

---

*Last updated: April 2026 | Institute 319 | CSE / AI Department*
