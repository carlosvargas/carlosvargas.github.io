---
date: 2025-02-15 09:12 +0800
title: Quoting Peter Eisentraut
linkblog: true
tags: [sql]
---

[Quoting Peter Eisentraut](http://peter.eisentraut.org/blog/2025/02/11/how-about-trailing-commas-in-sql), on the challenges of adding trailing commas do SQL. 


> can see a few possible approaches:
> 1. We just support a few of the most requested cases. Over time, we can add a few more if people request it.
> 2. We support most cases, except the ones that are too complicated to implement or cause grammar conflicts.
> 3. We rigorously support trailing commas everywhere commas are used and maintain this for future additions.
> These are all problematic, in my opinion. If we do option 1, then how do we determine what is popular? And if we change it over time, then there will be a mix of versions that support different things, and it will be very confusing. Option 2 is weird, how do you determine the cutoff? Option 3 would do the job, but it would obviously be a lot of work. And there might be some cases where it’s impossible, and it would have to degrade into option 2.

He continues to say, that even other popular programming languages support this feature, they have fewer syntactic constructs than SQL. Making it easier to support this on those languages. 