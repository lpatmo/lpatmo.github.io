---
title: '<span data-rel="title">How To Get Started With CSS</span>'
author: LP
layout: post
permalink: /day-2-getting-started-with-css/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 529988899
---
<span data-rel="content">

<div class="resources">
  <strong>Resources:</strong></p> 
  
  <ul>
    <li>
      W3Schools&#8217; Tutorial on CSS &#8211; <a href="http://www.w3schools.com/css/css_intro.asp">http://www.w3schools.com/css/css_intro.asp</a>
    </li>
    <li>
      <a href="http://www.amazon.com/CSS-Missing-David-Sawyer-McFarland/dp/0596802447">CSS: The Missing Manual</a> by David Sawyer McFarland (book) &#8212; The W3schools tutorial is good enough for a quick overview, but I recommend reading David McFarland&#8217;s book if you want to get a solid understanding of all that CSS has to offer. I read my copy on <a href="http://safaribooksonline.com/Corporate/Index/">Safari Books Online</a>, a subscription-based service that offers access to tons of programming books, but you can also purchase it directly.
    </li>
    <li>
      <a href="http://net.tutsplus.com">net.tutsplus.com</a> &#8212; I highly recommend this site as a go-to resource for finding tutorials of cool examples you can do with HTML and CSS. The tutorial below, in fact, is a simplification of some things I learned from <a href="http://net.tutsplus.com/tutorials/html-css-techniques/create-a-sticky-note-effect-in-5-easy-steps-with-css3-and-html5/">this post</a>.
    </li>
  </ul>
</div>

<p>
  Let&#8217;s try a simple example by learning how to recreate the block of text above. (Yes, <em>that</em> block of text hat vaguely looks like it rests on a yellow post-it-note.)
</p>

<p>
  But let&#8217;s not work with so much text. Ah, here&#8217;s our new HTML:
</p>

<pre class="syntax {css}">
This post-it note has been purposefully <em>simplified</em> to contain fewer words.
</pre>

<p>
  But we want to style it, right? So we&#8217;ll need to select it some way. Let&#8217;s do this by wrapping a div around it. Let&#8217;s name the div &#8220;postit.&#8221;
</p>

<p>
  But should we let &#8220;postit&#8221; be an ID or a class? You can <a href="http://css-tricks.com/the-difference-between-id-and-class/">read about the difference here</a>. For the purposes of this post, let&#8217;s make it a class so we can reuse the div.
</p>

<pre class="syntax {css}">


<div class="postit">
  This post-it note has been purposefully left <em>blank</em>.
</div>
</pre>

<p>
  Awesome! Now that the body of text we want to select has been selected, all that&#8217;s left to do is to write the CSS that styles the text. The most common method is to place the CSS in an <a href="http://www.w3schools.com/css/css_howto.asp" target="_blank">external style sheet</a>, but for the purposes of this post, let&#8217;s just write it above the HTML (otherwise known as an internal stylesheet). Makes it easy to see what happened at a glance.
</p>

<p>
  The first thing to remember, when writing CSS above the HTML, is to type these tags:
</p>

<pre class="syntax {css}">

</pre>

<p>
  See the space in the middle? That&#8217;s where we&#8217;re going to put the CSS. Since our div is a class, we type a period before the name of the div (&#8220;postit&#8221;). (Note: if it were an ID, we would have typed &#8220;#&#8221; in place of the period) Then we type in a set of brackets, inside of which will contain the styling.
</p>

<pre class="syntax {css}">

</pre>

<p>
  Now: what styles do we want? Say we want the font color inside the div to be a certain shade of blue, or the hex color code #369. This is what we&#8217;ll type inside:
</p>

<pre class="syntax {css}">

</pre>

<p>
  <strong>Note:</strong> Do NOT forget the semicolon after the statement!
</p>

<p>
  What else do we want to do with our block of text? Right underneath &#8220;color: #369&#8243;, type in:
</p>

<pre class="syntax {css}">
width: 30em; 
display: block;
</pre>

<p>
  This transforms the div into a block with a width of 30em, which is the same thing as 480 pixels. (Why type in &#8220;30em&#8221; instead of &#8220;480px&#8221;, which does the same thing? Stackoverflow members <a href="http://stackoverflow.com/questions/609517/why-em-instead-of-px" target="_blank">answer the question here</a>).
</p>

<p>
  Let&#8217;s also add in the following:
</p>

<pre class="syntax {css}">
background: #ffc;
</pre>

<p>
  This makes the background color a post-it color yellow.
</p>

<pre class="syntax {css}">
padding: 30px; 
</pre>

<p>
  This introduces some distance between the border of the div block and the text inside by a measure of 30 pixels all around.
</p>

<p>
  The final step? Adding some box shadow.
</p>

<pre class="syntax {css}">
-moz-box-shadow: 5x 5px 7x rgba(63,33,33,1);
-webkit-box-shadow: 5px 5px 7px rgba(63,33,33,.7);
box-shadow: 5px 5px 7px rgba(63,33,33,.7);
</pre>

<p>
  Here&#8217;s what your final product should look like:
</p>

<pre class="syntax {css}">




<div class="postit">
  This post-it note has been purposefully <em>simplified</em> to contain fewer words.
</div>
</pre>

<p>
  And you&#8217;re done! Make sure that your notepad++ file is saved as an appropriate .html or .php (which could also work), and preview it in your browser. Here&#8217;s what you should get:
</p>

<div class="postit">
  This post-it note has been purposefully <em>simplified</em> to contain fewer words.
</div></span>