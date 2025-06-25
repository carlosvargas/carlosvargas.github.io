---
layout: post
date: 2025-06-25 07:23 +0800
title: Quoting Learnings from two years of using AI tools for software engineering
linkblog: true
tags: [llm]
image: https://substack-post-media.s3.amazonaws.com/public/images/94587a2c-3dc9-45e6-92ef-5705eaa64638_1600x1326.png
---

[The Pragmatic Engineer has a guest post](https://newsletter.pragmaticengineer.com/p/two-years-of-using-ai) from Birgitta Bockeler, Distinguished Engineer at Thoughtworks, where they talk about the evolution of the AI ecosystem in developing software. 

It’s a really good overview of how we got from “autocomplete on steroids” in 2021, to “autonomous background agents” in only 4 years. 

> This really clicked for me: generative AI tooling is not like any other software. To use it effectively, it’s necessary to adapt to its nature and embrace it. This is a shift that’s especially hard for software engineers who are attached to building deterministic automation. It feels uncomfortable and hacky that these tools sometimes work and other times don’t.
> Therefore, the first thing to navigate is the mindset change of becoming an effective human in the loop.

This is spot on. It’s hard to trust the tool when it doesn’t always work, but Burgitta provides some ways to improve this:

- Custom instructions about coding style and conventions, tech stack, domain, or just mitigations for common pitfalls the AI falls into. 
- Break down the work first into smaller tasks so that it’s easier execute the right changes in small steps, and you have a chance to review the direction the AI is going in and to correct it early, if needed.
- It’s much more effective to start new conversations frequently, and not let the context grow too large because the performance usually degrades.
- A concrete description which will lead to more success is something like, "add a new boolean field 'editable' to the DB, expose it through /api/xxx and toggle visibility based on that".
- Use a form of memory: A common solution to this is to have the AI create and maintain a set of files in the workspace that represent the current task and its context, and then point at them whenever a new session starts. The trick then becomes to have a good idea of how to best structure those files, and what information to include. [Cline's memory bank](https://docs.cline.bot/prompting/cline-memory-bank) is one example of a definition of such a memory structure.

I’ve read this online in multiple places, but it’s great to have it all laid out in one spot. 