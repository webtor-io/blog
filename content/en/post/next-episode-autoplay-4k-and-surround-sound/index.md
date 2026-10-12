---
title: "The Next Episode Starts on Its Own, 4K and Surround Sound Stay as They Are — and a Friendlier Player"
description: "Webtor now moves to the next episode by itself, plays 4K HEVC and HDR in the original quality, keeps 5.1 and Dolby sound, and the player gets speed control, double-tap seek and subtitle delay. Plus a heads-up for sites that embed our player."
date: 2026-10-12T03:05:00+03:00
slug: "next-episode-autoplay-4k-and-surround-sound"
series: "What's new"
translationKey: "next-episode-autoplay-4k-and-surround-sound"
titleEmoji: ":clapper:"
---

Series now play one episode after another, 4K and surround sound reach you the way they were recorded, and the player picked up the controls it was missing. Plus a heads-up for anyone who embeds our player on their site.

## The Next Episode Starts on Its Own

Watching a series used to mean: the episode ends, you exit fullscreen, find the next file, press Watch. Now Webtor does it for you.

- When the credits start, an "Up next" card appears with a 10-second countdown. Do nothing and the next episode starts. Press Cancel if you'd rather stop.
- Webtor finds where the credits begin, so you don't sit through them waiting.
- Fullscreen stays on. The audio track and subtitles you picked come along to the next episode — an AI translation too.
- After three episodes in a row with no sign of you, the player asks "Still watching?" instead of playing all night.
- Want to pick the next one yourself? There's a Next button right after Play (or press N), and autoplay switches off in the new gear menu.

Albums work the same way: tracks play one after another, no pauses and no cards in between.

One more thing: an episode now counts as watched once the credits start. Episodes with long credits no longer stay "unfinished" forever.

## A Player That's Easier to Use

- **Playback speed** from 0.5x to 2x. The button shows the current speed, and the < and > keys work too.
- **Double-tap to skip 10 seconds** on your phone: tap the right half to go forward, the left half to go back. Tap faster to skip further.
- **Volume and speed are remembered.** No more turning the sound down every time.
- **Subtitles running early or late?** Shift them in 0.25-second steps right in the subtitle menu (or with the G and H keys). The fix is remembered for that file.
- **Lock screen and headphones.** Your phone's lock screen shows the title and poster, and the buttons on your headphones pause and skip.
- **Language without a restart.** If you haven't set a language in your profile, the player takes it from your browser — and you can change it right in the subtitle menu while the film keeps playing.

## 4K, HDR and Surround Sound — as They Are

Until now, videos in HEVC (x265) — the format most 4K releases use — were converted on our side before they reached you. That's slow, and 4K often didn't play at all.

Now, if your browser can play HEVC on its own, you get the original file with no conversion:

- **4K that used to be off-limits** plays in its original quality.
- **HDR stays HDR** on screens that support it.
- **Surround sound stays surround.** 5.1 and Dolby audio used to be squashed into stereo for every film — and about 40% of films have it. Now, if your device can play it, you hear it the way it was mixed.

On iPhone and iPad (iOS 17.1 and newer) video now plays a new way, and 4K HDR works there too. One trade-off: AirPlay isn't available in this mode for now.

If your device stumbles on a file, the player notices and switches back to the old way by itself — you don't have to do anything.

The Discover catalog knows about this too: new HEVC and HDR switches hide the releases your device can't play. And releases already sitting on our servers get an **Instant** badge and go to the top of the list — those start right away.

## See Where the Wait Is

The torrent status now shows the whole path: **swarm ▸ our servers ▸ you**, with the speed of each step and a bar of the parts already downloaded. If something is slow, you can see where.

And if the slow part is the swarm itself, we won't push a faster plan at you — it wouldn't help.

A few more things on the torrent page:

- Scroll down to the file list and the status follows you as a thin bar under the menu.
- A button you've pressed shows that it's working and can't be pressed twice by accident.
- Picking a file updates only the file section, not the whole page.

## The Embedded Player Leaves webtor.io on November 1

This one is for website owners who put the Webtor player on their site with our embed code. Embedding is being retired: **from November 1 it stops working through webtor.io.**

The embedded player stays in [self-hosted Webtor](https://github.com/webtor-io/self-hosted). If you need it, run your own copy and embed the player from there.

Nothing changes for anyone watching on webtor.io itself.

## Improved Stability

- If one of our servers hiccups mid-film, the player recovers by itself — without jumping back and without a spinner that only a page reload could fix.
- A dropped connection to our servers is noticed and restored much faster.
- A download no longer gets cut off just because one part of the file is arriving slowly.
- Files in your library are checked for damage, and broken copies are found and fixed.
- Signing in no longer fails with "unknown error" — the page reloads itself and lets you in.

Thanks for using Webtor. More coming soon.
