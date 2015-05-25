---
title: '<span data-rel="title">Day 1: Getting Started With HTML</span>'
author: LP
layout: post
permalink: /why-am-i-learning-html-and-css/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 522654046
---
<span data-rel="content">

<div class="resources">
  <strong>Resources:</strong></p> 
  
  <ol>
    <li>
      Download <strong><a href="http://www.barebones.com/products/textwrangler/">Text Wrangler</a></strong> if you&#8217;re on the mac or <strong><a href="http://notepad-plus-plus.org/">Notepad++</a></strong> if you&#8217;re on the PC. Or find a similar editor.<br /> &#8212; Seriously, please do it. I didn&#8217;t even know what I was missing out on until I tried out Notepad++ and found that I could use it to preview my elementary code in Chrome, Safari, IE, and Firefox. Just be sure to save your file in an appropriate file &#8212; .html
    </li>
    <li>
      <strong><a href="http://www.html.net/tutorials/html/">HTML.net</a></strong><br /> &#8212; Gives a pretty good overview of what you should know about HTML. Comes with examples.
    </li>
    <li>
      <strong><a href="http://w3schools.com/html/html_doctype.asp">W3Schools</a></strong>
    </li>
    <p>
      &#8212; W3Schools has been criticized for being a go-to resource (see <a href="http://w3fools.com/">W3Fools.com</a>), but it&#8217;s not a bad tutorial to start with if you want a quick way to scratch the surface of what HTML is about. </ol> </div> 
      
      <p>
        My advice for you &#8212; as you scan through the recommended tutorials &#8212; is to type out the HTML you learn in Notepad++ or Text Wrangler. Learning by <em>doing</em> is the fastest route, and you&#8217;ll also familiarize yourself with typing out tags such as &#8220;<" or ">&#8220;.
      </p>
      
      <p>
        The first time I encountered HTML was probably in 2003, when I was playing around with Microsoft Frontpage, and noticing the funny code that popped up in &#8220;source view&#8221; whenever I did something in the visual editor. HTML is pretty easy to pick up, although the thing to learn if you <em>really</em> want to have some power over your site&#8217;s design is CSS.
      </p>
      
      <p>
        But to start, here&#8217;re some of the HTML basics you should probably know off the top of your head:
      </p>
      
      <div class="steps">
        <h3>
          1. The Hyperlink
        </h3>
        
        <pre class="syntax {css}"><a href="http://www.google.com">Link to google</a>
<strong>Demo:</strong>
<a href="http://www.google.com">Link to google</a>


<h3>
  2. The list
</h3>


<ul>
  <li>
    List Item 1
  </li>
  	
  
  <li>
    List Item 2
  </li>
  	
  
  <li>
    List Item 3
  </li>
  	</pre>
  
  
  <p>
    <strong>Demo:</strong>
  </p>
  
  
  <ul>
    <li>
      List Item 1
    </li>
    
    
    <li>
      List Item 2
    </li>
    
    
    <li>
      List Item 3
    </li>
    
  </ul>
  
  
  <p>
    Just change &#8220;ul&#8221; to &#8220;ol&#8221; and &#8220;/ul&#8221; to &#8220;/ol&#8221; if you want the list to have numbered points instead of bullet points. 
  </p>
  
  
  <h3>
    2. The bolded, italicized, underlined, and strikethrough fonts
  </h3>
  
  
  <pre class="syntax {css}"><strong>Bolded text</strong>
<span style="text-decoration: underline;">Underlined text</span>
<em>Italicized text</em>
&lt;s>Strikethrough text&lt;/s></pre>
  
  
  <p>
    <strong>Demo:</strong><br />
    <strong>Bolded text</strong><br />
    <span style="text-decoration: underline;">Underlined text</span><br />
    <em>Italicized text</em>
  </p>
  
  
  <h3>
    3. The centered image with width and height defined
  </h3>
  
  
  <pre class="syntax {html}">


<center>
  <img src="http://upload.wikimedia.org/wikipedia/commons/2/2a/Brown_bear_(Ursus_arctos_arctos)_running.jpg" alt="Random Image I Found On Wikipedia" width="200px" height="80px" />
</center>

<strong>Demo:</strong>
</pre>
  
  
  <p>
    <center>
      <img src="http://upload.wikimedia.org/wikipedia/commons/2/2a/Brown_bear_(Ursus_arctos_arctos)_running.jpg" alt="Random Image I Found On Wikipedia" width="200px" />
    </center>
  </p>
  
  
  <h3>
    4. The anchor link
  </h3>
  
  
  <pre class="syntax {css}"><a name="up"></a>Up
<a href="#down">Click here to go right below the "down" anchor tag</a>
Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text
<a name="down"></a>Down
<a href="#up">Click here to go right below the "up" anchor tag</a></pre>
  
  
  <p>
    <strong>Demo:</strong><br />
    <a name="up"></a>Up<br />
    <a href="#down">Click here to go right below the &#8220;down&#8221; anchor tag</a><br />
    Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text Paragraph Text<br />
    <a name="down"></a>Down<br />
    <a href="#up">Click here to go right below the &#8220;up&#8221; anchor tag</a>
  </p>
  
  
  <h3>
    5. Creating a horizontal divisor line
  </h3>
  
  
  <pre class="syntax {html}">


<hr />
</pre>
  
  
  <p>
    <strong>Demo:</strong>
  </p>
  
  
  <hr />
  
  <p>
    ^See the horizontal line?
    
  </p></div>
  
  
  <p>
    Of course, you probably want to do a lot more styling with your content, like change the colors of of your links, fine-tune the layout of your site, make your images move in a content slider, or even change the appearance of the horizontal line when you type in <hr />. That&#8217;s where CSS and Javascript come into play. But for now, browsing through the two resources above will help you understand HTML, which is the precursor to learning CSS and Javascript.
  </p>
  
  
  <p>
    When I started taking an interest in web design I knew no CSS at all, so the next post will be dedicated to a few of the resources I found helpful.
  </p>
  
  
  <p>
    &nbsp;</li>
    </ul>
    </span>