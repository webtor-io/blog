---
title: "How to Stream Torrents on Your Smart TV with Stremio + Webtor"
date: 2026-03-22T12:00:00+03:00
slug: "stream-torrents-smart-tv-stremio-webtor"
translationKey: "stream-torrents-smart-tv-stremio-webtor"
series: "Torrent Basics"
---

One of the most common requests we've received since launching [Stremio integration](/post/watch-your-torrents-on-tv-with-stremio) is: "How exactly do I set this up on my TV?"

Fair question. Smart TVs come in many flavors — Android TV, Fire Stick, Apple TV, Chromecast — and the setup varies slightly depending on what you have. This guide covers all of them.

By the end, you'll have Stremio running on your TV with your personal Webtor library connected, ready to stream torrents with a single click.

---

## What is Stremio?

If you haven't heard of it before, [Stremio](https://www.stremio.com) is a free media center app. Think of it as a universal interface for your content — it aggregates movies, shows, and other media from different sources into one place.

What makes Stremio powerful is its **addon system**. Addons extend Stremio with new content sources, and anyone can create one. Webtor provides a personal addon that connects your Webtor library to Stremio, so your saved torrents show up as a media catalog with proper metadata, posters, and episode information.

---

## What you need before starting

- A **Webtor account** (the Stremio addon connects to your personal library)
- A **Stremio account** (free, create one at [stremio.com](https://www.stremio.com))
- Some **torrents added to your Webtor library** — movies, shows, whatever you want to watch
- Your **TV or streaming device** connected to the internet

---

## Setting up Stremio on your device

### Android TV (Sony, Philips, Xiaomi, Nvidia Shield, etc.)

Android TV has native Stremio support.

1. Open the **Google Play Store** on your TV
2. Search for **Stremio**
3. Install it and sign in with your Stremio account

That's it — Stremio runs natively on Android TV and the experience is smooth.

### Amazon Fire Stick / Fire TV

Fire Stick runs a modified Android, so Stremio works but isn't available directly in the Amazon App Store. You'll need to sideload it.

1. On your Fire Stick, go to **Settings > My Fire TV > Developer Options**
2. Enable **Apps from Unknown Sources** (or "Install Unknown Apps" on newer models)
3. Install the **Downloader** app from the Amazon App Store
4. Open Downloader and enter the URL: `https://www.stremio.com/downloads`
5. Download the Android APK and install it
6. Open Stremio and sign in

Alternatively, you can use **adbLink** from a computer to push the APK to your Fire Stick.

### Apple TV

Stremio is available on the Apple TV App Store.

1. Open the **App Store** on your Apple TV
2. Search for **Stremio**
3. Install and sign in with your Stremio account

### Chromecast / Google TV

If you have a Chromecast with Google TV (the one with a remote), you can install Stremio directly from the Play Store — follow the Android TV steps above.

For older Chromecast models without Google TV, you can **cast from your phone**:

1. Install Stremio on your Android phone or iPhone
2. Start playing content in Stremio
3. Use the cast button to send it to your Chromecast

---

## Connecting your Webtor library to Stremio

Once Stremio is running on your TV, the next step is adding your personal Webtor addon.

### Step 1: Add torrents to your library

Go to [webtor.io](https://webtor.io), sign in to your account, and add some torrents to your library. Movies and TV shows work best — Webtor will try to detect metadata automatically. Note: adding to your library is enough for Stremio — Vault is a separate feature for long-term cloud caching.

### Step 2: Get your personal addon link

Visit the [Stremio setup page](https://webtor.io/instructions/stremio) on the Webtor website. You'll see a personalized addon URL that's unique to your account.

### Step 3: Install the addon in Stremio

There are two ways to do this:

**Option A: From your phone or computer**
Open the addon URL in a browser. It will ask to open Stremio — confirm, and the addon will be installed. Since Stremio syncs addons across devices, it will automatically appear on your TV.

**Option B: Directly on TV**
In Stremio on your TV, go to the **Addons** section, search for your addon, or paste the URL in the addon search field.

### Step 4: Watch

Go to the Stremio home screen. You should now see your Webtor library content. Select a movie or episode, and streaming starts immediately.

---

## What to expect

- **Automatic metadata.** Webtor detects movie and show information from your torrent content. You'll see proper titles, posters, and episode listings.
- **Real-time transcoding.** Video is converted on the fly to a format your device can play. No need to worry about MKV vs MP4 compatibility.
- **Subtitle support.** If your torrent includes subtitle files, they're converted and available in the Stremio player.
- **Seek and skip.** You can jump to any point in the video just like with any streaming service.

---

## Troubleshooting common issues

### Stremio shows "No streams available"

- Make sure the torrent is added to your Webtor library (not just opened once).
- Check that your Webtor subscription is active.
- Try removing and re-adding the addon.

### Video buffers frequently

- Check your internet connection. Streaming requires a stable connection — at least 10 Mbps for HD content.
- If the torrent has very few seeders, initial buffering may be longer. Webtor handles the torrent download, but rare content takes more time to start.

### Addon doesn't appear on TV

- Make sure you're using the **same Stremio account** on both your phone/computer and your TV.
- Stremio syncs addons automatically, but it may take a minute. Try restarting Stremio on your TV.

### Subtitles don't show up

- Check if the torrent actually contains subtitle files (.srt, .ass, .sub).
- In the Stremio player, look for the subtitle toggle — it may not be enabled by default.

---

## Why this matters

For years, the typical flow for watching torrents on TV was painful:

1. Find the torrent
2. Download it to a computer
3. Transfer to a NAS or USB drive
4. Set up Plex or similar media server
5. Finally watch

With Webtor + Stremio, this becomes:

1. Add a torrent to your library
2. Open Stremio on your TV
3. Watch

No NAS, no media server, no file transfers. Just torrents playing on your TV like any other streaming service.

---

## Final thoughts

Setting up Stremio with Webtor takes about five minutes, and once it's done, you have a personal streaming service powered by your own torrent library. It works on Android TV, Fire Stick, Apple TV, and Chromecast — essentially any screen in your house.

If you haven't set up Stremio yet, start here:
[Stremio setup instructions on Webtor](https://webtor.io/instructions/stremio)

And if you don't have a Webtor account yet, [sign up at webtor.io](https://webtor.io) — streaming through Stremio requires a paid plan (starting at $2/mo).
