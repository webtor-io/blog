---
title: "New features in Webtor 1.12.0"
date: 2021-11-04T00:05:00+03:00
series: "What's new"
translationKey: "v1.12.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.12.0/
---
Here's a list of the key changes:

1. **️Progressive enhancement for video formats** - previously popular video-content was only cached to avoid the need of periodic
trnasmitting from the BitTorrent-network. Now the video is deferredly converted to various formats for optimal mobile playback
(adaptive bitrate streaming).
2. **Improved loading of cached HLS-fragments** - now cached fragments are loaded with lookahead, thus on request
the necessary fragment has already been preloaded to the edge-server from the main cache-storage.

Thank you for using [webtor.io](https://webtor.io/en/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!
