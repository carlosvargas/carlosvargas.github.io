---
layout: post
date: 2025-03-29 09:00 +0800
title: Quoting Jacob Voytko in debugging Google Docs
linkblog: true
tags: []
---

Keeping up with the Google Docs theme, [Jacob Voytko goes into detail](https://www.clientserver.dev/p/war-story-the-hardest-bug-i-ever) how they once debugged an (initial) nondeterministic bug in Google Docs. 

> It was a fatal error. This means that it prevented the user from editing without reloading. It didn’t correspond to a Google Docs release. The stack trace added very little information. There wasn’t an associated spike in user complaints, so we weren’t even sure it was really happening — but if it _was_ happening it would be really bad.
> ….
> I do it a few more times. It’s not always the 20th iteration, but it usually happens sometime between the 10th and 40th iteration. Sometimes it never happend. Okay, the bug is nondeterministic. We’re off to a bad start

Errors like this are always fun to debug /s 

I really like the way they did it though. Using their automated tool and just constantly having it repeat something tedious over and over again. 

As for the resolution, you can clearly see the benefit of working at such a big company where they also built the platform where the bug is happening. 