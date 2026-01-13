---
layout: post
date: 2026-01-13 07:19 +0800
title: Pi - multi LLM CLI coding agent
linkblog: true
tags: [llms]
---

Mario Zechner has [launched pi, a multi LLM provider CLI coding agent](https://shittycodingagent.ai/). 

Here's [a post about how they built it](https://mariozechner.at/posts/2025-11-30-pi-coding-agent/) and some of the design decisions behind it. 

The most interesting is how the tool doesn't include a lot of the complex features that are common on these tools now:

> pi is opinionated about what it won't do. These are intentional design decisions to minimize context bloat and avoid anti-patterns.
> 
> [No MCP.](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#no-mcp) Build CLI tools with READMEs (see [Skills](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#skills)). The agent reads them on demand. [Would you like to know more?](https://mariozechner.at/posts/2025-11-02-what-if-you-dont-need-mcp/) If you must, use [mcporter](https://github.com/steipete/mcporter).
> 
> [No sub-agents.](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#no-sub-agents) Spawn pi instances via tmux, or [build your own sub-agent extension](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent/examples/extensions/subagent/). Observability and steerability for you and the agent.
> 
> [No permission popups.](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#no-permission-system-yolo-mode) Security theater. Run in a container or build your own with [Extensions](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#extensions).
> 
> [No plan mode.](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#no-planning-mode) Gather context in one session, write plans to file, start fresh for implementation.
> 
> [No built-in to-dos.](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#no-built-in-to-dos) They confuse models. Use a TODO.md file, or [build your own](https://github.com/badlogic/pi-mono/blob/main/packages/coding-agent/examples/extensions/todo.ts)with [extensions](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#extensions).
> 
> [No background bash.](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent#no-background-bash) Use tmux. Full observability, direct interaction.