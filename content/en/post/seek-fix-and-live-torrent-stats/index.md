---
title: "Seek Is Finally Fixed + Live Torrent Stats"
date: 2026-03-19T18:00:00+03:00
slug: "seek-fix-and-live-torrent-stats"
series: "What's new"
translationKey: "seek-fix-and-live-torrent-stats"
titleEmoji: ":rocket:"
---
We've just shipped two updates that remove one of the most annoying problems in torrent streaming and make things way more transparent.

## Session-Based Transcoder — Seek Finally Works Properly

We've fully switched to a session-based transcoder.

**The key change:** you can now seek instantly without waiting for FFmpeg to catch up.

**Before:**
- Seeking meant waiting until the transcoder processed the stream up to that point
- Painful on long videos

**Now:**
- A single FFmpeg process per session
- Proper seek support
- Near-instant jumping to any position

The old mode is gone — this is now the only path.

## Live Torrent Status — No More Guessing

The resource page now shows a real-time torrent status.

You can see:
- How much of the torrent is cached
- How many peers are connected
- Whether it's vaulted or not

So instead of guessing *"is it downloading or stuck?"* — you just see it.

## Why This Matters

**Seek** → removes a major UX pain point

**Status** → removes uncertainty

Together, this makes Webtor feel much less like a black box and more like a predictable tool.
