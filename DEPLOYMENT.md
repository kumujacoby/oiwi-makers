# Quick Deployment to GitHub Pages

## Step-by-Step Instructions

### 1. Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `oiwi-makers` (or your preferred name)
3. Description: "ʻŌiwi Makers - TTRPG & Maker Curriculum for Kamehameha Schools"
4. Choose: **Public** (required for free GitHub Pages)
5. DO NOT initialize with README (we already have one)
6. Click "Create repository"

### 2. Upload Files

**Option A: Using GitHub Web Interface (Easiest)**
1. On your new repository page, click "uploading an existing file"
2. Drag and drop ALL files from this folder:
   - index.html
   - curriculum.html
   - README.md
   - .gitignore
3. Scroll down, add commit message: "Initial commit"
4. Click "Commit changes"

**Option B: Using Git Command Line**
```bash
# Navigate to this folder in terminal
cd /path/to/github-pages-ready

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - ʻŌiwi Makers curriculum"

# Connect to GitHub (replace YOUR-USERNAME and YOUR-REPO)
git remote add origin https://github.com/YOUR-USERNAME/oiwi-makers.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar, under "Code and automation")
4. Under "Source":
   - Branch: Select **main**
   - Folder: Select **/ (root)**
5. Click **Save**
6. Wait 1-2 minutes

### 4. View Your Live Site!

Your site will be available at:
```
https://YOUR-USERNAME.github.io/oiwi-makers/
```

For example, if your GitHub username is `jacobykamehameha`:
```
https://jacobykamehameha.github.io/oiwi-makers/
```

## Updating Your Site

After making changes:

```bash
git add .
git commit -m "Describe your changes"
git push origin main
```

Changes appear live in 1-2 minutes!

## Custom Domain (Optional)

If you want to use your own domain:

1. Create a file named `CNAME` (no extension)
2. Add your domain: `oiwi-makers.yourdomain.com`
3. Configure DNS with your domain provider
4. Full instructions: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Troubleshooting

**Site not loading?**
- Wait 2-3 minutes after enabling Pages
- Check that repository is Public
- Verify main branch and / (root) are selected

**Changes not appearing?**
- Wait 1-2 minutes for rebuild
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Check GitHub Actions tab for build status

**404 Error?**
- Make sure `index.html` is in the root folder
- Check that Pages is enabled
- Verify repository name in URL matches

## Need Help?

GitHub Pages documentation: https://docs.github.com/en/pages
