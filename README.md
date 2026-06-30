# 100Hires Portfolio Project — Setup & Process Log

**Candidate:** Guntur Satria  
**Repository:** [100Hires-Guntur-Satria-Application](https://github.com/project-klik/100Hires-Guntur-Satria-Application)  
**Task:** First step of the 100Hires portfolio process — install tools, create a public GitHub repository, and document the setup.

---

## Tools Installed

| Tool | Purpose | How I installed it |
|------|---------|-------------------|
| **Cursor IDE** | AI-assisted code editor used to open the repo, edit files, and run Git operations | Downloaded from [cursor.com](https://cursor.com/) and installed on my machine |
| **Claude Code** (Cursor extension) | AI coding assistant inside Cursor | Opened Cursor → **Extensions** → searched **"Claude Code"** → installed → signed in |
| **Codex** (Cursor extension) | Additional AI coding assistant inside Cursor | Opened Cursor → **Extensions** → searched **"Codex"** → installed → signed in |
| **Git** | Version control — clone, pull, commit, and push to GitHub | Already available on my system (used from Cursor's terminal and Source Control panel) |
| **GitHub account** | Host the public repository | Created / signed in at [github.com](https://github.com/) |

---

## Steps Completed

### 1. Install Cursor and extensions

1. Installed **Cursor IDE** from the official website.
2. Opened Cursor and went to **Extensions** (sidebar or `Ctrl+Shift+X`).
3. Installed and logged in to **Claude Code**.
4. Installed and logged in to **Codex**.

### 2. Create a public GitHub repository

1. Signed in to GitHub.
2. Created a new **public** repository named `100Hires-Guntur-Satria-Application`.
3. Initialized it with a basic README (optional initial commit).

### 3. Clone the repository to my computer

Before opening the project in Cursor, I **cloned the repository locally** so Git and the IDE work on a full copy of the repo on my PC:

```bash
git clone https://github.com/project-klik/100Hires-Guntur-Satria-Application.git
cd 100Hires-Guntur-Satria-Application
```

This step is important: Cursor needs a local Git repository folder, not just a single file opened in isolation.

### 4. Authenticate Cursor / Git with GitHub (Personal Access Token)

When connecting Cursor to GitHub, I had to **enter credentials first** so the IDE could access the remote repository (pull and push).

GitHub no longer accepts account passwords for Git over HTTPS. I used a **Personal Access Token (PAT)** instead:

1. On GitHub: **Settings** → **Developer settings** → **Personal access tokens** → **Tokens (classic)** or **Fine-grained tokens**.
2. Generated a new token with at least **`repo`** scope (read/write access to repositories).
3. When Cursor or Git prompted for credentials:
   - **Username:** my GitHub username  
   - **Password:** pasted the **token** (not my GitHub account password)

After this, Cursor could authenticate with GitHub for clone, pull, and push operations.

### 5. Open the cloned repository in Cursor

1. In Cursor: **File → Open Folder**.
2. Selected the cloned folder: `100Hires-Guntur-Satria-Application`.
3. Confirmed the Source Control view showed the Git repository connected to `origin`.

### 6. Workflow inside Cursor: Pull → Edit → Push

This is the workflow I used in the IDE:

#### Step A — Pull latest changes from GitHub

Before editing, I synced with the remote so my local copy was up to date:

- **Source Control** panel → **Sync / Pull**, or  
- Terminal:

```bash
git pull origin main
```

*(Use `master` instead of `main` if that is your default branch.)*

#### Step B — Edit README.md using the Cursor agent

1. Opened `README.md` in Cursor.
2. Used the **Cursor Agent** (AI chat) to draft and refine this document.
3. Described what I installed, what I did, and any problems I hit — as requested in the recruiter email.
4. Reviewed the generated content and adjusted wording so it accurately reflected my experience.

#### Step C — Commit and push to GitHub

1. Staged the updated file:

```bash
git add README.md
```

2. Committed with a clear message:

```bash
git commit -m "Document setup process, tools installed, and issues resolved"
```

3. Pushed to GitHub:

```bash
git push origin main
```

4. Verified on GitHub that `README.md` updated in the browser.

---

## Issues I Ran Into (and How I Solved Them)

### Issue 1: Cursor could not access the GitHub repository without credentials

**Problem:** Opening or syncing the repo failed until GitHub authentication was configured. Git asked for a username and password, and plain account passwords did not work.

**Solution:** Created a **GitHub Personal Access Token** and used it as the password when prompted. Stored credentials via Git credential helper (or re-entered when needed) so pull/push worked from Cursor.

### Issue 2: Repository had to be cloned locally first

**Problem:** Trying to work without a local clone made Git operations unclear — there was no `.git` folder and no link to `origin`.

**Solution:** Cloned the repository with `git clone`, then opened **that folder** in Cursor. After that, Source Control, pull, commit, and push all worked as expected.

### Issue 3: Pull before edit to avoid conflicts

**Problem:** If the remote changed (e.g., initial README on GitHub), pushing without pulling first could cause rejections or merge conflicts.

**Solution:** Always ran **`git pull`** before editing and pushing, so local and remote stayed in sync.

### Issue 4: Learning extensions and AI tools for the first time

**Problem:** First time installing Claude Code and Codex inside Cursor — unsure where extensions live and how login works.

**Solution:** Followed the recruiter’s hint: searched YouTube and Cursor docs for “install Cursor extensions” and “Claude Code Cursor”. Used **Extensions** search inside Cursor and signed in when each extension prompted.

---

## Summary

| Requirement (from email) | Status |
|------------------------|--------|
| Install Cursor IDE | Done |
| Install & log in to Claude Code | Done |
| Install & log in to Codex | Done |
| Create public GitHub repository | Done |
| Open repository in Cursor | Done (after local clone + token auth) |
| README: tools, steps, issues | Done (this file) |
| Commit and push to GitHub | Done |
| Reply to email with README link | Pending — link below |

**Direct link to this README on GitHub:**  
https://github.com/project-klik/100Hires-Guntur-Satria-Application/blob/main/README.md

---

## What I Learned

- Setting up a dev environment is not only installing an IDE — **Git auth** and **cloning the repo locally** are essential.
- **Personal Access Tokens** are the standard way to connect Git clients (including Cursor) to GitHub over HTTPS.
- A practical Git workflow: **pull → edit (with AI assistance) → commit → push**.
- Reading docs and tutorials when stuck is part of the process — exactly what this step is designed to evaluate.

---

*Submitted as part of the 100Hires portfolio project — Step 1.*
