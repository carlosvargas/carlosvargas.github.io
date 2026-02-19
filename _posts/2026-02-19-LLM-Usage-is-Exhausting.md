---
layout: post
date: 2026-02-19 06:35 +0800
title: LLM Usage is Exhausting
linkblog: true
tags: []
---

LLM Usage is Exhausting

> I'm frequently finding myself with work on two or three projects running parallel. I can get _so much done_, but after just an hour or two my mental energy for the day feels almost entirely depleted

- [Simon Willison](https://simonwillison.net/2026/Feb/9/ai-intensifies-work/) 

I'm used to context switching as part of my job, but I was just telling a coworker that because the LLM can reply within seconds, I find myself in a constant mode of high-intensity concentration. I'm perpetually reviewing code and architecting the next task. It's the same work we've always done, but now it's on a much more compressed timeline due to the sheer speed of the model. This means that I get tired much more quickly than before. 

Salvatore Sanfilippo - creator of Redis - [has discussed this as well](https://youtu.be/id9QG-mQSOo?si=9ONJZtBZ9Z2dLFvly), noting that he feels immense fatigue after just 4-5 hours of this type of work.


The [research paper](https://hbr.org/2026/02/ai-doesnt-reduce-work-it-intensifies-it) that Simon links to corroborates this:

> AI adoption can be unsustainable, causing problems down the line. Once the excitement of experimenting fades, workers can find that their workload has quietly grown and feel stretched from juggling everything that's suddenly on their plate. That workload creep can in turn lead to cognitive fatigue, burnout, and weakened decision-making.
> ...
> Some workers described realizing, often in hindsight, that as prompting during breaks became habitual, downtime no longer provided the same sense of recovery.
> ...
> While this sense of having a "partner" enabled a feeling of momentum, the reality was a continual switching of attention, frequent checking of AI outputs, and a growing number of open tasks. This created cognitive load and a sense of always juggling, even as the work felt productive.

Salvatore offers two tips to help us avoid burnout:
1. Take the initiative: Show the model what needs to be done and ensure you have a deep understanding of the solution, rather than letting the model figure it out and then trying to reverse engineer what it did during your review
2. One project at a time: Avoid the temptation to parallelize just because the AI is fast. Use the time while the LLM is "thinking" to stay deep in the current codebase. You can still use agentic mode for bug fixing or optimization, but for core work, we need to contribute more to the ideas without fracturing our context.

Now excuse me as I go tell my Claude Code and Codex running instances what to do. 