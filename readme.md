# 🚀 Quarto Blog Template

Turn your Jupyter notebooks into a beautiful blog. Write in notebooks, push to GitHub, and your site auto-deploys with GitHub Actions.

## 🎯 Features
- 📝 Write posts in Jupyter notebooks
- 🎨 Customizable Quarto theme
- 🚀 Automatic deploys to GitHub Pages
- 🔍 Built-in search and categories
- 📱 Mobile-friendly

## ⚡ Quick Start
1. Clone and open the project
   ```bash
   git clone https://github.com/username/your-blog.git my-blog
   cd my-blog/learn-quarto
   ```
2. Write and preview locally
   ```bash
   # Add .ipynb files to posts/
   quarto preview  # opens http://localhost:4200
   ```
3. Deploy
   ```bash
   git add . && git commit -m "Update blog" && git push
   ```

## 📝 Writing Posts
1. Create a notebook in `posts/`
2. Add metadata at the top:
   ```yaml
   ---
   title: "Your Post Title"
   date: "YYYY-MM-DD"
   categories: [example]
   ---
   ```

## ⚙️ Setup Checklist
- [ ] Install Quarto: https://quarto.org/docs/get-started/
- [ ] Update `_quarto.yml` (title, navbar, theme)
- [ ] Edit `about.qmd` and `index.qmd`
- [ ] In GitHub → Settings → Pages: Source = GitHub Actions

## � Useful Links
- Quarto Guide: https://quarto.org/docs/guide/
- Jupyter: https://jupyter.org/
- GitHub Pages: https://docs.github.com/pages

Sample post: `posts/sample-analysis.ipynb`
