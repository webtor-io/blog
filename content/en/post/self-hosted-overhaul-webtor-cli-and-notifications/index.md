---
title: "Self-Hosted Webtor Reborn, a New Command-Line App — and Notifications on the Site"
description: "The first self-hosted update in nine months brings everything webtor.io has — plus a master password and ARM support. Also new: the webtor command-line app and in-app notifications."
date: 2026-08-28T11:30:00+03:00
slug: "self-hosted-overhaul-webtor-cli-and-notifications"
series: "What's new"
translationKey: "self-hosted-overhaul-webtor-cli-and-notifications"
titleEmoji: ":rocket:"
---

The biggest batch of updates this year: a completely reworked self-hosted version, a brand-new terminal app, and notifications that finally live on the site instead of just your inbox.

## Self-Hosted, Completely Reworked

If you run [your own Webtor](https://github.com/webtor-io/self-hosted), this is the update you've been waiting for — the first in nine months, and by far the biggest ever.

**Everything webtor.io can do, your instance can do now.** The library, long-term Vault storage, the notification feed, Stremio, WebDAV and S3 access — the self-hosted version is no longer a lite edition. It's the same Webtor, on your hardware. AI recommendations and movie & series recognition via TMDB — with posters and descriptions in your language — plug in too; each just needs your own API key.

**A master password.** Set one, and your instance is yours alone: the site asks for the password before showing anything, and you manage it right from the profile page. Perfect for a box that's reachable from the internet.

**It runs on ARM now.** Raspberry Pi, ARM servers, Apple Silicon — one Docker image covers them all. A Pi in the corner of your room can be a full Webtor.

Smaller but sweet: MKV files now start playing properly, and the image is assembled from ready-made parts — so updates ship faster from now on.

## Meet webtor-cli

Webtor now lives in your terminal too. The new [webtor](https://github.com/webtor-io/webtor-cli) app streams and downloads torrents over plain HTTP — no torrent client, no waiting for the whole file:

```console
$ webtor play "magnet:..."   # straight into VLC
$ webtor download <id>       # resumable
$ webtor library             # library in the terminal
```

It's a real app, not just commands: run `webtor` bare and you get interactive menus — browse your library and Vault, pick files, start downloads in the background, pause and resume them. The mouse works. Finished downloads pop a desktop notification.

It talks to your webtor.io account (a one-time code logs the terminal in, like GitHub's CLI), to RapidAPI, or to your own self-hosted instance.

Installing takes one line:

```console
$ brew install webtor-io/tap/webtor
```

Prebuilt binaries for Linux, macOS and Windows — plus a Docker image — are on the [releases page](https://github.com/webtor-io/webtor-cli/releases/latest).

## Notifications, Right on the Site

There's a bell in the top bar now. Vault warnings — "your file expires in 7 days" — and other account events show up there and on a notifications page, with an unread counter and a mark-all-read button. Before, all of this went to email only; now email is the backup, not the front door. Your past email notifications are in the feed too, so the history is in one place.

## Emails in Your Language

Every email Webtor sends — Vault reminders, address verification — now arrives in the language your account uses. Eleven languages, not just English.

## For Developers: a Go SDK

The [official Go SDK](https://github.com/webtor-io/api-sdk-go) for the Webtor JSON API is out — it's what the CLI is built on. Logging in, storing torrents, resumable downloads, library access: all a few lines of Go.

## Improved Stability

- Fixed a rare bug that could put corrupted fragments into a video mid-stream. If you ever saw a brief burst of glitches, that's gone.
- A stream that keeps failing now stops cleanly instead of silently retrying forever.
- Lots of small interface fixes — the notifications page behaves on phones, and navigation no longer occasionally blanks the page.

## Webtor Turned 8

One more thing: on August 26, Webtor turned eight. The [first version](https://web.archive.org/web/20180826163118/https://webtor.io/) went live on August 26, 2018 — a single page with one simple promise: watch torrents online. Eight years later it's a player, a library, long-term storage, Stremio, a terminal app and a version you can run entirely on your own hardware. Thanks for being around all this time.

More coming soon.
