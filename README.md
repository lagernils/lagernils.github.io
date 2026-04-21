# lagernils.github.io

Personal academic website for **Nils Lager**, PhD student in Economics at the Stockholm School of Economics. Built with Jekyll using the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template and hosted on GitHub Pages.

**Live site:** https://lagernils.github.io/

## Site structure

### Pages

All pages live in `_pages/` and are Markdown or HTML files with YAML front matter. The navigation order is set in `_data/navigation.yml`.

| Page | File | URL | Description |
|------|------|-----|-------------|
| About (homepage) | `_pages/about.md` | `/` | Short bio and research interests |
| Research | `_pages/research.md` | `/research/` | Published papers, work in progress |
| Teaching | `_pages/teaching.html` | `/teaching/` | Courses taught (Lecturer and TA) |
| CV | `_pages/cv.md` | `/cv/` | Embedded PDF viewer with built-in download |
| Popular Writing | `_pages/third_mission.md` | `/popular-writing/` | Policy briefs + vertical scrollable list of opinion article cards with OG images |

### Key configuration

| File | Purpose |
|------|---------|
| `_config.yml` | Site title, author bio, social links, URL, Jekyll settings |
| `_data/navigation.yml` | Header navigation links and order |
| `_includes/head/custom.html` | Custom CSS/JS injected into `<head>` |

### Content directories

| Directory | Contents |
|-----------|----------|
| `_pages/` | All site pages (about, research, teaching, cv, popular writing, 404, terms) |
| `_publications/` | Publication entries (currently empty; research is in `_pages/research.md`) |
| `_talks/` | Talk entries (currently empty) |
| `_teaching/` | Teaching entries (currently empty; teaching is in `_pages/teaching.html`) |
| `_posts/` | Blog posts (currently empty; blog is not in navigation) |
| `_portfolio/` | Portfolio entries (currently empty; portfolio is not in navigation) |

### Assets

| Directory | Contents |
|-----------|----------|
| `files/` | Downloadable files. Currently: `Nils_Lager_CV.pdf` |
| `images/` | Profile photo (`profile.jpg`), favicon files, rent article image |
| `_sass/` | SCSS stylesheets (theme). Profile photo shape is set in `_sass/layout/_sidebar.scss` |
| `assets/` | Compiled CSS/JS assets |

### Theme and layout

| Directory | Purpose |
|-----------|---------|
| `_layouts/` | Page layout templates (default, single, archive, talk, cv, splash) |
| `_includes/` | Reusable HTML partials (author profile, header, footer, SEO, analytics) |

### Other files

| File/Directory | Purpose |
|----------------|---------|
| `Gemfile` | Ruby dependencies for Jekyll |
| `Dockerfile`, `docker-compose.yaml` | Docker setup for local development |
| `.devcontainer/` | VS Code Dev Container config |
| `markdown_generator/` | Python/Jupyter tools to generate Markdown from TSV (from original template) |
| `talkmap.py`, `talkmap.ipynb` | Generate map of talk locations (from original template) |

## How to edit

### Changing page content

Edit the Markdown/HTML files in `_pages/`. The front matter at the top of each file controls the layout, title, and permalink.

### Changing author info / sidebar

Edit the `author:` section in `_config.yml` (name, bio, email, location, employer, social links). The profile image is `images/profile.jpg`, referenced as `avatar` in `_config.yml`.

### Changing navigation

Edit `_data/navigation.yml`. Each entry has a `title` and `url` that must match a page's `permalink`.

### Updating the CV PDF

Replace `files/Nils_Lager_CV.pdf` with the new file (keep the same filename).

### Adding opinion articles to Popular Writing

In `_pages/third_mission.md`, add a new `<div class="article-card">` block inside the `<div class="article-list">` container. Each card is a horizontal row: image on the left, source/title/date on the right. Use the article's `og:image` for the thumbnail.

## Running locally

```bash
bundle install
bundle exec jekyll serve -l -H localhost
```

The site will be available at `http://localhost:4000`. Changes to Markdown and HTML files auto-reload; changes to `_config.yml` require a restart.

### With Docker

```bash
docker compose up
```

Site available at `http://localhost:4000`.

## Based on

Forked from [Academic Pages](https://github.com/academicpages/academicpages.github.io), which is based on the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) by Michael Rose (MIT License).
