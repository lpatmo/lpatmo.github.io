---
title: '<span data-rel="title">RESOURCE: Querying your Django Web App Without Using SQL</span>'
author: LP
layout: post
permalink: /resource-orm-query-api-from-the-full-web-framework-python-django-tutorial/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2693724373
---
<span data-rel="content">

<p>
  In case you need to query your Django API but don&#8217;t want to write SQL, here&#8217;s a useful video showing a summary of all the commands you can use:<br />
</p>

<p>
  Also: Ahh! Why is it that I often find screencasts to have much clearer explanations than written tutorials? In retrospect, it makes a lot of sense; the *ideal* tutorial would probably be a series of animated GIFs showing steps and the results of those actions, but nobody has time to compile a bunch of GIFs and then write out explanation texts when it&#8217;s possible to hit two birds with one stone using a screencast.
</p>

<p>
  The reason I&#8217;m happy with this tutorial is because 1/3 of the way through the video, it reminded me that I could use .value(&#8216;COLUMNA&#8217;, &#8216;COLUMNB&#8217;) to grab the contents of the columns I needed. And I&#8217;d failed to notice how to do it when I was skimming through the <a href="https://docs.djangoproject.com/en/1.2/topics/db/queries/" target="_blank">official documentation on Django querysets</a> earlier, mostly because &#8212; well,
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-17-at-11.42.55-PM.png"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-17-at-11.42.55-PM.png" alt="django documentation screenshot" width="921" height="545" class="alignnone size-full wp-image-759" /></a>
</p>

<p>
  &#8230; look a lot different than:
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-17-at-11.30.39-PM.png"><img class="alignnone size-full wp-image-758" alt="screenshot django query" src="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-17-at-11.30.39-PM.png" width="800" height="613" /></a>
</p>

<p>
  Yes, I know this means I could try to read better, too. Just wanted to point out the usefulness of screencasts as a teaching method, I suppose &#8212; especially for computer-based learning.
</p></span>