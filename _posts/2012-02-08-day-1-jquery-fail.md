---
title: '<span data-rel="title">Lessons Learned From Beginner jQuery Fail</span>'
author: LP
layout: post
permalink: /day-1-jquery-fail/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 568435421
---
<span data-rel="content">

<p>
  Reading <a href="http://www.amazon.com/JavaScript-jQuery-David-Sawyer-McFarland/dp/1449399029/ref=sr_1_1?ie=UTF8&#038;qid=1328679663&#038;sr=8-1" target="_blank">Javascript & jQuery: The Missing Manuals</a> was influential in several ways:
</p>

<div class="steps">
  (1) The book got me through the basics of javascript and its tutorials quickly got me using jQuery to <em>do stuff</em>.
</div>

<div class="steps">
  (2) Suddenly I knew exactly how components on under websites slid from place to place, faded in and out, and did a lot of other neat tricks. I was startled by how simple jQuery was &#8212; I wasn&#8217;t really writing code; I was accessing a <em>javascript library</em> and creating standard structures to pull in the hard work that other authors had done.
</div>

<p>
  Then I attempted to do a simple .show() and .hide() (translation: hiding an element, then showing it upon a click) today with jQuery, and it didn&#8217;t work. Asked a co-worker who&#8217;s an experienced web developer, and he suggested I start using a debugger of some sort. He kindly linked me to <a href="http://code.google.com/chrome/extensions/tut_debugging.html" target="_blank">Chrome Developer Tools</a>, which showed me that there was a syntax error in the javascript.
</p>

<p>
  What, you might ask, is a syntax error?
</p>

<p>
  I did some googling, and some asking, and apparently the majority of syntax errors have to do with punctuation &#8212; such as forgetting to close a line with a semicolon, or forgetting parentheses.
</p>

<p>
  I stared at the code. Stared some more. Then I finally had the bright idea to compare my code with another example of jquery that was working (I used <a href="http://www.w3schools.com/jquery/tryit.asp?filename=tryjquery_hide" target="_blank">this</a>), and that was where I immediately saw that <em>I was missing an entire set of closing parentheses });</em>.
</p>

<p>
  Whoops! Guess that I means I need to reread my book. Or just start practicing with some more examples.
</p>

<p>
  My co-worker also pointed out the <em>console.log(&#8220;comment about what your javascript is supposed to be doing here&#8221;)</em> trick, which is achieved by putting that line above every piece of javascript you want to test, opening up browser tools, and then seeing if the line you typed runs in the browser console. He told me that it&#8217;s a good idea to get rid of these lines when the code goes live, though, because of compatibility issues with IE9.
</p>

<p>
  Hurrah for super-helpful co-workers! Sometimes it&#8217;s good to have mentors who know their stuff. And to cross-check code with a working example rather than staring at it blindly, of course.
</p></span>