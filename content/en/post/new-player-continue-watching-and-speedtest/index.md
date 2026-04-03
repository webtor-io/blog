---
title: "New Player, Continue Watching & Speed Test"
date: 2026-04-03T18:00:00+03:00
slug: "new-player-continue-watching-and-speedtest"
series: "What's new"
translationKey: "new-player-continue-watching-and-speedtest"
titleEmoji: ":film_projector:"
---

We've completely rebuilt the video player, added continue watching, and shipped a few more things you might enjoy.

## New Video Player

We replaced mediaelement.js with a **custom player built on Preact and HLS.js**. It's lighter, faster, and gives us full control over the playback experience.

What changed:
- **Better mobile UX** — controls are more responsive on touch devices
- **Fixed seek on iOS** — jumping to a position now works reliably on iPhones and iPads
- **Improved embed mode** — the player works better when embedded on third-party sites

This is the foundation for everything we're building next with the player.

## Continue Watching

You can now **pick up where you left off**. Webtor tracks your playback position and shows a "Resume from X:XX?" prompt when you come back to a video.

For series, it goes further — when you finish an episode, the next one starts automatically. No more hunting for the right episode in a folder.

## Speed Test

We added a [speed test page](/speedtest) that measures your connection to Webtor servers right in the browser. But here's the twist — it runs a **dual test**, comparing throughput on a standard server vs. a premium one, so you can see the difference for yourself.

Results are saved and get a shareable link, so you can easily reference them later.

## TMDB Enrichment

Torrent pages now pull metadata from TMDB automatically — **posters, descriptions, and episode info** for series. If you open a torrent through Discover, the resource page shows full details instead of just file names.

We also added a **share button** for regular torrents, making it easier to send a link to someone.

## Under the Hood

A few things that make streaming smoother:

- **Prefetch buffering** — the proxy now buffers content from bursty torrent sources before sending it to you, resulting in steadier playback
- **Automatic retry** — if a backend pod goes down mid-stream, the proxy transparently retries on another one
- **No more size limits** — the seeder now evicts least-recently-used data on the fly, so you can stream torrents of any size without running out of disk space
- **Faster subtitle loading** — reduced timeout from 30s to 5s with proper fallbacks

---

Thanks for using Webtor. More updates coming soon.
