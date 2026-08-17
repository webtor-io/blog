---
title: "Smarter Library With AI Matching"
description: "Webtor's library now uses AI to identify movies and shows behind cryptic torrent names, match episodes in packs, and split anthology releases."
date: 2026-05-18T19:00:00+03:00
slug: "smarter-library-with-ai-matching"
series: "What's new"
translationKey: "smarter-library-with-ai-matching"
titleEmoji: ":brain:"
---

Your Webtor library got a lot smarter — it now uses AI to make sense of cryptic torrent names and identify what's actually inside.

## AI in Your Library

When a torrent name is too messy for the regular parser to handle, **AI now steps in and fills in the missing pieces** — the real title, year, and type. Files that used to show up as cryptic strings now appear as the actual movie or show.

Two more things changed alongside that:

- **Series and episode packs** — episodes inside multi-episode releases are matched up correctly, with proper season and episode numbers
- **Anthology torrents** — when a torrent is actually a bunch of separate films packed together, it's split into individual movies instead of being treated as one weird release

The result: less junk, cleaner titles, fewer "what is this file?" moments.

## Faster AI Chips on Discover

The AI chips on Discover used to greet you with a small lag — we waited for the whole batch to finish before drawing anything. Now chips **show up one by one as they're ready**, so the first one appears almost immediately when you open Discover or change your query.

There's also a new **refresh button** right next to the chips — tap it for a fresh set of suggestions without retyping your question.

Clicking a chip works immediately too, even while more are still appearing.

## Faster Playback During Vault Uploads

When you upload a torrent to your Vault, each file is now playable **as soon as that file is done** — you don't need to wait for the whole torrent to finish. Big movie packs feel a lot more responsive.

## Soft Limits on Link Sharing

Streaming links are now tied a bit more tightly to your session. You won't notice anything during normal viewing — but if a link gets scraped or shared widely, it'll hit a wall a lot sooner.

The current limits per session:

- **30** total concurrent streams
- **5** different IP addresses
- **10** concurrent connections to the same file
- **5** large files in parallel from the same torrent

Regular viewing sits well below all of these.

## Improved Stability

A bunch of small fixes that you won't see directly but will feel — fewer disconnects on long sessions, faster recovery when a backend pod restarts, and a few rare crash conditions in the seeder are gone.

---

Thanks for using Webtor. More coming soon.
