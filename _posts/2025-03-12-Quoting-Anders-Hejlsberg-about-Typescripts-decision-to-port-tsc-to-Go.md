---
layout: post
date: 2025-03-12 07:16 +0800
title: Quoting Anders Hejlsberg about Typescript’s decision to port tsc to Go
linkblog: true
tags: [eng]
---
The Typescript team just announced a rebuild of the typescript compiler in Go. It [promises close to x10 speed improvements](https://devblogs.microsoft.com/typescript/typescript-native-port/) However, the internet being the internet, took to complaining about why they used Go instead of C#, that Microsoft was abandoning .NET, etc. 

Here’s a [GitHub Discussion thread](https://github.com/microsoft/typescript-go/discussions/411#discussioncomment-12466988) about this, but the highlight is Anders’ comment (buried under all the noise at time of posting) about why Go made the most sense:

> Our decision to port to Go underscores our commitment to pragmatic engineering choices. Our focus was on achieving the best possible result regardless of the language used. At Microsoft, we leverage multiple programming languages including C#, Go, Java, Rust, C++, TypeScript, and others, each chosen carefully based on technical suitability and team productivity. In fact, C# still happens to be the most popular language internally, by far.
> 
> The TypeScript compiler's move to Go was influenced by specific technical requirements, such as the need for structural compatibility with the existing JavaScript-based codebase, ease of memory management, and the ability to handle complex graph processing efficiently. After evaluating numerous languages and making multiple prototypes - including in C# - Go emerged as the optimal choice, providing excellent ergonomics for tree traversal, ease of memory allocation, and a code structure that closely mirrors the existing compiler, enabling easier maintenance and compatibility.
> 
> In a green field, this would have been a totally different conversation. But this was not a green field - it's a port of an existing codebase with 100 man-years of investment. Yes, we could have redesigned the compiler in C# from scratch, and it would have worked. In fact, C#'s own compiler, Roslyn, is written in C# and bootstraps itself. But this wasn't a compiler redesign, and the TypeScript to Go move was far more automatable and more one-to-one in its mapping. Our existing codebase is all functions and data structures - no classes. Idiomatic Go looked just like our existing codebase so the port was greatly simplified.
> 
> While this decision was well-suited to TypeScript's specific situation, it does not diminish our deep and ongoing investment in C# and NET. A majority of Microsoft's services and products rely heavily on C# and NET due to their unmatched productivity, robust ecosystem, and strong scalability. C# excels in scenarios demanding rapid, maintainable, and scalable development, powering critical systems and numerous internal and external Microsoft solutions. Modern, cross-platform .NET also offers outstanding performance, making it ideal for building cloud services that run seamlessly on any operating system and across multiple cloud providers. Recent performance improvements in NET 9 further demonstrate our ongoing investment in this powerful ecosystem (https://devblogs.microsoft.com/dotnet/performance-improvements-in-net-9/).
> 
> Let's be real. Microsoft using Go to write a compiler for TypeScript wouldn't have been possible or conceivable in years past.
> 
> However, over the last few decades, we've seen Microsoft's strong and ongoing commitment to open-source software, prioritizing developer productivity and community collaboration above all. Our goal is to empower developers with the best tools available, unencumbered by internal politics or narrow constraints. This freedom to choose the right tool for each specific job ultimately benefits the entire developer community, driving innovation, efficiency, and improved outcomes. And you can't argue with a 10x outcome!
> 
> No single language is perfect for every task, and at Microsoft, we celebrate the strength that comes from diversity in programming languages. Our commitment to C# and NET remains stronger than ever, continually enhancing these technologies to provide developers with the tools they need to succeed now and into the future.