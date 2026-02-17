---
title: "Redesign and other cool features"
date: 2026-02-17T21:00:00+03:00
series: "What's new"
translationKey: "redesign-and-cool-features"
titleEmoji: ":tada:"
---
The web interface got a fresh redesign! We've reworked many components to make everything look and feel more polished — cleaner layout, more pleasant visuals, better responsiveness on mobile devices. But the redesign isn't just about looks, it also brought a bunch of important improvements under the hood:

1. **Toast notifications** - now when you perform actions like copying a link, adding to library, or deleting an item, you'll see a neat notification popup confirming the action. Earlier, there was no visual feedback for many of these actions and you had to guess whether your click actually did something. Now you get clear success, error, or info messages that appear briefly and disappear on their own.
2. **Status icons in progress log** - the progress log that shows during file processing now uses clear visual icons: a checkmark for completed steps, a cross for errors, and a warning sign for warnings. Earlier, the status was shown as text labels like `[done]` or `[error]`, which was harder to read, especially on mobile.
3. **Smoother video playback start** - earlier, when you started watching a video, the player could stutter or buffer during the first moments while the transcoder was warming up. Now the system pre-buffers up to 5 minutes of HLS video segments right after the transcoder starts, ensuring smooth playback from the very first second.
4. **Automatic restart of failed jobs** - earlier, if a background job (like transcoding or downloading) failed with an error, it would stay in that error state and you had to trigger it again manually. Now errored jobs automatically restart when re-requested, so you don't have to worry about stale failures.

Thank you for using [webtor.io](https://webtor.io/en/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!
