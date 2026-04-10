# 📋 Assessment Rubric — Software Testing Unit

**Course:** Software Engineering (B.Tech 6th Semester)
**Unit:** Software Testing
**Max Marks:** 100
**Institute:** 319 | Bareilly, Uttar Pradesh

---

## Overview

This rubric is used to assess student performance across the Software
Testing unit. It applies to both the hands-on lab experiment and the
mini-project submission. Each criterion is worth 20 marks, assessed
on a four-point scale.

---

## Main Rubric (100 Marks)

### Criterion 1 — Test Case Design (20 Marks)

*Assesses whether the student can design meaningful test cases using
recognised techniques.*

| Marks | Grade | Descriptor |
|---|---|---|
| 18–20 | A (Excellent) | Correctly applies Equivalence Partitioning, Boundary Value Analysis, and Decision Table Testing. Test cases have unique IDs, clear inputs, expected outputs, and pass/fail status. All valid and invalid partitions covered. |
| 14–17 | B (Good) | Correctly applies at least two of the three techniques. Most test cases are well-formed with IDs and expected outputs. Minor gaps in invalid partition coverage. |
| 10–13 | C (Pass) | Applies one technique partially correctly. Test cases have inputs and expected outputs but lack IDs or structured format. Some boundary values missed. |
| 6–9 | D (Below Pass) | Test cases written informally without a recognised technique. No distinction between valid and invalid partitions. |
| 0–5 | F (Fail) | No evidence of structured test case design. Random inputs with no expected outputs. |

**What to look for:**
- Are Equivalence Partitions identified and labelled?
- Are boundary values (min-1, min, min+1, max-1, max, max+1) all tested?
- Is there at least one valid and one invalid partition tested?
- Do test cases have a clear ID, input, expected output, and actual result?

---

### Criterion 2 — Code Coverage (20 Marks)

*Assesses whether the student's test suite achieves meaningful code coverage
and whether the student understands what coverage means.*

| Marks | Grade | Descriptor |
|---|---|---|
| 18–20 | A (Excellent) | Coverage ≥ 80% achieved and verified with a tool (coverage.py / Jest --coverage). Student identifies uncovered branches and explains why they were not covered. |
| 14–17 | B (Good) | Coverage 60–79% achieved with tool evidence. Most branches covered. Student can read the coverage report but does not explain gaps. |
| 10–13 | C (Pass) | Coverage 40–59% achieved. Tool used but report not fully interpreted. Some branches and statements missed without explanation. |
| 6–9 | D (Below Pass) | Coverage below 40% or no tool used. Student claims coverage without evidence. |
| 0–5 | F (Fail) | No coverage report. No evidence that tests were run against actual code. |

**What to look for:**
- Is a coverage screenshot or report attached?
- Does the report show statement coverage AND branch coverage?
- Can the student explain what the red lines (uncovered) mean?
- Is the coverage tool appropriate for the tech stack used?

**Accepted coverage tools by stack:**

| Stack | Tool | Command |
|---|---|---|
| MERN / React / JS | Jest | `jest --coverage` |
| Python | coverage.py | `coverage run -m pytest && coverage report` |
| Flutter | flutter_test | `flutter test --coverage` |
| Next.js | Vitest | `vitest run --coverage` |

---

### Criterion 3 — Tool Usage (20 Marks)

*Assesses whether the student selects and uses the correct testing tools
for their chosen technology stack.*

| Marks | Grade | Descriptor |
|---|---|---|
| 18–20 | A (Excellent) | Uses 3 or more tools appropriate to the stack (e.g. Jest + Postman + Cypress for MERN). All tools used correctly with evidence (screenshots, output logs, or test files). |
| 14–17 | B (Good) | Uses 2 appropriate tools with evidence. Minor configuration errors that do not affect test results. |
| 10–13 | C (Pass) | Uses 1 appropriate tool correctly. Other tools mentioned but not demonstrated. |
| 6–9 | D (Below Pass) | Tools used are inappropriate for the stack (e.g. flutter_test used for a Python project). Evidence is incomplete. |
| 0–5 | F (Fail) | No tools used or demonstrated. Testing done manually without a framework. |

**Expected tools per stack:**

| Stack | Minimum (C) | Good (B) | Excellent (A) |
|---|---|---|---|
| MERN | Jest | + Postman | + Cypress |
| React | Jest | + RTL | + Playwright |
| Flutter | flutter_test | + mockito | + Firebase Test Lab |
| Python | pytest | + coverage.py | + Locust or Bandit |
| JS Full Stack | Vitest | + Playwright | + Lighthouse CI |
| REST APIs | Postman | + k6 | + OWASP ZAP |

---

### Criterion 4 — Bug Report Quality (20 Marks)

*Assesses whether the student can document bugs professionally in a format
suitable for industry use.*

