🚀 Quarto + Jupyter + GitHub Pages Automation
🎯 Goal

# Quarto Blog Template
Easily create a Jupyter-powered blog with Quarto and deploy it automatically to GitHub Pages using GitHub Actions.

## 🚀 Quick Start
1. **Clone this repository:**
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. **Install [Quarto](https://quarto.org/docs/get-started/):**
   - Download and install Quarto for your OS
   - Verify installation:
     ```bash
     quarto check
     ```
3. **Customize your site:**
   - Edit `_quarto.yml` for site title, navbar, and theme
   - Update `about.qmd` and `index.qmd` with your info
   - Add your profile photo to `images/`
4. **Add blog posts:**
   - Place Jupyter notebooks (`.ipynb`) in the `posts/` folder
   - Each notebook should start with YAML metadata, e.g.:
     ```yaml
     ---
     title: "My First Post"
     date: "2025-09-17"
     author: "Your Name"
     categories: [blog, tutorial]
     ---
     ```
5. **Preview locally:**
   ```bash
   cd learn-quarto
   quarto preview
   ```
6. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Update blog"
   git push origin main
   ```
7. **Automatic Deployment:**
   - GitHub Actions will build and deploy your site to GitHub Pages
   - Your site will be live at `https://<your-username>.github.io/<your-repo>/`

## 🛠️ Customization
- Change theme, navbar, and layout in `_quarto.yml`
- Add more pages or sections as needed
- Update `posts/index.qmd` to configure blog listing

## 📝 Template Features
- Jupyter notebook support for posts
- Automatic blog listing page
- GitHub Actions workflow for deployment
- Easy customization

## 📋 Setup Checklist
- [ ] Fork or clone the repo
- [ ] Install Quarto
- [ ] Edit site metadata in `_quarto.yml`
- [ ] Add your first notebook to `posts/`
- [ ] Push to GitHub
- [ ] Enable GitHub Pages (Source: GitHub Actions)

## 💡 Notes
- Local preview: `quarto preview`
- Published site: `https://<your-username>.github.io/<your-repo>/`
- Default output folder: `_site` (auto-generated each build)

Automate the workflow so that:

I write content in a Jupyter/IPython Notebook (.ipynb).

I commit + push it to GitHub.

A GitHub Actions workflow automatically:

Builds the Quarto project

Converts the notebook into a blog post

Deploys the site to GitHub Pages

The updated blog is live at <username>.github.io/<repo> with zero manual steps.

✅ What’s Done So Far
1. Installed Quarto

Downloaded from quarto.org
.

Verified installation with:

quarto check

2. Created a Quarto Project

Created a new website project:

quarto create project website myblog


Project structure:

myblog/
  ├── _quarto.yml
  ├── index.qmd
  ├── about.qmd
  ├── posts/
  └── styles.css

3. Local Testing

Built the site:

quarto render
quarto preview


Verified homepage, blog index, and about page work locally.

4. GitHub Setup

Initialized Git and pushed project to GitHub:

git init
git add .
git commit -m "Initial Quarto site"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main

5. Added Notebook Support

Quarto supports .ipynb directly.

Any notebook placed inside posts/ becomes a blog post after rendering.

Example: posts/my-first-notebook.ipynb.

6. GitHub Actions Workflow

Created .github/workflows/publish.yml:

name: Quarto Publish

on:
  push:
    branches: [ main ]

jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: Setup Quarto
        uses: quarto-dev/quarto-actions/setup@v2

      - name: Render Quarto Project
        run: quarto render

      - name: Publish to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: _site

7. GitHub Pages

Enabled GitHub Pages in repo settings.

Selected gh-pages branch as the source.

🔜 Next Steps

Add more .ipynb notebooks to posts/.

Push changes → GitHub Actions builds & publishes automatically.

Customize site:

Navbar

Themes

About page with profile photo + links

📌 Notes

Local preview: quarto preview

Published site lives at: https://<username>.github.io/<repo>/

Default output folder = _site (auto-generated each build).