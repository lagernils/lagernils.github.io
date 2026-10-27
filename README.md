# lagernils.github.io

Personal academic website for **Nils Lager**, PhD student in Economics at the Stockholm School of Economics. Built with Jekyll using the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template and hosted on GitHub Pages.

**Live site:** https://lagernils.github.io/

## Site structure

### Pages

All pages live in `_pages/` and are Markdown or HTML files with YAML front matter. The navigation order is set in `_data/navigation.yml`.

| Page | File | URL | Description |
|------|------|-----|-------------|
| About (homepage) | `_pages/about.md` | `/` | Short bio and research interests |
| Research | `_pages/research.md` | `/research/` | Publications, working papers, work in progress |
| Teaching | `_pages/teaching.html` | `/teaching/` | Courses taught (Lecturer and TA), link to Boot Camp notes |
| CV | `_pages/cv.md` | `/cv/` | Embedded PDF viewer with built-in download |
| Popular Writing | `_pages/third_mission.md` | `/popular-writing/` | Policy briefs + vertical scrollable list of opinion article cards with OG images |

### Key configuration

| File | Purpose |
|------|---------|
| `_config.yml` | Site title, author bio, social links, URL, Jekyll settings |
| `_data/navigation.yml` | Header navigation links and order |
| `_includes/head/custom.html` | Favicons and Person structured data (JSON-LD) injected into `<head>` |
| `_includes/seo.html` | Meta description, Open Graph and Twitter card tags (default preview image: `og_image` in `_config.yml`) |

### Content directories

| Directory | Contents |
|-----------|----------|
| `_pages/` | All site pages (about, research, teaching, cv, popular writing, 404) |

The template's collection folders (`_publications/`, `_talks/`, `_teaching/`, `_posts/`, `_portfolio/`) are not used; all content is written directly in `_pages/`.

### Assets

| Directory | Contents |
|-----------|----------|
| `files/` | Downloadable files: `Nils_Lager_CV.pdf`, working paper manuscript and online appendix (`Lager_RollUps_MarkUps*.pdf`), policy brief `Skolbyten.pdf`, Boot Camp notes `Math5301_BootCamp_Notes_2026.pdf` |
| `images/` | Profile photo (`profile.jpg`), favicon files, rent article image, `article-placeholder.svg` (fallback thumbnail for opinion articles) |
| `_sass/` | SCSS stylesheets (theme). Profile photo shape is set in `_sass/layout/_sidebar.scss` |
| `assets/` | Compiled CSS/JS assets |

### Theme and layout

| Directory | Purpose |
|-----------|---------|
| `_layouts/` | Page layout templates (default, single, archive, talk, splash) |
| `_includes/` | Reusable HTML partials (author profile, header, footer, SEO, analytics) |

### Other files

| File/Directory | Purpose |
|----------------|---------|
| `Gemfile` | Ruby dependencies for Jekyll |
| `Dockerfile`, `docker-compose.yaml` | Docker setup for local development |
| `.devcontainer/` | VS Code Dev Container config |

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

In `_pages/third_mission.md`, add a new `<div class="article-card">` block inside the `<div class="article-list">` container. Each card is a horizontal row: image on the left, source/title/date on the right. Use the article's `og:image` for the thumbnail. If that image later disappears from the newspaper's server, a script on the page swaps in `images/article-placeholder.svg`.

### Adding a working paper

Put the PDFs in `files/` (avoid journal names in filenames) and add an entry under `## Working Papers` in `_pages/research.md`.

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
