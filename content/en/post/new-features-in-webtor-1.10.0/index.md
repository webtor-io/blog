---
title: "New features in Webtor 1.10.0"
date: 2021-05-01T21:00:00+03:00
series: "What's new"
translationKey: "v1.10.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.10.0/
---
Here's a list of the key changes:

1. **Badge with heart ❤️** - now every backer can see their status in the top menu.
2. **Easier to share links** - now you can generate direct links like `https://webtor.io/%infohash%` or `https://webtor.io/%magnet-uri%`.
The ability to generate them from the interface has also been added, just click "Share link".
3. **Player embed code generation** - now the "`</>`", appears in the video player, which allows you to generate
a code for inserting the player on your website or blog.
4. **Displaying the transcoding process** - now the player shows the progress of transcoding, and the time rail hightlights already transcoded fragment.
5. **External subtitles are also available for mobile devices** - previously, when selecting OpenSubtitles  they did not play on mobile devices,
but now it is working.
6. **Transcoding errors are visible** - now if a transcoding error occurs, its cause is immediately displayed in the player window.

Also in the [player SDK](https://github.com/webtor-io/player-sdk-js) an alternative method for initializing the player was added,
now you can simply embed the script and specify the Magnet-URI in the `<video>` tag:
```
<video controls src="magnet:?xt=urn:btih:08ada5a7a6183aae1e09d831df6748d566095a10&dn=Sintel"></video>
<script src="https://cdn.jsdelivr.net/npm/@webtor/player-sdk-js/dist/index.min.js" charset="utf-8" async></script>
```

Thank you for using [webtor.io](https://webtor.io/en/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!
