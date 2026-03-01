# Wild Econometrics & R Blog

A blogdown-based blog built with Hugo and deployed to GitHub Pages.

## Prerequisites

- R (4.0+)
- RStudio (recommended)
- The `blogdown` R package: `install.packages("blogdown")`

Hugo 0.80.0 is pinned in `.Rprofile` and will be installed automatically by blogdown if needed.

## Local Development

Start a live preview server:

```r
blogdown::serve_site()
```

Edit `.Rmd` files in `content/` — they auto-knit on save (configured via `blogdown.knit.on_save = TRUE`).

## Building the Site

Build the static site to the `docs/` folder:

```r
blogdown::build_site()
```

## Deployment

The blog is deployed to GitHub Pages from the `docs/` folder.

```bash
git add docs/
git commit -m "build site"
git push
```

GitHub Pages automatically serves the updated site.

## Project Structure

```
├── config.yaml          # Hugo/blogdown configuration
├── content/             # Source Rmd files
│   ├── about.Rmd
│   └── post/            # Blog posts
├── themes/hugo-tanka/   # Hugo theme
├── static/              # Static assets (images, etc.)
├── R/                   # Custom build scripts (optional)
└── docs/                # Generated site (output)
```

## Creating a New Post

```r
blogdown::new_post("My Post Title", ext = ".Rmd")
```

This creates a new post directory in `content/post/` with the current date.
