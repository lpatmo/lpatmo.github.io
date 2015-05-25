---
title: '<span data-rel="title">On the road to competency &#8211; two tips</span>'
author: LP
layout: post
permalink: /on-the-road-to-competency-two-helpful-searching-tips/
wiziapp_processed:
  - 1
---

<p>
  Last year, jumping from an HTML/CSS/JS mindset to working with full-stack apps was confusing. A single rendered page on a full-stack (e.g. Rails or Django or MeteorJS) app could be drawing in code from *multiple* files in different folders. I was often confused about where everything was located.
</p>

<p>
  Eventually, my co-worker Tim gave me two great tips, which made a *huge* difference in my ability to debug problems in more complicated apps.
</p>

<p>
  <strong>Tip #1: </strong>Install and use the silver searcher (<a href="https://github.com/ggreer/the_silver_searcher" target="_blank">https://github.com/ggreer/the_silver_searcher</a>). Once I started learning how to search for keywords by typing in &#8220;<strong>ag [keyword] -C5</strong>&#8221; or &#8220;<strong>ag [keyword] -l</strong>&#8221; in my terminal, I was able to figure out much more easily the files that certain bugs were located.
</p>

<p>
  The first example returns to you the file paths and line numbers where the keyword match (as well as 5 lines before and after the matching row for context).
</p>

<p>
  The second example returns the file paths and line numbers that match the keyword, but shows up as a list, and does not include any of the code or context. Using the &#8220;-l&#8221; search parameter is helpful if some of your search returns happen to be one long string.
</p>

<p>
  <strong>Tip #2: </strong>Use<strong> find . -name &#8220;keyword&#8221;</strong>
</p>

<p>
  This command searches for file <em>names</em> that match a specified keyword. Helpful if &#8212; for example, the word &#8220;apple&#8221; is the <em>name</em> of a file, but is never within the contents of any of my code.
</p>

<p>
  =====
</p>

<p>
  Interesting to reflect that in addition to being competent at &#8220;googling&#8221; for solutions on the internet, part of being a developer is becoming competent at searching for things in your own codebase.
</p>