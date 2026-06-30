# 100Hires Portfolio Project — Setup & Process Log

**Candidate:** Guntur Satria  
**Task:** First step of the 100Hires portfolio process — install tools, create a public GitHub repository, and document the setup.

Overall, the process went **very smoothly**. Each step built naturally on the previous one, and once the initial setup was done, working inside Cursor felt straightforward.

---

## Tools Installed

| Tool | Purpose | How I installed it |
|------|---------|-------------------|
| **Cursor IDE** | AI-assisted code editor to open the repo, edit files, and run Git operations | Downloaded from [cursor.com](https://cursor.com/) and installed on my machine |
| **Claude Code** (Cursor extension) | AI coding assistant inside Cursor | Cursor → **Extensions** → searched **"Claude Code"** → installed → signed in |
| **Codex** (Cursor extension) | Additional AI coding assistant inside Cursor | Cursor → **Extensions** → searched **"Codex"** → installed → signed in |
| **Git** | Version control — clone, pull, commit, and push | Already available on my system (used from Cursor's terminal and Source Control panel) |
| **GitHub account** | Host the public repository | Signed in at [github.com](https://github.com/) |

---

## Steps Completed

### 1. Install Cursor and extensions

1. Installed **Cursor IDE** from the official website.
2. Opened **Extensions** in Cursor (`Ctrl+Shift+X`).
3. Installed and logged in to **Claude Code**.
4. Installed and logged in to **Codex**.

All extensions installed without issues and were ready to use within a few minutes.

### 2. Create a public GitHub repository

1. Signed in to GitHub.
2. Created a new **public** repository named `100Hires-Guntur-Satria-Application`.
3. Added a basic initial README commit on GitHub.

### 3. Clone the repository to my computer

Before opening the project in Cursor, I **cloned the repository locally** so Git and the IDE had a full working copy on my PC:

```bash
git clone <repository-url>
cd 100Hires-Guntur-Satria-Application
```

This was a quick step and set everything up correctly for the rest of the workflow.

### 4. Authenticate Cursor / Git with GitHub

To connect Cursor to GitHub, I entered my credentials once so the IDE could pull from and push to the remote repository.

GitHub uses a **Personal Access Token (PAT)** instead of an account password for Git over HTTPS:

1. On GitHub: **Settings** → **Developer settings** → **Personal access tokens**.
2. Generated a token with **`repo`** scope (read/write access).
3. When prompted by Cursor or Git:
   - **Username:** my GitHub username
   - **Password:** the **token**

After that one-time setup, authentication worked smoothly for all Git operations.

### 5. Open the cloned repository in Cursor

1. **File → Open Folder** in Cursor.
2. Selected the cloned `100Hires-Guntur-Satria-Application` folder.
3. Confirmed the Source Control panel showed the repo connected to `origin`.

### 6. Workflow inside Cursor: Pull → Edit → Push

This was the main day-to-day workflow in the IDE — simple and repeatable:

#### Step A — Pull latest changes from GitHub

Synced with the remote before editing:

```bash
git pull origin main
```

#### Step B — Edit README.md using the Cursor Agent

1. Opened `README.md` in Cursor.
2. Used the **Cursor Agent** to draft and refine this document.
3. Reviewed the output and adjusted it to match what I actually did.

The agent made writing the README fast and easy — I described the process and it helped structure the content clearly.

#### Step C — Commit and push to GitHub

```bash
git add README.md
git commit -m "Document setup process, tools installed, and issues resolved"
git push origin main
```

Pull → edit with the agent → commit → push. The full cycle completed without friction.

---

## Notes Along the Way

The process was smooth overall. A few small things worth mentioning:

### GitHub authentication (one-time setup)

Before the first push, I needed to set up a **Personal Access Token** so Git could talk to GitHub over HTTPS. Once configured, pull and push worked reliably from Cursor.

### Clone before opening in Cursor

Working from a **local clone** (not just a single file) made Git operations clear — Source Control, pull, commit, and push all behaved as expected.

### Pull before editing

Running **`git pull`** before making changes kept my local copy in sync with GitHub and avoided unnecessary conflicts.

### First time with Cursor extensions

Installing **Claude Code** and **Codex** was my first time using them. The Extensions panel in Cursor made it easy — search, install, sign in, and they were ready to use.

---

## Summary

| Requirement (from email) | Status |
|--------------------------|--------|
| Install Cursor IDE | Done |
| Install & log in to Claude Code | Done |
| Install & log in to Codex | Done |
| Create public GitHub repository | Done |
| Open repository in Cursor | Done |
| README: tools, steps, issues | Done (this file) |
| Commit and push to GitHub | Done |

---

## What I Learned

- The setup flow is logical: **install tools → create repo → clone → authenticate → open in Cursor**.
- A **Personal Access Token** is the standard way to connect Git (and Cursor) to GitHub.
- The day-to-day workflow is simple: **pull → edit (with AI assistance) → commit → push**.
- Using Cursor Agent to help write this README made documenting the process quick and smooth.

---

*Submitted as part of the 100Hires portfolio project — Step 1.*
