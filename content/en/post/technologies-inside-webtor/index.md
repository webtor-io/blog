---
title: "Technologies inside Webtor.io"
date: 2019-10-30T21:47:00+03:00
series: "What's inside"
translationKey: "technology"
aliases:
    - /en/technology/
---
{{< figure src="/images/technologies-inside-webtor/kittens.jpg" >}}
Periodically, my users are interested in what technologies **Webtor** is based on,
whether I use library A or tool B. This time I want to fully answer all questions.

To begin with, **Webtor** has made a 3-year-long journey from a monolithic application living on a dedicated server
to the introduction of microservices, containerization, and moving to the [Kubernetes (k8s)](https://kubernetes.io/) cluster.
Currently, about 10 different services are running in the cluster and 100+ simultaneous jobs are running
for downloading torrents and transcoding content.

Next, go through the frequently asked questions.

## What is Webtor written on?
Almost the entire backend is built on [Go](https://golang.org/). In fairness, the first prototype was
on [Node.js](https://nodejs.org), but this venture turned out to be a failure.
Go allowed more efficient use of resources and withstand more users.
It can be said, that the transition to Go and Kubernetes became the key technical solutions for the project.
[Vue.js](https://vuejs.org/) was selected for the frontend.

## How does torrent download work? Is it based on WebTorrent?
Unlike many other services **Webtor** is built in such a way to 
provide instant access to content without waiting for the full download to finish.
Content saved to disk for caching purpose only and deleted in 5 minutes after the last access.
As the torrent client the go-library [anacrolix/torrent](https://github.com/anacrolix/torrent) is used.
It provides the ability of sequential download and streaming of still underloaded content.
For each new torrent, a separate container in the cluster is launched, this allows
achieve maximum process isolation and high scalability of the system.

## FFmpeg is used for conversion, right?
I'll start a little from afar.

Probably the most difficult challenge awaited me here. It was necessary to give users
the ability to play still underloaded avi/mkv/flac files as they used to
do it earlier, with the ability to rewind to the desired position, with choice of subtitles and audio tracks.
I did not find any ready-made solutions, so I had to reinvent the wheel.

So how does it work. Transcoding begins with determining the duration of the content. Based on this duration
a full HLS-playlist is generated with records of still non-existent 10 second fragments. When any of these fragments
is accessed the new [FFmpeg](https://www.ffmpeg.org/) process is launched to
convert the necessary fragment (in this case, only the necessary part of the torrent is downloaded).
As soon as the fragmnet is converted, it is sent to the user. If the user suddenly rewound to another section,
then the current FFmpeg process "falls asleep", and somewhere already starts a new one. If the user came back, then the old
process located nearby "wakes up" and continues its work. In the end, you get a whole seamless video.
And yes, each conversion also runs in a separate container.

Under ideal conditions, video with a low resolution (720p) and a sufficient number of peers is converted
without tangible delays.

## I want to install Webtor on my server, how do I do this?
Slowly but surely, work is underway to opensource the project. At the end, everyone can
install **Webtor** into their Kubernetes cluster.

Thank you for using [webtor.io](https://webtor.io/) and [sponsor it](https://www.patreon.com/bePatron?u=24145874) if you wish!