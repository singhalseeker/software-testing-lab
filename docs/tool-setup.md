# Tool Setup Guide — Software Testing Lab

## Prerequisites

Before starting the lab, ensure you have the following installed:

| Tool | Version | Purpose |
|------|---------|---------|
| Node.js | 18+ | JavaScript runtime |
| npm | 9+ | Package manager |
| Git | 2.40+ | Version control |
| VS Code | Latest | Code editor |

---

## Installation Steps

### 1. Install Node.js

Download from [nodejs.org](https://nodejs.org) and install the LTS version.

Verify installation:
```bash
node --version
npm --version
```

### 2. Install Git

Download from [git-scm.com](https://git-scm.com) and follow the installer.

Verify installation:
```bash
git --version
```

### 3. Clone the Repository

```bash
git clone https://github.com/singhalseeker/software-testing-lab
cd software-testing-lab
```

### 4. Install Dependencies

```bash
npm install
```

### 5. Run Tests

```bash
npm test
```

---

## VS Code Extensions (Recommended)

Install these extensions for the best experience:

- **ESLint** — JavaScript linting
- **Prettier** — Code formatting
- **GitLens** — Enhanced Git integration
- **Jest Runner** — Run tests inline

To install via command line:
```bash
code --install-extension dbaeumer.vscode-eslint
code --install-extension esbenp.prettier-vscode
code --install-extension eamodio.gitlens
code --install-extension firsttris.vscode-jest-runner
```

---

## GitHub Setup

1. Create a free account at [github.com](https://github.com)
2. Configure your identity locally:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
3. Generate an SSH key (optional but recommended):
```bash
ssh-keygen -t ed25519 -C "you@example.com"
```

---

## Troubleshooting

**Tests not running?**
- Ensure Node.js 18+ is installed
- Run `npm install` again

**Git push rejected?**
- Check you have write access to the repository
- Ensure you're on the correct branch

**VS Code not detecting Jest?**
- Open the project folder (not a parent folder) in VS Code
- Ensure `node_modules` is present
