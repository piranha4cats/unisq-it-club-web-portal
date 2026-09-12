### Step 1: Recommended Extensions (`.vscode/extensions.json`)

Create a `.vscode` folder in your repository root and add `extensions.json`. VS Code will prompt anyone opening the project repository to install these extensions with one click:

```json
{
  "recommendations": [
    "ritwickdey.liveserver",
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint"
  ]
}

```

* **Live Server (`ritwickdey.liveserver`):** Launches a local development server with live reload for your HTML/CSS/JS files.
* **Prettier (`esbenp.prettier-vscode`):** Auto-formats code on save to maintain uniform code style across the team.
* **ESLint (`dbaeumer.vscode-eslint`):** Catches syntax and logic errors in Vanilla JavaScript / Alpine.js scripts.



---

### Step 2: Workspace Settings (`.vscode/settings.json`)

Add `settings.json` in the `.vscode` directory to automatically enable format-on-save and map Prettier as the default formatter for your web files:

```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "liveServer.settings.donotShowInfoMsg": true,
  "liveServer.settings.port": 5500
}

```

---

### Step 3: Project Prettier Config (`.prettierrc`)

Create `.prettierrc` in the root of the project to set standardized formatting rules:

```json
{
  "semi": true,
  "singleQuote": false,
  "tabWidth": 2,
  "useTabs": false,
  "trailingComma": "es5",
  "printWidth": 100
}

```

Add a `.prettierignore` file to ensure build artifacts and dependencies are ignored:

```text
node_modules
.git
dist

```

---

### Step 4: Quick Launch Instructions for Team Members

* **Running the dev server:** Open any `.html` file (e.g., `index.html`) and click **"Go Live"** in the bottom status bar, or right-click the file and select **"Open with Live Server"**.
* **Formatting code:** Simply save the file (`Ctrl+S` / `Cmd+S`), and Prettier will format it according to `.prettierrc`.