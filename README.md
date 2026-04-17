# PS-Acq-Claude-Code-Test
# 🤖 Team Claude Projects

A shared space for our team to build and showcase personal projects created with Claude. No collaborator access needed — just fork, build, and submit a PR!

---

## 📋 Table of Contents

- [Getting Started](#getting-started)
- [Project Directory Naming Convention](#project-directory-naming-convention)
- [How to Fork & Submit a Pull Request](#how-to-fork--submit-a-pull-request)
- [Project Structure](#project-structure)
- [Guidelines](#guidelines)

---

## Getting Started

Before you begin, make sure you have:

- A [GitHub account](https://github.com)
- [Git](https://git-scm.com/downloads) installed on your machine
- Access to [Claude](https://claude.ai) or the [Anthropic API](https://console.anthropic.com)

---

## Project Directory Naming Convention

Each project lives in its own directory at the root of this repository. To keep things organized and make it easy to see who built what, all project directories must follow this naming scheme:

```
[firstname-lastname]_[short-project-name]
```

### Rules

- Use **lowercase only**
- Separate your name from the project name with an **underscore** (`_`)
- Use **hyphens** (`-`) within your name and within the project name (no spaces)
- Keep the project name short but descriptive (2–4 words max)

### Examples

| Author | Project | Directory Name |
|---|---|---|
| Jane Smith | Resume Builder | `jane-smith_resume-builder` |
| Alex Johnson | Slack Summarizer | `alex-johnson_slack-summarizer` |
| Maria Garcia | Recipe Generator | `maria-garcia_recipe-generator` |
| Tom Lee | Code Reviewer | `tom-lee_code-reviewer` |

> **Tip:** If you have a common name and aren't sure if there's a collision, check the existing directories before creating yours.

---

## How to Fork & Submit a Pull Request

Follow these steps to add your project to the repository without needing collaborator access.

### Step 1 — Fork the Repository

1. Navigate to the main repository page on GitHub.
2. Click the **Fork** button in the top-right corner of the page.
3. Select your personal GitHub account as the destination for the fork.

GitHub will create a copy of the repository under your account (e.g., `your-username/team-claude-projects`).

### Step 2 — Clone Your Fork Locally

```bash
git clone https://github.com/YOUR-USERNAME/REPO-NAME.git
cd REPO-NAME
```

### Step 3 — Create a Branch for Your Project

Always work on a dedicated branch — never commit directly to `main`.

```bash
git checkout -b add/jane-smith_resume-builder
```

Use the format `add/[your-directory-name]` for your branch name.

### Step 4 — Create Your Project Directory

Inside the repository root, create a new directory following the [naming convention](#project-directory-naming-convention) above.

```bash
mkdir jane-smith_resume-builder
cd jane-smith_resume-builder
```

Add your project files and a `README.md` describing what your project does (see [Project Structure](#project-structure) below).

### Step 5 — Commit and Push Your Changes

```bash
git add .
git commit -m "Add jane-smith_resume-builder"
git push origin add/jane-smith_resume-builder
```

### Step 6 — Open a Pull Request

1. Go to **your fork** on GitHub.
2. You'll see a banner prompting you to **Compare & pull request** — click it. (If you don't see it, go to the **Pull requests** tab and click **New pull request**.)
3. Make sure the base repository is set to the **original team repo** and the base branch is `main`.
4. Give your PR a clear title, e.g.: `Add: Jane Smith – Resume Builder`
5. Fill in a brief description of your project and click **Create pull request**.

A maintainer will review and merge your PR. 🎉

### Keeping Your Fork Up to Date

If time has passed since you forked, sync your fork with the original repo before starting new work:

```bash
# Add the original repo as a remote (one-time setup)
git remote add upstream https://github.com/ORG-OR-USERNAME/REPO-NAME.git

# Fetch and merge the latest changes
git fetch upstream
git checkout main
git merge upstream/main

# Push the updated main to your fork
git push origin main
```

---

## Project Structure

Each project directory should contain at minimum:

```
your-name_project-name/
├── README.md          # Required — describes your project
└── ...                # Your project files
```

### Project README Template

Use this template for your project's `README.md`:

```markdown
# Project Name

**Author:** Your Name
**Date:** YYYY-MM-DD

## What It Does
A short description of what your project does.

## How to Run
Step-by-step instructions to run or use the project locally.

## How Claude Was Used
Describe how you used Claude to build this — prompts, API usage, workflow, etc.

## Notes
Anything else worth sharing — limitations, future ideas, etc.
```

---

## Guidelines

- **One directory per project.** Don't add multiple projects in a single PR.
- **Keep projects self-contained.** All files for your project should live inside your project directory.
- **No sensitive data.** Do not commit API keys, passwords, or personal information. Use `.env` files and add them to `.gitignore`.
- **Be a good reviewer.** You're encouraged to leave constructive comments on teammates' PRs.
- **Have fun.** This is a space to experiment and learn — share what you're building!
