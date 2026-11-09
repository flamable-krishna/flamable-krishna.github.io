# Gokul — Personal Website (Jekyll)

A clean, minimal personal website for **Gokul** with **Home, About, Projects, and Blog** pages. Built with [Jekyll](https://jekyllrb.com/) for native **GitHub Pages** hosting.

- **Site:** https://flamable-krishna.github.io/
- **Repository:** `flamable-krishna/flamable-krishna.github.io`
- **GitHub profile:** https://github.com/flamable-krishna

## Structure

```text
.
├── _config.yml           # Site settings (title, author, URL)
├── _layouts/             # Page/post templates
├── _data/
│   └── projects.yml      # Curated projects list (edit to add projects)
├── _posts/               # Blog posts (Markdown)
├── assets/css/style.css  # Styles
├── index.html            # Home / hero
├── about.md              # About page
├── projects.md           # Projects page
└── blog/index.html       # Blog listing
```

## Write a new blog post (simple ongoing workflow)

1. Create a new Markdown file in `_posts/` named with this format:
   ```text
   YYYY-MM-DD-your-post-title.md
   ```
   Example: `2026-12-01-what-i-learned-this-week.md`

2. Add front matter at the top, then write your post:
   ```md
   ---
   layout: post
   title: "Your Post Title"
   date: 2026-12-01
   ---

   Write your post here using Markdown.
   - Bullet points work
   - **Bold** and [links](https://example.com) work
   ```

3. Commit and push to GitHub — GitHub Pages will build and publish the post.

## Add a GitHub project

Edit `_data/projects.yml` and add an entry:

```yml
- name: My Project
  description: What it does and what I learned.
  github: https://github.com/flamable-krishna/my-project
  demo: https://flamable-krishna.github.io/my-project/   # optional; remove if none
```

You can add multiple entries. Commit and push to update the Projects page.

## Publish on GitHub Pages

1. Push this repository to **`flamable-krishna/flamable-krishna.github.io`** on GitHub (user site repo).
2. In the repo: **Settings → Pages**.
3. Set **Source** to *Deploy from a branch*, choose your default branch (usually `main`) and folder **/ (root)**, then save.
4. GitHub will build the Jekyll site and publish it at **https://flamable-krishna.github.io/**.

## Local preview (optional)

To preview locally, install Ruby + Jekyll and run:

```bash
bundle exec jekyll serve
```

(Requires a `Gemfile`; not required for GitHub Pages publishing.)

## Customize

- **Profile/contact/intro:** `index.html`, `about.md`, `_config.yml`
- **Navigation/title:** `_config.yml`, `_layouts/default.html`
- **Styles (colors/fonts/layout):** `assets/css/style.css`
