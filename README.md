# 🧪 Software Testing Virtual Lab
### B.Tech 6th Semester — Software Engineering | Institute 319

An interactive, browser-based learning environment where engineering students
can explore, compare, and practise software testing strategies across six
real-world technology stacks — with no installation required.

---

## 🌐 Live Demo

| Resource | Link |
|---|---|
| 🖥 Virtual Lab | https://singhalseeker.github.io/software-testing-lab |
| 🃏 Flashcards (28 concepts) | https://singhalseeker.github.io/software-testing-lab/flashcards |


---

## 📸 What It Covers

```
Virtual Lab
├── Part 1 — Project Dashboard     (4 sample projects to choose from)
├── Part 2 — Methodology           (step-by-step workflow per tech stack)
├── Part 3 — Test Pyramid          (visual + failure vs success scenarios)
├── Part 4 — Tool Mapping Table    (24 rows: stack × type × tool × workflow)
├── Part 5 — Hands-on Lab          (4 guided exercises with expected answers)
└── Part 6 — Teacher Guide         (4 delivery formats + assessment rubric)

Flashcards
└── 28 concepts — Browse Mode + Quiz Mode + Category Filter
```

---

## 🛠 Tech Stacks Covered

| Stack | Tools Demonstrated |
|---|---|
| 🟢 MERN Stack | Jest, Supertest, Cypress, React Testing Library, MongoDB Memory Server |
| 🔵 React Frontend | Jest, RTL, Playwright, Storybook, axe-core, MSW |
| 🟣 Flutter Mobile | flutter_test, integration_test, mockito, golden_toolkit, Firebase Test Lab |
| 🟡 Python Backend | pytest, httpx, Locust, Bandit, coverage.py, Factory Boy |
| 🟤 JS Full Stack | Vitest, Playwright, Prisma test DB, Lighthouse CI |
| 🔴 REST APIs | Postman/Newman, k6, OWASP ZAP, Pact, Chaos Monkey |

---

## 🎓 For Students

### How to use this lab

1. Open the [Live Lab](https://singhalseeker.github.io/software-testing-lab) — no login, no install
2. Select a **project** (E-Commerce, Chat App, Student Portal, Trek API)
3. Select your **tech stack** (MERN, React, Flutter, Python, JS Full Stack, REST API)
4. Read the testing strategy, study the code example
5. Switch to **Hands-on Lab** tab and complete all 4 exercises in order
6. Use the **Flashcards** to revise all 28 concepts before your exam

### Exercise progression

| Exercise | Skill | Difficulty |
|---|---|---|
| Ex 1 — Introduce a Bug | Understanding what tests catch | Beginner |
| Ex 2 — Select Strategy | Choosing the right test type | Intermediate |
| Ex 3 — Analyze Failures | Reading and diagnosing test output | Intermediate |
| Ex 4 — Fix and Retest | Fixing code + achieving coverage | Advanced |

### Deliverables for mini-project submission

- [ ] 15 black box test cases (EP + BVA)
- [ ] White box coverage report ≥ 70%
- [ ] 5 unit tests using pytest or Jest
- [ ] Postman collection — 8 API tests
- [ ] 1 Selenium / Playwright E2E script
- [ ] Alpha test bug report (minimum 3 bugs)
- [ ] JMeter / k6 performance report — 50 concurrent users
- [ ] 1-page summary: what broke and why

---

## 👨‍🏫 For Faculty

See the full documentation in the `docs/` folder:

| Document | Purpose |
|---|---|
| [Teaching Guide](docs/teaching-guide.md) | 4 delivery formats with step-by-step plans |
| [Assessment Rubric](docs/assessment-rubric.md) | 100-mark rubric with grade descriptors |
| [Tool Setup Guide](docs/tool-setup.md) | Installation instructions for every tool |

### Quick delivery formats

| Format | Duration | Mode |
|---|---|---|
| Classroom Demo | 90 min | Lecturer-led, projector |
| Workshop Activity | 3 hours | Groups of 4 students |
| Mini Hackathon | Full day (6–8 hrs) | Competitive teams |
| Lab Experiment | 2 hours | Individual assessment |

---

## 📦 Run Locally (Offline Use)

```bash
# Clone the repo
git clone https://github.com/singhalseeker/software-testing-lab.git

# Open in browser — no build step, no server needed
cd software-testing-lab
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

The entire lab is plain HTML + JavaScript. It works offline once downloaded.

---

## 🗂 Repo Structure

```
software-testing-lab/
│
├── index.html                    ← Main virtual lab (all 6 parts)
├── flashcards/
│   └── index.html                ← 28-concept flashcard deck
│
├── exercises/                    ← Standalone exercise files
│   ├── ex1-introduce-bug.js
│   ├── ex2-select-strategy.md
│   ├── ex3-analyze-failures.md
│   └── ex4-fix-and-retest.js
│
├── sample-projects/              ← Broken codebases for students
│   ├── mern-auth-broken/
│   ├── python-api-broken/
│   └── react-form-broken/
│
├── docs/
│   ├── teaching-guide.md
│   ├── assessment-rubric.md
│   └── tool-setup.md
│
├── .github/
│   └── ISSUE_TEMPLATE/
│       └── bug-report.md
│
├── CONTRIBUTING.md
├── LICENSE                       ← MIT
└── README.md                     ← This file
```

---

## 🤝 Contributing

Contributions from faculty and students are welcome.

- Found a bug in an exercise? [Open an Issue](../../issues/new)
- Want to add a new tech stack? See [CONTRIBUTING.md](CONTRIBUTING.md)
- Want to improve the flashcards? Edit `flashcards/index.html` and raise a PR

Please follow the existing code style and test any HTML changes in both
light and dark mode before submitting.

---

## 📅 Semester Versioning

Each semester's stable version is tagged for permanent reference:

```bash
# Faculty: tag at the start of each semester
git tag -a "2025-odd-sem" -m "B.Tech CSE 6th Sem — Odd Semester 2025"
git push origin --tags
```

Students can always access their semester's exact version via GitHub Releases.

---

## 📄 License

MIT License — free to use, share, and modify for educational purposes.
See [LICENSE](LICENSE) for full terms.

---

## 👤 Author

**Prateek Agarwal**
Assistant Professor — CSE / AI Department
Institute AKTU 319 | Bareilly, Uttar Pradesh

---

*Built for engineering students who deserve industry-grade learning tools.*
