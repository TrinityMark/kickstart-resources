# KickStart Resources — Setup and User Guide

## What This Tool Does

KickStart Resources is a web-based reference app that gives Kickstart program participants instant access to 20 Success Stack examples. Each example shows a complete Success Stack — an identity statement, a SMART goal, an X-Goal, and two Keystone Habits with supporting Daily Actions — covering both business and personal themes.

Users browse the sidebar, pick the example that resonates most, and see the full stack displayed in a clear, structured layout. The app is fully responsive and works on desktop, tablet, and mobile.

**Built by:** Mark Nixey, Trinity Advisory — mark.nixey@trinityadvisory.com.au

---

## Who This Is For

Participants in the Trinity Advisory Kickstart coaching program who want to explore Success Stack examples online and find one that fits their current focus.

---

## How to Use the App

1. Open the app URL in any modern web browser (Chrome, Safari, Edge, Firefox).
2. The left sidebar lists all 20 examples grouped by **Business** and **Personal**.
3. Click any example to display its full Success Stack in the main content area.
4. On mobile, tap the **☰** menu icon (top left) to open the example list, then tap any item to view it.
5. Scroll down to read the Keystone Habits and Daily Actions at the bottom of each stack.

---

## Deploying to GitHub Pages

### Step 1 — Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in.
2. Click **New repository**.
3. Give it a name (e.g. `kickstart-resources`).
4. Set it to **Public** (required for free GitHub Pages hosting).
5. Click **Create repository**.

### Step 2 — Upload the files
1. In your new repository, click **Add file → Upload files**.
2. Drag in `index.html` and the entire `docs/` folder.
3. Click **Commit changes**.

### Step 3 — Enable GitHub Pages
1. In the repository, go to **Settings → Pages**.
2. Under **Source**, select **Deploy from a branch**.
3. Set branch to **main** and folder to **/ (root)**.
4. Click **Save**.
5. Wait 1–2 minutes. Your app will be live at:
   `https://[your-username].github.io/[repository-name]/`

### Alternatively — deploy with the GitHub CLI
```
git init
git add .
git commit -m "Initial deploy"
git branch -M main
git remote add origin https://github.com/[username]/[repo-name].git
git push -u origin main
```
Then enable Pages in Settings as above.

---

## How to Add or Edit Examples

All content lives in the `EXAMPLES` array inside `index.html`. No build tools or server is needed — just edit the file and push/re-upload.

### To edit an existing example:
1. Open `index.html` in any text editor (Notepad, VS Code, etc.).
2. Find the example by searching for its title (e.g. `'Financial Control'`).
3. Update the relevant fields: `iAmStatement`, `smartGoal`, `xGoal`, habit text, or daily actions.
4. Save the file and re-upload or push to GitHub.

### To add a new example:
1. Copy an existing object from the `EXAMPLES` array.
2. Add it to the array with a new `id`, `num`, `category`, and content.
3. Set `category` to either `'business'` or `'personal'`.
4. Save and redeploy.

---

## Troubleshooting

| Problem | Likely cause | Fix |
|---|---|---|
| Sidebar not visible on desktop | Browser window too narrow | Widen the browser window to at least 768px |
| App shows blank page | File served from wrong location | Ensure `index.html` is at the repository root, not inside a subfolder |
| Fonts look different / plain | Google Fonts blocked or offline | Fonts fall back to system sans-serif — this is expected behaviour offline |
| GitHub Pages URL returns 404 | Pages not yet enabled, or recently pushed | Wait 2–3 minutes after enabling Pages or pushing a change |
| Content looks squashed on mobile | Old browser | Use a modern browser (Chrome, Safari 14+, Edge) |

---

## Building From Source (Developers)

There is no build process. The entire app is a single `index.html` file with inline CSS and JavaScript. Open it directly in a browser for local development:

```
# macOS / Linux
open index.html

# Windows
start index.html
```

Or run a simple local server:
```
npx serve .
# then open http://localhost:3000
```

No dependencies, no npm install, no compilation step required.
