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
- **Crawling**: `static/robots.txt` allows everything and points at `/sitemap.xml`, the sitemap index Hugo builds for the multilingual site (it lists `/en/sitemap.xml` and `/ru/sitemap.xml`)
- **Analytics**: Umami (privacy-focused), configured in `layouts/partials/head_includes.html`

### Content Structure

Posts use Hugo leaf bundles: `content/{lang}/post/{slug}/index.md` with colocated images.

```
content/
  en/post/{slug}/index.md   # English posts
  ru/post/{slug}/index.md   # Russian translations
```

### i18n / Translation Linking

Two languages configured in `config.toml`: `en` (weight 1, default) and `ru` (weight 2). English and Russian versions of the same post are linked via the `translationKey` frontmatter field — **both versions must use the same `translationKey` value**. The language switcher and the hreflang tags are built from this: `layouts/partials/header.html` lists every version including the page itself, plus `x-default` pointing at the English one.

Check a pair by reading both posts, not by folder names. Keep the RU folder, its pinned `slug` and the EN folder of the same post on one name. Until 2026-09-23 the RU folders `new-transcoding-system` and `webtor-web-ui-v2` held each other's posts: the `translationKey`s were right, but the slugs pinned in February 2026 followed the folders, so each of the two RU URLs named the other post.

### Taxonomies

- `series` — groups related posts (e.g., "What's new", "Torrent Basics")
- `tags` — topic tagging

Permalink pattern: `/post/:slug`

### Layout Override Pattern

The theme lives in `themes/hugo-theme-basic/`. To customize, place override files in the root `layouts/` directory rather than modifying the theme directly. Currently `layouts/partials/head_includes.html` overrides the theme's version to add Tachyons, custom CSS, Highlight.js, and Umami analytics.

### Keeping a page out of search

`noindex: true` in a post's front matter adds `<meta name="robots" content="noindex, follow">` and drops the page from the sitemap. The URL, its aliases and its backlinks keep working. The rule lives in one place, `layouts/partials/noindex.html`; `layouts/partials/header.html` and `layouts/sitemap.xml` (Hugo's embedded sitemap plus that one filter) both call it, so don't add `sitemap.disable` next to it. Series and tag pages have no front matter of their own: they drop out when every post in them is noindex.

Noindexed today: the four 2019 how-tos "Watch movies online from yts.am / nyaa.si / rutor.org / rutracker.org" and their two series pages (EN, RU). The owner chose noindex over deletion on 2026-09-23 so it stays reversible: remove the `noindex` line to bring a post back. They still show up in the blog's own post lists and RSS. Don't link to them from other posts.

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
noindex: true                         # Optional, keeps the page live but out of search
---
```

`translationKey` is critical — without it, Hugo won't link translations together.

## Tone of Voice

Blog posts are written for a **non-technical audience** — regular users who stream torrents, not engineers.

- **Simple language** — no jargon, no implementation details (no "nginx-vod", "madvise", "OOM", "range requests", "database leases"). Describe what changed for the user, not how it was built
- **Short and direct** — short sentences, no filler. Get to the point
- **Conversational** — talk like a friend sharing good news, not a corporate changelog
- **Show the benefit** — instead of "increased buffer size from 256K to 4MB", say "4K streams play smoothly now"
- **Use examples** — when describing features, show what the user would actually type or see (e.g., "just type 'suggest a fresh comedy for tonight'")
- **No self-congratulation** — don't say "we're excited to announce". Just say what's new
- **Russian version is not a translation** — it should read naturally in Russian, not like translated English. Use native phrasing and examples