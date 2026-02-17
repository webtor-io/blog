---
title: "New features in Webtor 1.7.0"
date: 2020-05-27T22:59:00+03:00
series: "What's new"
translationKey: "v1.7.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.7.0/
---
It has been quite a while since the previous release, but it was worth it!

Here is a list of key changes:

1. **Player SDK is already available!** - Now you can embed the playback of torrent content in any site without extra effort. SDK with an example
usage [published to Github](https://github.com/webtor-io/player-sdk-js).
2. **Interface for selecting and displaying subtitles improved** - it became much easier to select subtitles from a large list, as well as the opportunity
to change subtitle size on the fly.
3. **Dark mode by default** - now the main color scheme of the interface is solved in dark shades by default. They say it protects our eyes!
4. **Caching of downloaded content improved** - now all downloaded content is saved for a day and does not require re-downloading from the BitTorrent network.
5. **WebRTC support** - if several users watch the same movie, then they exchange fragments of it by the [WebRTC](https://webrtc.org/) protocol.
This uses a private tracker. Only MP4 is currently supported.
This was made possible thanks to the [WebTorrent](https://github.com/webtorrent/webtorrent) project.

Now all server components of the Webtor platform and SDK are available opensource:

* [github.com/webtor-io](https://github.com/webtor-io) - all opensources repositories
* [github.com/webtor-io/helm-charts](https://github.com/webtor-io/helm-charts) - all Helm-charts and installation instructions for Webtor API
* [github.com/webtor-io/platform-sdk-js](https://github.com/webtor-io/platform-sdk-js) - client-side JS SDK to work with API Webtor 
* [github.com/webtor-io/platform-sdk-php](https://github.com/webtor-io/platform-sdk-php) - server-side PHP SDK to work with API Webtor (functionality is limited)

Thank you for using [webtor.io](https://webtor.io/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish