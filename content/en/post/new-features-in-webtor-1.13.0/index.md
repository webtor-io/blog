---
title: "New features in Webtor 1.13.0"
date: 2021-12-11T16:38:00+03:00
series: "What's new"
translationKey: "v1.13.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.13.0/
---
Here's a list of the key changes:

1. **️Resume download bug fixed** - now, in the case of a failure during downloading, resuming works correctly,
this applies to downloads of both individual files and downloads in a ZIP archive.

2. **Fewer drops and crashes** - earlier, during component releases, all downloads were interrupted, now they just pause
at the time of the update.

3. **Torrent files live forever** - previously torrent files were deleted after a certain time, now they are saved forever, this
allows less frequent access to the BitTorrent network and improves response time. (this does not apply to downloadable content!)

4. **Displaying download priority** - previously, when displaying download progress, only downloaded fragments were highlighted,
fragments that are loaded with high priority are now also highlighted.

5. **Improved interface responsiveness** - now the screen space on mobile devices is used more efficiently.

6. **Drag&drop works for subtitles** - now you can simply drag subtitles into the player window.

In addition, now the project has its own [Subreddit](https://www.reddit.com/r/webtor/), where we can discuss improvements and directions of the project development.

And for [WordPress](https://wordpress.org/) there is [a special plugin](https://github.com/webtor-io/wordpress-plugin) for
embedding webtor player to any WordPress blog!

Thank you for using [webtor.io](https://webtor.io/en/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!
