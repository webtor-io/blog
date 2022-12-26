---
title: "New features in Webtor 1.16.0"
date: 2022-12-26T21:34:00+03:00
series: "What's new"
translationKey: "v1.16.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.16.0/
---
Last release of the year!

The outgoing year was extremely difficult for the project. In addition to development, it was necessary
resolve issues related to finding a new hosting and payment methods. But luckily, it's over now! 😆😆😆

So, the list of changes (as usual):

1. **Shorter time to download** - earlier, before the start of the download, a new torrent client was launched, which could
take 5-10 seconds, and only after that the search for peers and the actual download itself began. Now, a certain number of
torrent clients are working in the cluster all the time, which can process several torrent downloads simultaneously, this
made it possible to remove just those 5-10 seconds necessary for a cold start.
2. **Long-lasting cache** - earlier, if no one accessed the torrent client, then after 10 minutes it turned off and all
downloaded data disappeared with it. Now data is deleted only if there is no room left on the server and only the oldest
unused files are deleted. This allows to save the downloaded information for a longer period.

Work has begun on the next version of the web interface, more details can be found on
[its repository page](https://github.com/webtor-io/web-ui-v2).

Thank you for using [webtor.io](https://webtor.io/en/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!

Merry Christmas and Happy New Year! 🎄🎄🎄