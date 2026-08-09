---
title: "Pay With Crypto, Download Only What You Need — and Binge-Watching Fixed in Stremio"
date: 2026-08-09T12:00:00+03:00
slug: "crypto-payments-partial-downloads-and-stremio-fixes"
series: "What's new"
translationKey: "crypto-payments-partial-downloads-and-stremio-fixes"
titleEmoji: ":package:"
---

A summer batch of updates: a new way to pay, smarter folder downloads, a much better Stremio experience, and a bunch of fixes you'll feel right away.

## Pay With Crypto

You can now get a Webtor membership **with cryptocurrency** — straight from the [donate page](https://webtor.io/donate). Pick a plan, choose crypto at checkout, and pay with popular coins or stablecoins. The minimum depends on the coin, roughly from $12.

There's also a new **payment history** page in your profile, so you can always see what you paid and when. And if something goes wrong, we've published a clear [refund policy](https://webtor.io/legal/refund).

## Download Only the Files You Need

Downloading a folder no longer means downloading *everything* in it. There's a new **select mode** — tick the files you actually want, and Webtor packs just those into an archive. Grabbing two episodes out of a full season is finally a two-click job.

Folder downloads now come as **TAR by default** — it's more reliable for big folders, and every file inside checks out correctly after download. Prefer ZIP? It's still right there in the dropdown next to the download button.

## Binge-Watching in Stremio Works Now

If you watch through our Stremio addon, this one's for you:

- **The next episode actually plays.** Finishing an episode used to sometimes leave you hanging — now binge-watching rolls on to the next one like it should.
- **Resume works the next day.** Stopped mid-movie in the evening? Picking it up tomorrow works — no more mysterious failures on old links.
- **Your library loads faster and looks better.** Series in the library open noticeably quicker, and streams show proper titles and details instead of cryptic file names.

## A Getting-Started Checklist

New to Webtor? There's now a short **checklist on the home page** (with a counter in the top bar) that walks you through the essentials during your first two weeks: add something to your library, save a title on Discover, try the Vault, connect Stremio. Each step links straight to the right place — no hunting through menus.

## Your Library as a Cloud Drive

Alongside WebDAV, your library is now reachable over an **S3-compatible interface**. That means tools like rclone or Cyberduck can browse and sync your Webtor library like any cloud storage. Connection details and instructions are in your profile.

## Webtor Now Has an API — Build Your Own Apps on Top

A big one for developers: Webtor now serves a **full JSON API** at [api.webtor.io](https://api.webtor.io). Everything the site can do is available through it — resources, file listings, streaming, library, vault and profile.

That means you can now **build your own applications on top of Webtor**: a mobile client, a bot, a media center, an integration into your own service — anything that needs torrent streaming without running the infrastructure yourself. The heavy lifting stays on our side; you just call the API.

It ships with interactive docs where you can try every call right in the browser. Directory exports take new parameters too: choose the archive format and pass only the files you want.

## Fixes You'll Feel

- **Uploaded torrents that used to stall now start.** If you uploaded your own .torrent file and it just sat there — that's fixed.
- **Friendly error pages.** On the rare occasion something breaks, you get a clear page with a way forward instead of a bare error code.
- **Faster library browsing** and fewer background restarts — things just stay smooth for longer.

---

Thanks for using Webtor. More coming soon.
