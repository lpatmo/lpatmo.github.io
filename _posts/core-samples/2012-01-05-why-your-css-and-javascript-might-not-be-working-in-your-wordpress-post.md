---
title: '<span data-rel="title">Why Your CSS and Javascript Might Not Be Working In Your WordPress Post</span>'
author: LP
layout: post
permalink: /why-your-css-and-javascript-might-not-be-working-in-your-wordpress-post/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 530895843
---
<span data-rel="content">

<p>
  I was working on a CSS/Javascript design that involved a couple of thumbnails the other day. Clicking on each thumbnail would generate the corresponding video or graphic, and hide all the other pieces of content. I coded the design in notepad++, tested it in a couple of browsers, and made sure it worked. Then I pasted the code into the HTML editor of a WordPress post, hit &#8220;preview,&#8221; and encountered a mess.
</p>

<p>
  Thanks goodness for co-workers who code. Since I couldn&#8217;t figure out why my code was working in my text editor but not in WordPress, S. looked it over for me and figured out that WordPress was adding paragraph tags to all the blank lines in my script. Some of these tags ended up in the middle of the CSS and Javascript!
</p>

<p>
  Needless to say, we deleted all the blank lines. S. also ended up simplifying my javascript. As for me, I&#8217;m back hitting the books.
</p></span>