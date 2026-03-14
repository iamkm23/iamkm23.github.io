# Step-by-Step GitHub Deployment Guide

Follow these steps from your terminal inside the root `asciidoc` folder.

### 1. Initialize and Commit (Local)

If you haven't already:

```bash
# Go to root
cd /Users/kyawmyooo/Desktop/asciidoc

# Initialize git
git init

# Add all required files (.github folder, .gitignore, engineering-docs folder)
git add .

# Create the initial commit
git commit -m "chore: initial setup for multi-site docs"
```

### 2. Connect to GitHub

Replace `YOUR_URL` with your actual repo link if different:

```bash
# Add your remote
git remote add origin https://github.com/iamkm23/iamkm23.github.io.git

# Push to main
git push -u origin main
```

### 3. Check GitHub Actions

1. Open your repo on GitHub.
2. Click the **Actions** tab.
3. You should see a workflow named **"Deploy to GitHub Pages"** running.
4. Wait for it to finish (Green checkmark).

### 4. Configure GitHub Pages Settings (One-time setup)

Once the workflow finishes for the first time, it will create a new branch called `gh-pages`.

1. Go to **Settings** -> **Pages**.
2. Under **Build and deployment** -> **Branch**:
   - Select **`gh-pages`**.
   - Select folder **`/(root)`**.
3. Click **Save**.

### 5. Verify the Live Site

Wait about 1 minute for GitHub to process the new branch, then visit:
`https://iamkm23.github.io/engineering-docs/docs-main/1.0/index.html`

Your CSS and navigation should now work perfectly!
