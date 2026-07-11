# Wild Econometrics in R and Python

A Quarto-powered blog on econometrics and statistical inference, deployed to GitHub Pages.

## Prerequisites

- [pixi](https://pixi.sh/) — package manager and task runner
- Quarto, R, and R packages (knitr, rmarkdown) — all managed via pixi

## Local Development

```bash
# Install dependencies
pixi install

# Start live preview server
pixi run preview

# Render the site (builds to docs/)
pixi run render

# Clean and rebuild
pixi run clean
```

## Project Structure

```
├── _quarto.yml           # Quarto website configuration
├── pixi.toml             # pixi project / environment / tasks
├── index.qmd             # Blog home page (listing)
├── about.qmd             # About page
├── styles.css            # Custom CSS
├── images/               # Global images (profile photo, etc.)
├── posts/                # Blog posts (one subdirectory per post)
│   ├── _metadata.yml     # Shared post options (freeze, eval: false)
│   └── <slug>/
│       ├── index.qmd     # Post source
│       └── *.jpg/png     # Post figures
├── _freeze/              # Cached knitr output (freeze: true)
└── docs/                 # Generated site (output-dir: docs)
```

## Deployment

The blog is deployed to GitHub Pages from the `docs/` folder.

```bash
pixi run render
git add docs/
git commit -m "build site"
git push
```

## Creating a New Post

```bash
mkdir -p posts/my-new-post
touch posts/my-new-post/index.qmd
```

Add front matter:

```yaml
---
title: "My New Post"
author: "Alexander Fischer"
date: "2025-01-15"
categories: [R, econometrics]
---
```
