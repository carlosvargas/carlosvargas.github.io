---
date: 2025-02-05 21:40 +0800
title: LLM writing documentation
linkblog: true
tags: [llms]
---

Simon Willinson fed [his GitHub repo to o3-mini](https://simonwillison.net/2025/Feb/5/o3-mini-documentation/), and was able to get it to write detailed documentation on the code. 

> The prompt used 99,348 input tokens and produced 3,118 output tokens (320 of those were invisible reasoning tokens). That's [a cost](https://tools.simonwillison.net/llm-prices) of 12.3 cents.

He used his command line tool LLM, to send the whole repo to it. 

```shell
cd /tmp
git clone https://github.com/simonw/datasette
cd datasette
files-to-prompt datasette -e py -c | \
  llm -m o3-mini -s \
  'write extensive documentation for how the permissions system works, as markdown'
```

This type of use case might actually get me to try his tool - https://llm.datasette.io/en/stable/. Normally, my interactions via the browser or code editor are more than enough, but this is the first instance where CLI might make the best sense. 