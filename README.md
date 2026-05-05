# GitHubSlideAwesomeness

Keynote Slidedeck Test - A GitHub Pages site for presenting Keynote slides.

## Setup

This repository is configured to deploy to GitHub Pages automatically when changes are pushed to the `main` branch.

### Step 1 — Enable GitHub Pages

1. Go to **Settings** → **Pages** in this repository
2. Under **Build and deployment**, select **GitHub Actions** as the source
3. Click **Save** — the deployment workflow will automatically publish your site on the next push

### Step 2 — Export Your Keynote Slides as HTML

1. Open your presentation in **Keynote** on macOS
2. Go to **File** → **Export To** → **HTML…**
3. Configure any options (e.g. enable "Include presenter notes" if needed)
4. Click **Next**, choose a destination folder on your Mac, and click **Export**
5. Keynote will create a folder containing an `index.html` file and a subfolder with all assets (images, scripts, CSS)

### Step 3 — Add the Exported Files to This Repository

**Option A — GitHub web UI (no git required)**

1. Open this repository in your browser
2. Click **Add file** → **Upload files**
3. Drag and drop **all** files and folders from your Keynote export folder
4. Make sure the target branch is `main`
5. Click **Commit changes**

**Option B — Command line**

```bash
# Clone the repo (if not already done)
git clone https://github.com/tolgabalci/GitHubSlideAwesomeness.git
cd GitHubSlideAwesomeness

# Copy all files from your Keynote export (replace the path below)
cp -r /path/to/your/KeynoteExport/* .

# Stage, commit, and push
git add .
git commit -m "Add Keynote HTML presentation"
git push origin main
```

> **Tip:** Make sure the main entry file from your Keynote export is named `index.html` — Keynote exports this by default, so you should be all set.

### Step 4 — Verify Deployment

After pushing, the GitHub Actions workflow will automatically deploy your site. Monitor progress under the **Actions** tab. Once complete, your presentation will be live at:

`https://tolgabalci.github.io/GitHubSlideAwesomeness/`