| Marks | Grade | Descriptor |
|---|---|---|
| 18–20 | A (Excellent) | Each bug report includes: unique ID, descriptive title, severity (Critical/High/Medium/Low), priority, step-by-step reproduction steps, expected behaviour, actual behaviour, environment details, root cause analysis, and confirmation that fix was verified by rerunning the test suite. |
| 14–17 | B (Good) | Bug report includes ID, title, severity, reproduction steps, expected and actual behaviour. Root cause identified but fix not verified. |
| 10–13 | C (Pass) | Bug identified and described with steps to reproduce. Severity assigned but not justified. No root cause analysis. |
| 6–9 | D (Below Pass) | Bug described informally. No severity, no reproduction steps. Fix not verified. |
| 0–5 | F (Fail) | No bug report submitted or bugs listed as a single sentence with no structure. |

**Bug Report Template (share with students):**

```
Bug ID:       BUG-001
Title:        [Short, specific description — e.g. "Login accepts any password"]
Severity:     Critical / High / Medium / Low
Priority:     P1 / P2 / P3
Reported by:  [Student name / roll number]
Date:         [Date]

Steps to Reproduce:
  1. Open the application at localhost:3000
  2. Enter a valid email address
  3. Enter any random password (e.g. "wrongpassword")
  4. Click Login

Expected Result:
  Login should fail with error: "Invalid credentials"

Actual Result:
  Login succeeds and user is redirected to dashboard

Environment:
  Browser: Chrome 120 | OS: Windows 11 | Node: v18.12

Root Cause:
  The password comparison check was removed from auth.js (line 24).
  bcrypt.compare() was never called, so any password passes.

Fix Applied:
  Restored bcrypt.compare(password, user.hash) check on line 24.

Verification:
  Reran test suite after fix. Test "rejects invalid password" now PASSES.
  Screenshot: [attached]
```

---

### Criterion 5 — CI/CD Integration (20 Marks)

*Assesses whether the student understands and can implement automated
testing within a CI/CD pipeline.*

| Marks | Grade | Descriptor |
|---|---|---|
| 18–20 | A (Excellent) | Full CI pipeline configured (e.g. GitHub Actions .yml file). Pipeline runs unit tests, integration tests, and at least one other stage (coverage check, E2E, or security scan) automatically on every push. Evidence: green CI badge or pipeline run screenshot. |
| 14–17 | B (Good) | CI pipeline runs tests automatically on push. Covers at least unit tests and one other stage. Minor configuration issues but pipeline runs successfully. |
| 10–13 | C (Pass) | CI pipeline configured but only runs one test stage (e.g. only unit tests). Pipeline runs but no evidence of multi-stage execution. |
| 6–9 | D (Below Pass) | Pipeline configuration attempted but fails to run. Student understands the concept but cannot implement it. |
| 0–5 | F (Fail) | No CI/CD attempted. All testing done manually. No pipeline configuration file submitted. |

**Minimum acceptable GitHub Actions file (share as example):**

```yaml
# .github/workflows/test.yml
name: Run Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install dependencies
        run: npm install

      - name: Run unit tests
        run: npm test

      - name: Check coverage
        run: npm test -- --coverage --coverageThreshold='{"global":{"lines":70}}'
```

---

## Mini-Project Submission Checklist

Faculty use this checklist to verify all deliverables before marking.

| # | Deliverable | Present? | Marks Component |
|---|---|---|---|
| 1 | 15 black box test cases (EP + BVA documented) | ☐ | Criterion 1 |
| 2 | Coverage report screenshot (≥ 70%) | ☐ | Criterion 2 |
| 3 | 5 unit test files with assertions | ☐ | Criterion 3 |
| 4 | Postman collection exported (.json) | ☐ | Criterion 3 |
| 5 | 1 E2E test script (Selenium / Playwright / Cypress) | ☐ | Criterion 3 |
| 6 | Bug report for ≥ 3 bugs (structured format) | ☐ | Criterion 4 |
| 7 | Performance report (JMeter / k6 — 50 users) | ☐ | Criterion 3 |
| 8 | CI/CD pipeline config file (.yml) | ☐ | Criterion 5 |
| 9 | 1-page written summary (what broke and why) | ☐ | All criteria |

---

## Grade Boundaries

| Total Marks | Grade | Classification |
|---|---|---|
| 90–100 | O (Outstanding) | Exceptional industry-level quality |
| 80–89 | A+ (Excellent) | All criteria met at high standard |
| 70–79 | A (Very Good) | Most criteria met well |
| 60–69 | B+ (Good) | Solid understanding, minor gaps |
| 50–59 | B (Above Average) | Basic competency demonstrated |
| 40–49 | C (Pass) | Minimum standards met |
| Below 40 | F (Fail) | Resubmission required |

---

## Moderation Notes (For Faculty)

- If a student uses a different tech stack than expected, apply the rubric
  to the tools appropriate for that stack — do not penalise for stack choice
- Coverage below 70% should not automatically fail Criterion 2 if the
  student demonstrates understanding of why coverage is low
- Bug reports submitted without a fix still earn partial marks under Criterion 4
- CI/CD pipelines that fail to run but are correctly configured earn Criterion 5 C-grade

---

*Last updated: April 2026 | Institute 319 | CSE / AI Department*
