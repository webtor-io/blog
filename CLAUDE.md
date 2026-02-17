# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Multilingual Hugo blog for [webtor.io](https://webtor.io). Live at https://blog.webtor.io. Supports English and Russian content.

## Commands

```bash
hugo server        # Local dev server with live reload (http://localhost:1313)
hugo               # Build static site to public/ directory
```

Hugo extended version is required. Verify with `hugo version`.

## Architecture

- **Static site generator**: Hugo with `hugo-theme-basic` theme (git submodule in `themes/`)
- **CSS**: Tachyons utility framework + custom dark theme in `static/css/webtor.css`
- **Deployment**: Docker (nginx:alpine serving `public/`), CI via GitHub Actions pushing to ghcr.io
- **Analytics**: Umami (privacy-focused), configured in `layouts/partials/head_includes.html`

### Content Structure

Posts use Hugo leaf bundles: `content/{lang}/post/{slug}/index.md` with colocated images.

```
content/
  en/post/{slug}/index.md   # English posts
  ru/post/{slug}/index.md   # Russian translations
```

### i18n / Translation Linking

Two languages configured in `config.toml`: `en` (weight 1, default) and `ru` (weight 2). English and Russian versions of the same post are linked via the `translationKey` frontmatter field — **both versions must use the same `translationKey` value**. Hugo auto-generates hreflang tags and language switcher links from this.

### Taxonomies

- `series` — groups related posts (e.g., "What's new", "Torrent Basics")
- `tags` — topic tagging

Permalink pattern: `/post/:slug`

### Layout Override Pattern

The theme lives in `themes/hugo-theme-basic/`. To customize, place override files in the root `layouts/` directory rather than modifying the theme directly. Currently `layouts/partials/head_includes.html` overrides the theme's version to add Tachyons, custom CSS, Highlight.js, and Umami analytics.

## Post Frontmatter

```yaml
---
title: "Post Title"
date: 2026-01-18T21:47:00+03:00      # ISO 8601 with timezone
slug: "post-slug"                     # URL slug
translationKey: "post-slug"           # Links EN/RU versions (CRITICAL)
series: "What's new"                  # Optional, groups posts
titleEmoji: ":rocket:"               # Optional, emoji in title
aliases:                              # Optional, URL redirects
  - /old-url/
---
```

`translationKey` is critical — without it, Hugo won't link translations together.