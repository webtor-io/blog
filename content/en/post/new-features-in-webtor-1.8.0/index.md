---
title: "New features in Webtor 1.8.0"
date: 2020-12-24T00:20:00+03:00
series: "What's new"
translationKey: "v1.8.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.8.0/
---
Latest release of this year!

Here's a list of the key changes:

1. **The main page has been improved** - now there is a field for entering a magnet-link (by the way, now you can use just infohash).
2. **Resuming the download of the ZIP-archive after break** - now when downloading the ZIP-archive, the browser will display the full size of the downloaded archive, and you can also pause and resume downloading the archive from the same location.
3. **View video only via HLS** - now mp4 format is also converted to HLS on-the-fly. Thanks to this, it was possible
implement the ability to save bandwidth by sharing HLS-fragments via [WebRTC](https://webrtc.org/)
using the [p2p-media-loader](https://github.com/Novage/p2p-media-loader) library
([WebTorrent](https://github.com/webtorrent/webtorrent) had to be abandoned due to large delays at the beginning of playback).
4. **Added a lot of features to the player SDK** - now in the [SDK](https://github.com/webtor-io/player-sdk-js) you can specify
which elements of the player should be disabled. It became possible to stretch the player simultaneously in width and height by 100%.
5. **Switching between files in the player** - now you can switch between files within folder without leaving the player

Thank you for using [webtor.io](https://webtor.io/en/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!

Merry Christmas and Happy New Year! 🎄🎄🎄