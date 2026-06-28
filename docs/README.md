# Site source (`docs/`)

The GitHub Pages site for **The QHSE Standard**, built with Jekyll using
GitHub's integrated Pages build (no Actions workflow required).

## Enable Pages

In the repository settings → **Pages**:

- **Source:** Deploy from a branch
- **Branch:** `main` · **Folder:** `/docs`

Published at: **https://the-qhse-standard.github.io/.github/**
(the `baseurl: "/.github"` in `_config.yml` matches this project path).

## Run locally

```sh
cd docs
bundle install
bundle exec jekyll serve
# → http://127.0.0.1:4000/.github/
```

## Structure

| Path | What it is |
| :--- | :--- |
| `_config.yml`        | Site settings, plugins, baseurl |
| `_layouts/`          | `default`, `page`, `post` templates |
| `_includes/`         | `head`, `header`, `footer` partials |
| `_posts/`            | Notes (the RSS feed + `/notes/`) |
| `index.html`         | Home page |
| `start-here.md`, `about.md`, `notes.html` | Content pages |
| `assets/css/style.css` | Site styles |

Content files (`*.md` / `*.html`) carry front matter; the layout is applied
automatically via the `defaults` in `_config.yml`.
