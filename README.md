# Nikolabs website

Static site built with Hugo, deployed on Cloudflare Pages at `https://nikolabs.ai`.

## Local development

Prereqs: Hugo extended v0.128+.

Run a local server:

```bash
hugo server --buildDrafts --disableFastRender
```

Build for production:

```bash
hugo --minify
```

## Cloudflare Pages

- Create a new Pages project and connect this GitHub repo
- Framework preset: None
- Build command: `hugo --minify`
- Build output directory: `public`
- Environment variable: `HUGO_VERSION` = the version you use locally (e.g. `0.145.0`)

Set custom domain `nikolabs.ai` to this Pages project. Ensure DNS `CNAME` to `<project>.pages.dev` is configured in Cloudflare.

## Content structure

- `content/`: Markdown pages
- `layouts/`: HTML templates
- `static/`: Static assets (CSS, robots.txt)
- `hugo.toml`: Site configuration
