---
date: 2025-02-04 19:24 +0800
title: “Quoting Stephen”
linkblog: true
tags: [python]
---

> String interning (in CPython) happens for short strings that don’t have any special characters (anything that can’t be used as an identifier) 
- [Stephen Gruppetta](https://bsky.app/profile/stephengruppetta.com/post/3lhefod7x3c2c)

TIL **string interning** is a method of storing only one copy of each distinct String value, which must be immutable. Interning strings makes some string processing tasks more time-efficient or space-efficient at the cost of requiring more time when the string is created or interned. The distinct values are stored in a string intern pool. 