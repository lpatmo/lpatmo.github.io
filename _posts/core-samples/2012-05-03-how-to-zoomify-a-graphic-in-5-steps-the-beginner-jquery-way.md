---
title: '<span data-rel="title">How To Magnify A Graphic In 5 Steps (The Beginner jQuery Way)</span>'
author: LP
layout: post
permalink: /how-to-zoomify-a-graphic-in-5-steps-the-beginner-jquery-way/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 692826187
---
<span data-rel="content">

<p>
  A few weeks ago I tinkered around with &#8220;zoomifying&#8221; a graphic upon mouseover. I quickly discovered that I needed to add a &#8220;mouseout&#8221; event, so with some more hobbling around I was able to write up something that works. I have the feeling that experts would have written it more simply &#8212; but hey, it works!
</p>

<p>
  For this tutorial we&#8217;re going to assume that the natural width of the image is 300, and the magnified width of the image is 800px. Note that the jQuery library must be called before any of the jQuery can work.
</p>

<p>
  <strong>Mouseover the image to see example: </strong><br />
</p>

<p>
  <img src="http://www.thecodingdiaries.com/wp-content/uploads/2012/05/metacodingdiaries-300x164.jpg" alt="image" title="Hey, it's blurrier but larger!" width="300" height="164" class="infographic" />
</p>

<div class="steps">
  <strong>Step 1:</strong><br /> Save the image in its original, high-quality size.<br /> <strong>Step 2:</strong><br /> Upload the high-quality image into PicMonkey (or another photo editor) and find the heights for when the image is resized to width=300 and for when the image is resized to width=800</p> 
  
  <p>
    Copy and paste the following script to the top of the WordPress post. Switch out the heights that you found from picmonkey.
  </p>
  
  <pre class="syntax {css}">
</pre>
  
  <p>
    <strong>Step 3:</strong><br /> Get rid of the tags in the image on the post. So
  </p><pre class="syntax {CSS}>
  
  <a href="IMAGE URL"><img class="wp-image" title="P1" src="IMAGE SOURCE" alt="" width="300" height="648" /></a></pre> 
  
  <p>
    becomes
  </p><pre class="syntax {css}>
  
  <img class="wp-image" title="P1" src="IMAGE URL" alt="" width="300" height="648" /></pre> 
  
  <p>
    <strong>Step 4: </strong><br /> Change the class to be equal to &#8220;infographic1&#8243;, and edit out the title to whatever you desire.
  </p><pre class="syntax {css}>>
  
  <img class="wp-image" title="P1" src="IMAGE URL" alt="" width="300" height="648" /></pre> 
  
  <p>
    becomes
  </p><pre class="syntax {css}>
  
  <img class="infographic1" title="IMAGE TITLE" src="IMAGE URL" alt="" width="300" height="648" /></pre> 
  
  <p>
    <strong>Step 5:</strong><br /> Click &#8220;preview&#8221; to check that the zoomification effect is working. Double check the other steps if it&#8217;s not.
  </p>
</div></span>