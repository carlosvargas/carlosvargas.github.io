---
layout: post
date: 2025-03-15 13:55 +0800
title: Thoughts on Armin’s Ugly Code and Dumb Things
linkblog: true
tags: [eng]
---
A few weeks ago [Armin Ronacher](https://lucumr.pocoo.org/about/) wrote a post about [Ugly Code and Dumb Things](https://lucumr.pocoo.org/2025/2/20/ugly-code/), where he expands that you can’t always build real life products on top of clean, sparkling codebases. You have to sometimes just do the ugly dirty hack, to be able to launch. 

> Perfect code doesn't guarantee success if you haven't solved a real problem for real people. Pursuing elegance in a vacuum leads to abandoned side projects or frameworks nobody uses. By contrast, clunky but functional code often comes with just the right compromises for quick iteration. And that in turn means a lot of messy code powers products that people love — something that's a far bigger challenge.

This is something that I’ve been discussing with my team lately. If we’re going to run a quick experiment, let’s do it fast and dirty (without compromising security and too much performance). If it succeeds, we will be able to build it in a more scalable way. But the key thing is that we could launch something much faster, so that we can realize if it’s worth it to focus on it long term. 

This is in contrast to when you’re building a framework or foundry that other people will depend on:

> But it took me years to fully realize what was happening here: reusability is not that important when you’re building an application, but it’s crucial when you’re building a library or framework.

And the final conclusion:

> At the end of the day, where you stand on “shitty code” depends on your primary goal:
> 
>  * Are you shipping a product and racing to meet user needs?
>  * Or are you building a reusable library or framework meant to stand the test of time?
> 
> Both mindsets are valid, but they rarely coexist harmoniously in a single codebase. Flamework is a reminder that messy, simple solutions can be powerful if they solve real problems. Eventually, when the time is right, you can clean it up or rebuild from the ground up.