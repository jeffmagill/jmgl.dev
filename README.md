# jmgl.dev

Jeff Magill's personal site and blog, built with [Eleventy](https://www.11ty.dev/) and deployed to GitHub Pages by GitHub Actions.

## Run it locally

```bash
npm install
npm start          # http://localhost:8080, reloads on save
npm run build      # outputs the site to _site/
```

## Write a post

Add a Markdown file to `src/posts/`, named `YYYY-MM-DD-short-slug.md`:

```markdown
---
title: How we found where our BI numbers were breaking
description: One sentence for the post list, link previews, and search results.
date: 2026-10-15
draft: true
---

Post body in Markdown...
```

- The URL becomes `/posts/short-slug/` (the date prefix is dropped).
- `draft: true` shows the post when you run it locally but leaves it out of the live site. Remove the line to publish.
- Images go in `src/img/` and are referenced as `/img/file.png`.
- `src/posts/2026-10-08-formatting-reference.md` shows every supported format. Delete it before launch.

## Deploy

Pushing to `master` builds and deploys automatically (`.github/workflows/deploy.yml`).
One-time setup: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Layout

```
src/
  _data/site.json          site title, tagline, social links
  _includes/layouts/       base.njk (page shell), post.njk (post template)
  css/                     style.css, prism.css (code highlighting)
  posts/                   blog posts (Markdown)
  index.njk                home page / post list
  about.md                 About page
  CNAME                    custom domain (jmgl.dev). Keep this.
eleventy.config.js         plugins, filters, Markdown settings
```
