---
layout: post
date: 2025-03-22 04:12 +0800
title: contenteditable HTML attribute
linkblog: true
tags: []
---
While reading the Hacker News post: [Show HN: Nash, I made a standalone note with single HTML file](https://keepworking.github.io/nash/), one of the discussions centered around how the linked site used 
```
   <div id="editor" contenteditable="true">
```
to do most of the heavy lifting. 

To which Steve Newman, one of the cofounders of what became Google Docs replied with:

> This one line was like 90% of the original implementation of Writely (the startup that became Google Docs; source: I was one of the founders).
> 
> The other 90% was all the backend code we had to write to properly synchronize edits across different browsers, each with their own bizarre suite of bugs in their contenteditable implementations :-)

Checking the [contenteditable documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contenteditable), it’s been available since 2008. 
I always assumed that Google Docs were using JavaScript to dynamically render a textarea when the user focused on an element, then render that into HTML elements when the element lost focus. Like we used to do with WYSIWYG editors around that time. But the fact that it was “simpler” than that and that attribute launched a multimillion dollar product (and I’m going to assume Microsoft Office, Notion, etc are built similarly?), makes it more beautiful. 