---
layout: post
date: 2025-05-01 19:00 +0800
title: Apple AppStore commission 
linkblog: true
tags: [blog]
image: https://upload.wikimedia.org/wikipedia/commons/archive/5/5d/20120930120055%21Available_on_the_App_Store_%28black%29.png
---

Today has been an eventful day for the Apple AppStore. [John Gruber](https://daringfireball.net/2025/04/gonzales_rogers_apple_app_store_ruling) has an excellent summary of it, but TLDR; Apple cannot charge a commission to developers, for telling users to purchase an in app purchase or subscription from outside the AppStore. 

At Scribd, I work on the team that’s responsible for all things subscriptions. Before that, I dabbled in AppStore payments for Bitwise. So I’ve spent countless hours trying to understand if it was possible for us to use our web payments processor, that we already integrate and support, for everything Apple or Google. And the answer was always no, until today (there was a ruling in 2021 that allowed developers to do this, but Apple’s restrictions effectively rendered it moot). 

From a user perspective, I like subscribing via the AppStore. It’s easy to keep track of my subscriptions, I trust my payment information is secure and I like Family Sharing. But as a developer, it’s such a pain sometimes. Documentation isn’t always the best (Google’s is a bit better), customer support is harder since we don’t have a lot of control, and it’s really easy to make a mess of your subscription groups. But the fact that we have to create a specific integration to each AppStore is expensive to do and maintain. It’s much easier for developers to handle subscriptions via the web (there’s plenty of paid or open source platforms that help you with this now, or if you’re adventurous to roll your own), and have all platforms subscribe via it. Then you just have to devote your resources to a single platform. 

Plus the [commission on every purchase](https://developer.apple.com/app-store/subscriptions/) is such a hard pill to swallow. I do think that they should take a cut, the AppStore does deserve it since they provide a platform for subscriptions, purchases and processing payments costs them money. But charging such a high fee (30% for the first year if your business makes more than $1MM) is expensive for a business, on top of the team needed to maintain it. 

Either way, I’m excited about this ruling. We as developers and consumers, want more options. We can continue to use AppStores (at a more reasonable fee) or use something else. 