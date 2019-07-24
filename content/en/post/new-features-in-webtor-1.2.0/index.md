---
title: "New features in Webtor 1.2.0"
date: 2019-09-04T20:02:00+03:00
series: "What's new"
translationKey: "v1.2.0"
titleEmoji: ":tada:"
aliases:
    - /en/v1.2.0/
---
Here is a list of new features:

1. **Open magnet-urls** - now it is possible to open magnet-url with "Open torrent online" button.
There's a special arrow near the "Open torrent online" button. After a click on it you will find a list of recent torrents and also field for pasting magnet-url.
After pasting of valid url there will open the a window with the torrent.
File list may not appear right away, it takes time to fetch torrent-file from the peers.
2. **Real progress bar** - earlier progress bar shows only what portion of file was downloaded (downloaded bytes from total). But now it shows what specific pieces of file were downloaded (beginning, middle or end). It represents real status of the torrent pieces.
3. **External subtitles encoding detection** - earlier there was a problem with usage of SRT-subtitles with encoding that differs from UTF-8, part of the symbols (or whole of them) might be corrupted.
Now original subtitle encoding is detected automatically and subtitles are converted to WebVTT with UTF-8 encoding.
4. **Feedback form** - now you have an opportunity to write feedback about any issue occurred, also you can just suggest any new feature with our new [feedback form](https://webtor.io/en/support).

Thank you for using [**webtor.io**](https://webtor.io/en/)!