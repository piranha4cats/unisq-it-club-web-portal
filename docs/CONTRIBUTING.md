# 🚀 UniSQ IT Sandbox Web Portal: How to Contribute

Welcome to the build! Since we all have different levels of experience with Git and GitHub, we are keeping our workflow simple, safe, and collaborative. Whether you are an experienced developer or learning Git for the first time, this guide will walk you through setting up your environment, following our standards, and contributing safely.

---

## 1. The Core Concepts & Our Golden Rule

To keep collaboration smooth and protect the project, we follow a simple branching model:

* **The Repository (Repo)**: This is our shared folder hosted on GitHub (`unisq-it-club-web-portal` / `piranha4cats/unisq-it-club-web-portal`). It holds all our HTML, CSS, JavaScript, and project files.
* **The `main` Branch**: This is the "live" version of our website. 
  * **Our Golden Rule**: We never save (commit) or push code directly to the `main` branch. It is protected. Everything goes through a "Pull Request" (PR) so we can review it together and learn from each other's code.
* **Feature Branches**: Think of this as your personal sandbox. When you want to build something, you create a copy of `main` (a branch), do your work there, and test it safely without breaking the live site.
* **Pull Requests (PR)**: When your branch is finished, you submit a PR. This is simply you asking the team: *"Here is my code, can someone review it and merge it into the main project?"*

---

## 2. Initial Setup (Do this once)

### Step 1: Accept the Invite & Clone the Repo
First, check your email or GitHub notifications and accept the repository invitation. Once you are in, open your terminal (or VS Code) and download the code to your machine:

```bash
git clone https://github.com/piranha4cats/unisq-it-club-web-portal.git
cd unisq-it-club-web-portal
```

### Step 2: Configure Primary Development Tools (VS Code)

We use **VS Code** as our primary editor to ensure consistent formatting and workflows across the team. When you open the project folder in VS Code, install the recommended extensions when prompted, or install them manually:

* **Live Server (`ritwickdey.liveserver`)**: Launches a local preview server with instant hot-reloading.
* **Prettier (`esbenp.prettier-vscode`)**: Formats code automatically on save.
* **ESLint (`dbaeumer.vscode-eslint`)**: Detects syntax errors and issues in JavaScript.

Ensure the workspace configuration files inside `.vscode/` remain present:

* `.vscode/extensions.json`: Recommends workspace extensions for team members.
* `.vscode/settings.json`: Configures auto format-on-save using Prettier.

---

## 3. Code Standards & Formatting

Formatting is standardized across asynchronous contributors via **Prettier** to avoid formatting conflicts:

* **Format on Save**: Saving any `.html`, `.css`, or `.js` file (`Ctrl+S` / `Cmd+S`) automatically formats your code.
* **Rules Summary**:
    * 2 spaces indentation (no tabs)
    * Double quotes (`"`) for HTML/JS
    * Semicolons enabled
    * 100-character line width

---

## 4. Running Locally

Because this project is built on lightweight static web technologies (HTML5, CSS3, Vanilla JavaScript), no build tools or local servers like Python/Node runtimes are strictly required.

1. Open the repository root folder in VS Code.
2. Open any `.html` entry file (e.g., `index.html`).
3. Click **"Go Live"** in the bottom status bar, or right-click `index.html` and select **"Open with Live Server"**.
4. The site will launch at `http://127.0.0.1:5500/` and auto-refresh as you edit and save files.
---

## 5. The Daily Workflow (Step-by-Step)

Whenever you sit down for your 2–4 hours of weekly project work, follow this exact loop for claiming a task and writing code:

### Step 1: Claim an Issue on the Sprint Board

1. Go to the **Projects** tab in our GitHub repository and open the **Web Portal Sprint Board**.
2. Pick an open task from the **To Do** column (e.g., *"Draft Header HTML"* or *"Create CSS Variables"*).

3. Assign yourself to the task and drag the card into the **In Progress** column so the team knows you are on it.

### Step 2: Get the Latest Updates

Before you start coding, always make sure your local computer has the newest code from the rest of the team:

```bash
git switch main
git pull origin main
```

### Step 3: Create Your Feature Branch

Before you write any code, create an isolated sandbox for your work. Name the branch clearly based on what you are building:

```bash
git switch -c feature/your-task-name
# Example: git switch -c feature/navbar-html
# Example: git switch -c feature/issue-12-navbar-html
```

### Step 4: Write Code & Commit

Work your magic in VS Code! For Weeks 1–2, we are focusing purely on base HTML, CSS templates, and wireframe setups. As you finish small pieces (like finishing the HTML layout, or adding CSS colors), save a snapshot of your progress:

```bash
git add .
git commit -m "Added base HTML structure for the navigation bar (#12)"
```

### Step 5: Push to GitHub

Send your branch up to the repository so the rest of the team can see your work:

```bash
git push -u origin feature/your-task-name
```

### Step 6: Open a Pull Request (PR)

1. Go to the repository in your web browser. You will see a green button that says **Compare & pull request**—click it!
2. Add a brief description of what you built.
3. On the right-hand menu, link your PR to our **Web Portal Sprint Board** and reference the Issue number (e.g., `Closes #12`).
4. Click **Create pull request**.
5. Another team member will review your code, approve it, and merge it into the main project! Once merged, drag your task to the **Done** column.

---

## 6. Domain Restrictions & Auth Policy

Any modifications to member-only sections or authentication routines must enforce the **`@umail.usq.edu.au`** institutional email domain restriction. Never disable or bypass this validation logic in production, staging, or pull requests.

---

## 7. Quick Troubleshooting

* **"I'm stuck in Vim/a weird text screen in the terminal!"**
Type `:wq` and press `Enter` to save and exit.
* **"Git says I have uncommitted changes and won't let me switch branches!"**
Either commit your current work (`git commit`), or stash it away temporarily with `git stash` (you can reapply it later using `git stash pop`).