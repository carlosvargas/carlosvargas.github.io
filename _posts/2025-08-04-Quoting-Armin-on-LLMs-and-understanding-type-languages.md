---
layout: post
date: 2025-08-04 18:33 +0800
title: Quoting Armin on LLMs and understanding type languages
linkblog: true
tags: [llm]
---

It turns out that LLMs are as adept as writing Typescript as I am. Which is to say, not very good at all. 

From Armin’s [In Support of Shitty Types](https://lucumr.pocoo.org/2025/8/4/shitty-types/), he says:
> This gets really bad when the types themselves are incredibly complicated and non-obvious. TypeScript has arcane expression functionality, and some libraries go overboard with complex constructs (e.g., [conditional types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)). LLMs have little clue how to read any of this. For instance, if you give it access to the .d.ts files from TanStack Router and the forward declaration stuff it uses for the router system to work properly, it doesn’t understand any of it. It guesses, and sometimes guesses badly. It’s utterly confused. When it runs into type errors, it performs all kinds of manipulations, none of which are helpful.

I’ve experienced this when having Claude Code write some Typescript. It doesn’t understand it and I have to end up fixing the most obscure errors. 

It seems that compiled languages might fared better (it’s been a while since I’ve worked with them):
> the types that Go has are rather strictly enforced. If they are wrong, it won’t compile. Because Go has a much simpler type system that doesn’t support complicated constructs, it works much better—both for LLMs to understand the code they produce and for the LLM to understand real-world libraries you might give to an LLM.
