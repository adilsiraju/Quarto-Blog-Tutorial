🚀 Quarto + Jupyter + GitHub Pages Automation
🎯 Goal

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