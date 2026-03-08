---
layout: post
date: 2026-03-08 05:48 -0700  
title: TIL Meta's Use of FFmpeg
linkblog: true
tags: [til]
---
The [Meta blog has a good post](https://engineering.fb.com/2026/03/02/video-engineering/ffmpeg-at-meta-media-processing-at-scale/) about their usage of FFmpeg and how their years long fork managed to get merged back into the official repo:

> Meta executes ffmpeg (the main CLI application) and ffprobe (a utility for obtaining media file properties) binaries tens of billions of times a day, introducing unique challenges when dealing with media files. FFmpeg can easily perform transcoding and editing on individual files, but our workflows have additional requirements to meet our needs. For many years we had to rely on our own internally developed fork of FFmpeg to provide features that have only recently been added to FFmpeg, such as threaded multi-lane encoding and real-time quality metric computation.
> 
> Over time, our internal fork came to diverge significantly from the upstream version of FFmpeg. At the same time, new versions of FFmpeg brought support for new codecs and file formats, and reliability improvements, all of which allowed us to ingest more diverse video content from users without disruptions. This necessitated that we support both recent open-source versions of FFmpeg alongside our internal fork. Not only did this create a gradually divergent feature set, it also created challenges around safely rebasing our internal changes to avoid regressions.
> 
> As our internal fork became increasingly outdated, we collaborated with FFmpeg developers, FFlabs, and VideoLAN to develop features in FFmpeg that allowed us to fully deprecate our internal fork and rely exclusively on the upstream version for our use cases. Using upstreamed patches and refactorings we've been able to fill two important gaps that we had previously relied on our internal fork to fill: threaded, multi-lane transcoding and real-time quality metrics.