---
title: "New extension for Google Chrome Webtor.io 0.1.10"
date: 2019-08-03T00:13:37+03:00
series: "What's new"
translationKey: "chrome-ext-0.1.10"
titleEmoji: ":tada:"
aliases:
    - /en/chrome-ext-v0.1.10/
---
This minor update solves annoying problem with automatic opening of downloaded torrent-files on several sites ([yts.am]({{< relref "/post/watch-movies-online-from-yts.am/index.md" >}}) for example).

To make it working we need to check that "Allow Access to file URLs" option is enabled. Follow these steps:

0. We need to be sure that [Webtor.io extension](https://chrome.google.com/webstore/detail/webtorio-watch-torrents-o/ngkpdaefpmokglfnmienfiaioffjodam) is already installed.
1. Go to Google Chrome's extensions page {{< figure src="step1.png" >}}
2. Find Webtor.io extension and click "Details" {{< figure src="step2.png" >}}
3. Option "Allow Access to file URLs" should be activated {{< figure src="step3.png" >}}

After accomplishing these steps you should not meet any problems with opening of downloaded torrent-files. 