# Gokul — Personal Website (Jekyll)

A clean, minimal personal website for **Gokul** with **Home, About, Projects, and Blog** pages. Built with [Jekyll](https://jekyllrb.com/) for native **GitHub Pages** hosting.

- **Site:** https://flamable-krishna.github.io/
- **Repository:** https://github.com/flamable-krishna/flamable-krishna.github.io
- **GitHub profile:** https://github.com/flamable-krishna

## Project structure

```text
.
├── _config.yml           # Site settings (title, author, URL, permalink)
├── _layouts/             # Page/post templates (default, post)
├── _data/
│   └── projects.yml      # Curated projects list (edit to add projects)
├── _posts/               # Blog posts (Markdown, dated filenames)
├── assets/css/style.css  # Styles
├── index.html            # Home / hero
├── about.md              # About page
├── projects.md           # Projects page
├── blog/index.html       # Blog listing
├── Gemfile               # Local Jekyll/GitHub Pages dependencies
└── README.md
```

## Write more blog posts

Blog posts live in `_posts/` and are written in **Markdown**. Jekyll uses the filename date and front matter to publish them.

### 1) Create a new post file

Add a file in `_posts/` with this exact name format:

```text
YYYY-MM-DD-your-post-title.md
```

Examples:
- `2026-11-15-what-i-learned-this-week.md`
- `2026-12-01-my-first-python-project.md`

Rules:
- Use the **date you want to publish** (usually today).
- Use **lowercase letters, numbers, and hyphens** in the title part.
- Keep the `.md` extension.

### 2) Add front matter + content

Paste this template at the top of the file, then write your post below it:

```md
---
layout: post
title: "Your Post Title"
date: 2026-11-15
---

Write your introduction here.

## What I learned

- Point one
- Point two
- Point three

## Code or notes (optional)

You can use **bold**, *italic*, [links](https://example.com), and code:

```text
example code block
```

## What’s next

Write what you plan to learn or build next.
```

Tips:
- `layout: post` is required (uses the blog post layout).
- `title` is what appears on the Blog page and the post.
- `date` should match the filename date (`YYYY-MM-DD`).
- Use normal Markdown for headings, lists, links, images, and code blocks.
- To add an image, place it in a folder like `assets/images/` and reference it: `![Alt text](/assets/images/my-photo.png)`.

### 3) Preview and publish

- **Local preview:** run the site locally (see below) and open the Blog page.
- **Publish:** commit and push to GitHub. GitHub Pages will build and publish automatically.

```powershell
cd "C:\Users\harit\OneDrive\Documents\Default Project"
git add _posts/YYYY-MM-DD-your-post-title.md
git commit -m "Add blog post: Your Post Title"
git push
```

Your post will appear at: `https://flamable-krishna.github.io/blog/YYYY/MM/DD/your-post-title/` (based on the permalink setting in `_config.yml`).

## Add a GitHub project

Edit `_data/projects.yml` and add an entry:

```yml
- name: My Project
  description: What it does and what I learned.
  github: https://github.com/flamable-krishna/my-project
  demo: https://flamable-krishna.github.io/my-project/   # optional; remove if none
```

You can add multiple entries. Commit and push to update the Projects page.

## Run the site locally

This is a Jekyll site, so opening `index.html` directly won’t render layouts/Liquid correctly. Run a local Jekyll server instead.

### Prerequisites (Windows)
1. Install **Git**: https://git-scm.com/download/win
2. Install **Ruby+Devkit** (recommended via RubyInstaller for Windows): https://rubyinstaller.org/
   - During setup, install MSYS2/devkit components when prompted.
3. Open a **new** terminal (PowerShell) after installation.

Verify:
```powershell
ruby -v
gem -v
bundle -v
```

If `bundle` is missing:
```powershell
gem install bundler
```

### Install dependencies and start the server

From the project folder:

```powershell
cd "C:\Users\harit\OneDrive\Documents\Default Project"
bundle install
bundle exec jekyll serve
```

Then open: http://127.0.0.1:4000/

Notes:
- The `Gemfile` uses `github-pages` so local builds are closer to GitHub Pages.
- Keep the server running while you edit. Jekyll usually rebuilds on changes; refresh the browser to see updates.
- Stop the server with `Ctrl + C`.
- If you get dependency/SSL errors on Windows, update RubyGems and retry: `gem update --system`.

### Open in VS Code
- Folder: `C:\Users\harit\OneDrive\Documents\Default Project`
- Link: `vscode://file/C:/Users/harit/OneDrive/Documents/Default%20Project`
- Command (in the folder): `code .`

## Publish on GitHub Pages

1. Push this repository to **`flamable-krishna/flamable-krishna.github.io`**.
2. In GitHub: **Settings → Pages**.
3. **Source:** *Deploy from a branch* → Branch **`main`** / Folder **`/ (root)`** → **Save**.
4. Site URL: https://flamable-krishna.github.io/

## Customize

- **Profile/contact/intro:** `index.html`, `about.md`, `_config.yml`
- **Navigation/title:** `_config.yml`, `_layouts/default.html`
- **Blog layout:** `_layouts/post.html`, `blog/index.html`
- **Projects list:** `_data/projects.yml`, `projects.md`
- **Styles (colors/fonts/layout):** `assets/css/style.css`
