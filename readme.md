# 🚀 Quarto Blog Template for Data Scientists

**Transform your Jupyter notebooks into a professional blog in minutes!**

Perfect for sharing data science projects, machine learning experiments, tutorials, and visualizations. No HTML/CSS knowledge required - just write in Jupyter notebooks and everything else is automated.

## ✨ What You Get

- 📊 **Beautiful Blog** - Professional design with syntax highlighting
- 🚀 **Auto-Deploy** - Push to GitHub and your site updates automatically  
- 📝 **Write in Jupyter** - Use familiar notebook environment
- 📱 **Mobile-Friendly** - Responsive design that works everywhere
- � **Built-in Search** - Readers can easily find content
- 📈 **Interactive Plots** - Plotly, Bokeh, and other visualizations work perfectly
- � **Code Folding** - Readers can hide/show code as needed

## 🎯 Who This Is For

- Data scientists sharing projects
- Researchers documenting experiments  
- Educators creating tutorials
- Anyone wanting to blog with code

## 🚀 Quick Start (5 minutes)

### Step 1: Get the Template
```bash
# Option A: Use this template on GitHub (recommended)
# Click "Use this template" button above

# Option B: Clone directly
git clone https://github.com/username/quarto-blog-template.git my-blog
cd my-blog/learn-quarto
```

### Step 2: Install Requirements
```bash
# Install Python packages
pip install jupyter quarto-cli pandas numpy matplotlib plotly seaborn

# Verify Quarto installation
quarto check
```

### Step 3: Preview Your Blog
```bash
# Start local preview (auto-refreshes as you edit)
quarto preview
# Opens http://localhost:4200
```

### Step 4: Deploy to GitHub Pages
1. Create new repository on GitHub
2. Push your code:
   ```bash
   git remote set-url origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
3. In GitHub: Settings → Pages → Source: **GitHub Actions**
4. Your blog is live at: `https://YOUR-USERNAME.github.io/YOUR-REPO/`

## 📝 Creating Your First Post

### 1. Create a Notebook
```bash
# Create new notebook in posts/ folder
touch posts/my-first-post.ipynb
```

### 2. Add Metadata (First Cell)
```yaml
---
title: "My Amazing Data Analysis"
description: "Exploring interesting patterns in the data"
author: "Your Name"
date: "2025-09-17"
categories: [analysis, python, visualization]
image: "thumbnail.png"  # Optional
format:
  html:
    code-fold: true
    toc: true
---
```

### 3. Write Your Content
- **Markdown cells** for explanations, conclusions, methodology
- **Code cells** for analysis, plotting, data processing
- **Mix freely** - tell your story with code and narrative

### 4. See It Live
```bash
# Save notebook and refresh preview
# Changes appear instantly at http://localhost:4200
```

## 📊 Example Posts (Included)

### 1. Basic Data Analysis (`posts/sample-analysis.ipynb`)
- Loading and cleaning data with pandas
- Creating visualizations with matplotlib
- Statistical analysis and insights
- **Perfect starting point for beginners**

### 2. Interactive Visualizations (`posts/interactive-viz.ipynb`)
- Plotly scatter plots and animations
- Interactive charts that work in browsers
- Time series visualizations
- **Shows advanced visualization techniques**

## ⚙️ Customizing Your Blog

### Site Configuration (`_quarto.yml`)
```yaml
website:
  title: "Your Blog Name"
  description: "Your tagline here"
  navbar:
    background: primary
    search: true
    right:
      - text: "About"
        href: about.qmd
      - icon: github
        href: https://github.com/YOUR-USERNAME
  page-footer: "© 2025 Your Name"

format:
  html:
    theme: cosmo  # Try: flatly, minty, pulse, sandstone
    css: styles.css
    toc: true
    code-fold: true
```

### Personal Pages
- **`about.qmd`** - Your bio, skills, contact info
- **`index.qmd`** - Homepage content
- **`styles.css`** - Custom colors and fonts

### Adding Your Branding
- Add logo: `images/logo.png`
- Profile photo: `images/profile.jpg`
- Favicon: `images/favicon.ico`

## 🔧 Common Issues & Solutions

### Plots Not Showing?
```bash
# Install missing packages
pip install plotly kaleido

# For matplotlib issues
pip install matplotlib --upgrade
```

### Build Failing?
1. Check GitHub Actions tab in your repository
2. Look for error messages in the log
3. Common fixes:
   ```bash
   # Update packages
   pip install --upgrade quarto-cli
   
   # Check notebook for errors
   jupyter nbconvert --execute posts/your-post.ipynb
   ```

### Need Help?
- [Quarto Discussion Forum](https://github.com/quarto-dev/quarto-cli/discussions)
- [Example Sites Gallery](https://quarto.org/docs/gallery/)
- [Documentation](https://quarto.org/docs/guide/)

## 🎨 Themes & Customization

### Available Themes
Try these in your `_quarto.yml`:
- `cosmo` (default) - Clean and modern
- `flatly` - Flat design
- `minty` - Green accents
- `pulse` - Purple theme
- `sandstone` - Warm colors
- `superhero` - Dark theme

### Custom CSS
Edit `styles.css` for:
- Brand colors
- Font choices  
- Layout adjustments
- Mobile responsiveness

## 📈 Growing Your Blog

### SEO Tips
- Use descriptive titles and descriptions
- Add relevant categories and tags
- Include alt text for images
- Keep URLs clean and readable

### Sharing Content
- Enable social media previews
- Add share buttons
- Cross-post to LinkedIn, Twitter
- Submit to data science communities

## 🚀 Advanced Features

### Custom Domains
```yaml
# In _quarto.yml
website:
  site-url: "https://yourdomain.com"
```

### Analytics
```html
<!-- Add to _quarto.yml -->
format:
  html:
    include-in-header: |
      <!-- Google Analytics code -->
```

### Comments
- Add Disqus or Giscus for reader engagement
- Configure in `_quarto.yml`

## 📚 Resources & Learning

### Documentation
- [Quarto Guide](https://quarto.org/docs/guide/) - Complete documentation
- [Jupyter Guide](https://jupyter.org/documentation) - Notebook basics
- [GitHub Pages](https://docs.github.com/pages) - Hosting documentation

### Inspiration
- [Quarto Gallery](https://quarto.org/docs/gallery/) - Example sites
- [Data Science Blogs](https://github.com/rushter/data-science-blogs) - Curated list
- [Blog Post Ideas](https://towardsdatascience.com/how-to-start-a-data-science-blog-7e0d7a027467)

### Community
- [r/datascience](https://reddit.com/r/datascience) - Share your posts
- [Kaggle](https://kaggle.com) - Find datasets for analysis
- [Towards Data Science](https://towardsdatascience.com) - Publication opportunities

---

**Ready to start blogging? Clone this template and share your first post! 🎉**

Questions? Open an issue or start a discussion. Happy blogging! 📝
