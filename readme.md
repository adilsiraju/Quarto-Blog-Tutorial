# 🚀 Quarto Blog Template

Easily create and deploy a data science blog with Jupyter notebooks + Quarto.

## ⚡ Quick Start

1. **Clone & Setup**

   ```bash
   git clone https://github.com/adilsiraju/Quarto-Blog-Tutorial.git my-blog
   cd my-blog/learn-quarto
   ```

2. **Write & Preview**

   ```bash
   # Add .ipynb files to posts/
   quarto preview   # open http://localhost:4200
   ```

3. **Deploy**

   ```bash
   git push   # Site auto-updates via GitHub Actions
   ```

## 📝 Writing Posts

1. Create a notebook in `posts/`
2. Add metadata:

   ```yaml
   ---
   title: "Your Post Title"
   date: "YYYY-MM-DD"
   ---
   ```

## ⚙️ Setup Checklist

* [ ] Install [Quarto](https://quarto.org/docs/get-started/)
* [ ] Update `_quarto.yml` (title, theme)
* [ ] Edit `about.qmd` and `index.qmd`
* [ ] Enable GitHub Pages (Settings → Pages → Source: GitHub Actions)

## 🔄 Workflow

1. Write in Jupyter Notebook (`.ipynb`).
2. Commit & push to GitHub.
3. GitHub Actions:

   * Builds Quarto site
   * Converts notebooks to blog posts
   * Publishes to GitHub Pages

Live site: `https://<username>.github.io/<repo>/`

## ✅ What’s Done

* Installed Quarto (`quarto check`)
* Created Quarto project (`quarto create project website myblog`)
* Verified local build (`quarto render`, `quarto preview`)
* GitHub repo initialized & pushed
* Notebook support added (place `.ipynb` in `posts/`)
* GitHub Actions workflow setup for publishing
* GitHub Pages enabled (branch: `gh-pages`)

## 🔜 Next Steps

* Add more `.ipynb` notebooks in `posts/`
* Customize site: navbar, theme, about page

## 📌 Notes

* Local preview: `quarto preview`
* Output folder: `_site/` (auto-generated)
* Published site: `https://<username>.github.io/<repo>/`

## 📚 Resources

* [Quarto Docs](https://quarto.org/docs/guide/)
* [Jupyter Docs](https://jupyter.org/)
