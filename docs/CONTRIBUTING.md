
# Contributing to the UniSQ IT Sandbox Club Web Portal

Thank you for contributing to the UniSQ IT Sandbox Club Web Portal! This guide will help you get your local environment set up, adhere to our team’s coding standards, and submit pull requests cleanly.

---

## 1. Development Environment Setup

We use **VS Code** as our primary editor to ensure consistent formatting and development workflows across the team.

### Recommended VS Code Extensions

When opening the repository in VS Code, install the recommended workspace extensions prompted in the lower right, or install them manually:

* **Live Server (`ritwickdey.liveserver`)**: Local preview server with live reload.


* **Prettier (`esbenp.prettier-vscode`)**: Automated code styling on save.


* **ESLint (`dbaeumer.vscode-eslint`)**: Syntax and error checking for JavaScript.

### Workspace Configuration

Ensure the `.vscode/` configurations are committed in your local clone:

* `.vscode/extensions.json`: Recommends required team plugins.
* `.vscode/settings.json`: Enforces format-on-save and sets Prettier as default.

---

## 2. Code Standards & Formatting

To maintain a uniform codebase across asynchronous contributors, formatting is standardized using **Prettier**.

* **Format on Save**: Saving any `.html`, `.css`, or `.js` file (`Ctrl+S` / `Cmd+S`) will automatically format according to the repository's `.prettierrc`.
* **Rules Summary**:
* 2 spaces indentation (no tabs)
* Double quotes (`"`) for HTML/JS
* Semicolons enabled
* 100-character line width



---

## 3. Running Locally

Because this project is built on lightweight static web technologies (HTML5, CSS3, Vanilla JavaScript), no build tools or local servers like Python/Node runtimes are strictly required.

1. Open the repository root folder in VS Code.
2. Open any `.html` entry file (e.g., `index.html`).


3. Click **"Go Live"** in the bottom status bar, or right-click `index.html` and select **"Open with Live Server"**.
4. The site will launch at `[http://127.0.0.1:5500/](http://127.0.0.1:5500/)`. Any changes you save will auto-refresh the browser.

---

## 4. Branching & Contribution Workflow

We follow an issue-driven branch workflow to make tasks manageable for busy study schedules:

1. **Pick an Issue**: Assign yourself to an open GitHub Issue on the project board before starting work.


2. **Create a Feature Branch**:
```bash
git checkout main
git pull origin main
git checkout -b feature/issue-<number>-short-description

```


3. **Commit Messages**: Keep commit messages clear and concise:
```bash
git commit -m "Add responsive hero section to index.html (#12)"

```


4. **Push and Open a Pull Request**:
```bash
git push origin feature/issue-<number>-short-description

```


5. Open a Pull Request targeting `main` and reference the Issue number (e.g., `Closes #12`). Request a review from the Project Lead or a teammate before merging.



---

## 5. Domain Restrictions & Auth Policy

Any modifications to member-only sections or authentication routines must enforce the **`@umail.usq.edu.au`** institutional email domain restriction. Never disable or bypass this validation logic in production or staging branches.