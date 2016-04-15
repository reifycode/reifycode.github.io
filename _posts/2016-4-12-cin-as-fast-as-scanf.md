---
layout: post
published: true
exacttime: "20:31:00"
title: "Making cin as fast as scanf"
category: 
- "C++"
- "Competitive Coding"
author: thepulkitagarwal
---

There are a lot of reasons why you may want to make `cin` as fast as `scanf`. In my case, it was because of a [question on codechef](https://www.codechef.com/problems/DISHOWN).

Here is the single line of code that made the status of the answer go from "TLE" to "AC":

`ios::sync_with_stdio(false);`

[Note: This has to be there in `main()`, preferably before any `cin` or `scanf` operation]

What this statement does is disable the synchronization between the C++ and the C standard streams. By default, this is enabled. This synchronization allows us to use iostream operations, i.e. `cin`, with stdio operations, i.e. `scanf`, such that their output is predictable - the output follows the same order as used in the program. If the synchronization is disabled, which is what we're doing, it becomes unpredictable, but as fast as scanf.

In my case, this reduced the time taken on codechef from >0.50s to 0.45s.

If you are planning to use this method, know that there are a lot of negative consequences on doing this. (Read this [SO answer](http://stackoverflow.com/a/31165481) for more). And if you really need the speed of `scanf` and none of these negative consequences, just use `scanf` instead.