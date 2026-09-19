---
title: "A Brand-New Subtitle Menu and AI Translation Into Your Language — While You Watch"
description: "We rebuilt the subtitle menu from scratch and added automatic AI translation: if there are no subtitles in your language, Webtor translates them for you. Plus an honest torrent status and clearer errors."
date: 2026-09-19T10:40:00+03:00
slug: "ai-subtitle-translation-and-new-subtitle-menu"
series: "What's new"
translationKey: "ai-subtitle-translation-and-new-subtitle-menu"
titleEmoji: ":speech_balloon:"
---

We rebuilt the subtitle menu from scratch and added automatic AI translation. The rest of this update is about always knowing what your torrent is up to.

## AI Subtitle Translation

You know the story: you found the movie, but the only subtitles are in English. Or Korean. That's no longer a problem — Webtor translates them into your language.

Here's how it goes:

- Start the movie. If there are no subtitles in your language, an offer shows up right on the picture: "Translate to Spanish".
- One click and it's running. You don't wait for the whole film — subtitles appear as you watch, with the translation staying a little ahead of you.
- Jumped to a part that isn't translated yet? The player holds the film for a few seconds and carries on with subtitles in place. If the translation falls behind, a small note at the top lets you wait for it or keep watching.
- Come back the next day and the translation is still there. Nothing to start again.

Any subtitles can be translated: the ones built into the file, the ones sitting next to it in the torrent, or the ones found on OpenSubtitles. A translation never starts on its own — only when you ask for it.

The language comes from your settings: pick a preferred language in your profile, and that's the one Webtor offers.

AI translation is available on paid plans. On the free plan you'll see the track with a little lock — and if the offer gets in your way, you can turn it off for good.

## The Subtitle Menu, Rebuilt

The old menu was a list you had to dig through. The new one fits on a single screen:

- **Languages as buttons with flags.** Audio and subtitles side by side, and the row opens right at your language.
- **You can see where a track came from.** From the file, from OpenSubtitles, your own upload or an AI translation — each has its own mark.
- **A real off switch.** Subtitles turn off with one toggle, not an "Off" item buried somewhere in the list.
- **Your files at hand.** Uploaded subtitles live right there, and you can delete them one by one. Upload a file and it switches on immediately.
- **Click outside to close.** A small thing, but it was missing.

## Subtitles Are Found More Often — and Fit Better

The OpenSubtitles search got smarter. Webtor first looks for subtitles made for your exact file — those line up to the second. If there are none, it searches by the movie or the specific episode, and puts the best matches first. When a track was matched by title rather than by file, the menu says so.

A few more things:

- ASS/SSA subtitles work now, not just SRT. Anime fans will notice.
- "Forced" tracks — the ones that only translate signs and foreign-language lines — are labelled and no longer get picked instead of full subtitles.
- Your choice sticks: switch the audio track and the subtitles stay on.

## An Honest Torrent Status

The badge on the torrent page used to say very little. Now it tells you what's going on at a glance: checking, loading, paused, or simply no seeders. Next to it is the download speed, and below it a bar showing which parts of the file are already there.

If a video doesn't start, Webtor tells you what went wrong instead of just "try again". And the support form already knows which torrent you're asking about — no need to copy a link.

## Magnet Links: Fewer Dead Ends

A magnet with nobody online used to end in a dry error. Now there's a countdown while you wait, and if the torrent still can't be found you get a card that explains why and offers a longer wait — up to 10 minutes. Rare torrents often turn up on the second try.

Magnets are found more often, too: Webtor now looks for them across more trackers, even when the link has none at all.

## Stremio in One Click

The Stremio addon now installs with a single button from your profile — no link copying. And after you pay for a plan, you get a proper welcome email: where to start, when the trial ends, and when the next charge is. Your profile also shows who handles the billing and where to manage it.

## Small Things and Stability

- The "I'm not a robot" check now only shows up if you're not signed in. Sign in and you won't see it again.
- In fullscreen the cursor hides itself, and the subtitle menu opens over the video instead of kicking you out.
- After a seek, the player no longer replays a bit from the previous spot.
- An interrupted file download resumes properly from where it stopped.
- Archives with lots of small files download more smoothly, without long pauses.
- More video and audio formats play.
- File sizes are counted the same way on every page.
- Profile and notifications no longer spill past the edge of a phone screen.
- Subscribed to new episodes without an account? The subscription completes itself once you sign in.
- [Self-hosted](https://github.com/webtor-io/self-hosted) gets AI translation and OpenSubtitles search too — each needs its own API key.

Thanks for using Webtor. More coming soon.
