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
- **Links to webtor.io carry UTM**: `layouts/_default/_markup/render-link.html` adds `utm_source=blog&utm_medium=post&utm_campaign=<post slug>` to every markdown link to webtor.io without utm of its own; the logo and footer links use `utm_medium=nav` / `footer`. Write plain `https://webtor.io/...` links in posts — the hook tags them

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

## What the blog doesn't publish

No how-tos built around third-party torrent sites or catalogues ("find the movie on site X, grab the .torrent, open it in Webtor"): Webtor plays torrents the reader already has; it is not a way to find content. The four 2019 posts of that kind ("Watch movies online from yts.am / nyaa.si / rutor.org / rutracker.org") and their series were deleted on 2026-09-23 on the owner's decision; their URLs answer 404. Don't bring them back. The same went on 2026-09-24 for "Webtor + Torrentio = ⚡" (`webtor-torrentio-stremio`): a post named after a torrent-scraping addon that promised "any content … instantly"; the feature it announced is covered by webtor.io/stremio-addons-online and the Smart TV post.

## Tone of Voice

Blog posts are written for a **non-technical audience** — regular users who stream torrents, not engineers.

- **Simple language** — no jargon, no implementation details (no "nginx-vod", "madvise", "OOM", "range requests", "database leases"). Describe what changed for the user, not how it was built
- **Short and direct** — short sentences, no filler. Get to the point
- **Conversational** — talk like a friend sharing good news, not a corporate changelog
- **Show the benefit** — instead of "increased buffer size from 256K to 4MB", say "4K streams play smoothly now"
- **Use examples** — when describing features, show what the user would actually type or see (e.g., "just type 'suggest a fresh comedy for tonight'")
- **No self-congratulation** — don't say "we're excited to announce". Just say what's new
- **Russian version is not a translation** — it should read naturally in Russian, not like translated English. Use native phrasing and examples