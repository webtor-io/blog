---
title: "Discover Page is Live + Streaming Improvements"
date: 2026-02-27T20:00:00+03:00
series: "What's new"
translationKey: "discover-page-and-streaming-improvements"
titleEmoji: ":clapper:"
---
Hey everyone! Been a busy few days — here's what's new in Webtor.

## Discover — Browse Movies & Series Right Inside Webtor

The biggest addition this week is the Discover page (`/discover`). You can now browse and search movies and series without leaving Webtor:

- **Cinemeta catalogs built in** — top movies and series are available by default, no setup needed
- **Stremio addon support** — connect your favorite Stremio addons to expand the catalog. Free users can add up to 3 addons, paid plans get unlimited
- **Addon Wizard** — a guided setup flow that lets you browse official and community Stremio addons, see popularity ratings, and install them in batch
- **Search across all sources** — type a title and get results from Cinemeta + all your connected addons at once
- **Series support** — full episode picker with season navigation, including proper handling of Specials (Season 0)
- **Stream selection** — pick from available streams with filters by source, label, and language, then play directly through Webtor

The whole thing is built with Preact for a lightweight, fast experience — no heavy framework bloat.

## Streaming Quality Checks

Before you start streaming, Webtor now checks your available bandwidth against what the file actually needs for smooth playback. If your connection or plan speed isn't enough, you'll get a clear message explaining why and what your options are (smaller file, more seeders, Vault, or upgrading your plan). No more wondering why a video keeps buffering.

---

As always, your support makes this possible — thank you!
