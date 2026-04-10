# 🔧 Tool Setup Guide

**Software Testing Virtual Lab — B.Tech 6th Semester**
Institute 319 | CSE / AI Department

Install these tools once. They work for all six tech stacks covered in the lab.

---

## Quick Install (Copy-Paste Ready)

### Windows (PowerShell as Administrator)

```powershell
# 1. Node.js (includes npm)
winget install OpenJS.NodeJS

# 2. Python
winget install Python.Python.3.11

# 3. Git
winget install Git.Git

# 4. Jest (after Node is installed)
npm install -g jest

# 5. pytest + coverage
pip install pytest coverage httpx pytest-asyncio

# 6. Playwright
npm install -g @playwright/test
npx playwright install
```

### macOS (Terminal)

```bash
# Install Homebrew first if not present
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew install node python git
npm install -g jest @playwright/test
pip3 install pytest coverage httpx pytest-asyncio
npx playwright install
```

### Linux (Ubuntu / Debian)

```bash
sudo apt update
sudo apt install -y nodejs npm python3 python3-pip git
npm install -g jest @playwright/test
pip3 install pytest coverage httpx pytest-asyncio
npx playwright install
```

---

## Tool-by-Tool Setup

### Jest (JavaScript Unit Testing)

```bash
# In your project folder:
npm init -y
npm install --save-dev jest

# Add to package.json:
# "scripts": { "test": "jest", "test:coverage": "jest --coverage" }

# Run tests:
npm test
npm run test:coverage
```

### pytest (Python Unit Testing)

```bash
pip install pytest

# Run tests:
pytest                          # all tests
pytest test_auth.py             # specific file
pytest -v                       # verbose output
pytest --tb=short               # shorter tracebacks
```

### coverage.py (Python Code Coverage)

```bash
pip install coverage

# Run with coverage:
coverage run -m pytest
coverage report                 # terminal report
coverage report -m              # show missing lines
coverage html                   # open htmlcov/index.html in browser
```

### Cypress (E2E Testing — Web)

```bash
npm install --save-dev cypress

# Open interactive UI:
npx cypress open

# Run headless (for CI):
npx cypress run
```

### Playwright (Cross-browser E2E)

```bash
npm install --save-dev @playwright/test
npx playwright install           # downloads Chrome, Firefox, Safari

# Run tests:
npx playwright test
npx playwright test --headed     # see browser while running
npx playwright show-report       # view HTML report
```

### Postman (API Testing)

1. Download from https://postman.com/downloads
2. Install and open
3. Create a new Collection → add requests
4. Export collection as JSON for submission

**Newman (run Postman from terminal):**
```bash
npm install -g newman
newman run MyCollection.json -e environment.json
```

### Apache JMeter (Performance Testing)

1. Download from https://jmeter.apache.org/download_jmeter.cgi
2. Extract the zip / tar.gz
3. Run: `bin/jmeter` (GUI) or `bin/jmeter -n -t test.jmx -l results.jtl` (CLI)
4. Requires Java — install from https://adoptium.net

### k6 (Modern Load Testing)

```bash
# Windows (via Chocolatey):
choco install k6

# macOS:
brew install k6

# Linux:
sudo gpg --no-default-keyring --keyring /usr/share/keyrings/k6-archive-keyring.gpg --keyserver hkeys.openpgp.org --recv-keys C5AD17C747E3415A3642D57D77C6C491D6AC1D69
echo "deb [signed-by=/usr/share/keyrings/k6-archive-keyring.gpg] https://dl.k6.io/deb stable main" | sudo tee /etc/apt/sources.list.d/k6.list
sudo apt-get update && sudo apt-get install k6

# Run a test:
k6 run script.js
```

### OWASP ZAP (Security Testing)

1. Download from https://www.zaproxy.org/download/
2. Install and launch
3. Enter your app URL in the "Quick Start" tab
4. Click "Automated Scan"
5. View the Alerts panel for vulnerabilities found

### Flutter Test (Mobile Testing)

```bash
# Install Flutter SDK from https://flutter.dev/docs/get-started/install
# Then:
flutter pub get
flutter test                     # run all tests
flutter test --coverage          # with coverage
flutter test test/login_test.dart  # specific file
```

### Locust (Python Load Testing)

```bash
pip install locust

# Create locustfile.py, then:
locust -f locustfile.py
# Open browser at http://localhost:8089
# Enter number of users and host URL
# Click Start Swarming
```

---

## Verify Everything is Installed

Run this checklist in your terminal:

```bash
node --version       # should show v18+
npm --version        # should show 9+
python --version     # should show 3.10+
git --version        # any version
jest --version       # should show 29+
pytest --version     # should show 7+
k6 version           # any version
```

---

## Free Online Alternatives (No Install Needed)

| Tool | Online Version | Use For |
|---|---|---|
| DartPad | https://dartpad.dev | Run Flutter/Dart snippets |
| Replit | https://replit.com | Run Python/JS tests in browser |
| CodeSandbox | https://codesandbox.io | Full React/Node projects |
| Postman Web | https://web.postman.co | API testing without desktop install |
| GitHub Actions | https://github.com | CI/CD pipeline (free for public repos) |

---

## Troubleshooting Common Errors

| Error | Likely Cause | Fix |
|---|---|---|
| `jest: command not found` | Jest not installed globally | Run `npm install -g jest` |
| `ModuleNotFoundError: pytest` | pip installed to wrong Python | Use `python -m pytest` instead |
| `playwright: browser not found` | Browsers not downloaded | Run `npx playwright install` |
| `Permission denied` on macOS/Linux | Missing permissions | Add `sudo` before the command |
| `EACCES` npm error | npm global permissions issue | Run `npm config set prefix ~/.npm-global` |
| `python` not found on Windows | Python not in PATH | Reinstall Python, check "Add to PATH" box |

---

*Last updated: April 2026 | Institute 319*
