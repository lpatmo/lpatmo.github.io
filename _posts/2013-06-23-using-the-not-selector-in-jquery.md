---
title: '<span data-rel="title">Using the &#8220;not&#8221; selector in jQuery</span>'
author: LP
layout: post
permalink: /using-the-not-selector-in-jquery/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 1450521041
---

<p>
  Was trying to figure out how to select every <li><span style="font-size: 16px;"> item in a row except the one with a class of &#8220;active.&#8221; As always, </span><a style="font-size: 16px;" href="http://stackoverflow.com/questions/520250/jquery-if-div-doesnt-have-class-x" target="_blank">Stackoverflow</a><span style="font-size: 16px;"> reminded me that jQuery came with &#8220;:not.&#8221;</span>
</p>

<p>
  <span style="font-size: 16px;">Example:</span>
</p>

<blockquote>
  <p>
    $(&#8220;li:not(.active)&#8221;).hover();
  </p>
</blockquote>