---
title: '<span data-rel="title">Deploying to Heroku</span>'
author: LP
layout: post
permalink: /deploying-to-heroku/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 1238450644
---
<span data-rel="content">

<p>
  Chapter 1.4  of <a href="http://ruby.railstutorial.org/" target="_blank">railstutorial.org</a> taught me how to deploy a Rails app onto Heroku.
</p>

<p>
  But how does one deploy a static app?
</p>

<p>
  After some googling, I found <a href="http://www.lemiffe.com/how-to-deploy-a-static-page-to-heroku-the-easy-way/" target="_blank">this</a> from lemiffe.com.
</p>

<p>
  The standard index.html file would need to be renamed into something like home.html, and the index.php file would have to include<br /> <code>&lt; ? php include_once("home.html"); ? >.</code>
</p>

<p>
  And then &#8212; voila!
</p>

<p>
  1. <code>cd</code> into the directory<br /> 2. Make sure you <code>commit</code> your files.<br /> 3. <code>heroku create</code><br /> 4. <code>git push heroku master</code>
</p>

<p>
  The terminal will spit back to you a URL on herokuapps.com. Finally, if you want to rename it, just use the following command:
</p>

<p>
  <code>heroku rename newname</code>
</p></span>