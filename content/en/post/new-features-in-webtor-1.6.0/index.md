---
title: "New features in Webtor 1.6.0"
date: 2019-12-14T16:52:00+03:00
series: "What's new"
translationKey: "v1.6.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.6.0/
---
This release was mainly focused on stability and fixing performance issues of the service.

The most affected component was transcoding. Here is a short list of changes:

1. **Dropped HEVC-support** - transcoding from HEVC(x265) to h264(x264) is a really heavy lifting that freezes work of whole service.
2. **Dropped "fast forward" functionality** - now transcoding starts always from the beginning. It makes possible to just repack stream
to HLS instead of "real transcoding". This change also dramatically insreases quality of h264-based video. Also "fast forward" freezes
sometimes and looks quite unreliable.

Here we see an example of reducing features in favor of image quality and service stability.

Here is a list of newly opensourced components:

* [torrent-web-seeder](https://github.com/webtor-io/torrent-web-seeder) - wrapper around BitTorrent-client
* [content-transcoder](https://github.com/webtor-io/content-transcoder) - transcodes HTTP-stream to HLS
* [torrent-store](https://github.com/webtor-io/torrent-store) - temporary torrent storage with Redis backend and GRPC access
* [magnet2torrent](https://github.com/webtor-io/magnet2torrent) - magnet-uri to torrent converter as GRPC-service

Thank you for using [webtor.io](https://webtor.io/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!