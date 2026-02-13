---
layout: post
date: 2026-02-13 07:50 +0800
title: All you really need is PostgreSQL
linkblog: true
tags: [db]
---

A few days ago, OpenAI published[ how they scaled using Postgres and Azure](https://openai.com/index/scaling-postgresql/). 

Now [Azure goes into a lot of details](https://techcommunity.microsoft.com/blog/adforpostgresql/supporting-chatgpt-on-postgresql-in-azure/4490247) into how they improved their infrastructure to support this: TCP congestion control algorithms and a DB re-architecture.

> To understand how Azure HorizonDB delivers these capabilities, let's look at its high‑level architecture as shown in Figure 1. It follows a log-centric storage model, where the PostgreSQL writeahead log (WAL) is the sole mechanism used to durably persist changes to storage. PostgreSQL compute nodes never write data pages to storage directly in Azure HorizonDB. Instead, pages and other on-disk structures are treated as derived state and are reconstructed and updated from WAL records by the data storage fleet.
> 
> Azure HorizonDB storage uses two separate storage services for WAL and data pages. This separation allows each to be designed and optimized for the very different patterns of reads and writes PostgreSQL does against WAL files in contrast to data pages. The WAL server is optimized for very low latency writes to the tail of a sequential WAL stream and the Page server is designed for random reads and writes across potentially many terabytes of pages. 

But the biggest takeaway is that all you really need is Postgres, after all.