---
layout: post
date: 2025-03-01 06:41 +0800
title: The Software Engineer Spectrum Speed vs. Accuracy
linkblog: true
tags: [career]
---

[Ben Howdle has a good post](https://benhowdle.im/software-engineer-spectrum.html) talking about this. 

> Over the years, I've spotted a pattern: _all engineers exist on a spectrum between speed and accuracy_.
> 
> This spectrum isn't about skill or seniority—it's about how engineers naturally approach their work. Some lean towards _speed_, optimizing for fast iteration and progress, while others prioritize _accuracy_, ensuring long-term maintainability and scalability.
> 
> Neither end of the spectrum is "better" than the other, but knowing where you sit—and understanding what kind of engineer your company actually needs—can be the difference between thriving in a role or feeling completely out of sync.

This is an interesting insight. I feel that my role requires both of these. Somewhere in the between what he calls the “Scaling Startup” and “Enterprise”, which is where Scribd as a company is at right now. 

I need to look at the current goals that we have and see if we can deliver them fast without introducing tech debt. If it’s a quick experiment, doing it fast and breaking *some* things is fine. We work with subscriptions, so breaking them is a no-go. But launching quick AB tests around other parts around checkout is OK to do fast. We can clean them up based on the results. 

At the same time, because we’re talking about subscriptions, plans and features, I’m always thinking about how to support those in a maintainable and scalable manner. This includes dealing with tech debt from the past few years. Which requires moving slower on some things to make sure we’re making the right architectural tradeoffs. 

And I enjoy this. Living both worlds. It’s not easy and it has a lot of challenges, but I find it rewarding. 