---
title: '<span data-rel="title">OMG, I got a two-gold-star-difficulty question on Udacity right!</span>'
author: LP
layout: post
permalink: /yay-i-got-this-two-gold-star-difficulty-question-on-udacity-right/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2656578533
---
<span data-rel="content">

<p>
  <strong>The question:</strong>
</p>

<blockquote>
  <p>
    # Given a variable, x, that stores the<br /> # value of any decimal number, write Python<br /> # code that prints out the nearest whole<br /> # number to x.<br /> # If x is exactly half way between two<br /> # whole numbers, round up, so<br /> # 3.5 rounds to 4 and 2.5 rounds to 3.<br /> # You may assume x is not negative.
  </p>
  
  <p>
    # Hint: The str function can convert any number into a string.<br /> # eg str(89) converts the number 89 to the string &#8217;89&#8217;
  </p>
  
  <p>
    # Along with the str function, this problem can be solved<br /> # using just the information introduced in unit 1.
  </p>
  
  <p>
    # x = 3.14159<br /> # >>> 3 (not 3.0)<br /> # x = 27.63<br /> # >>> 28 (not 28.0)<br /> # x = 3.5<br /> # >>> 4 (not 4.0)
  </p>
  
  <p>
    <strong>My answer:</strong><br /> x = 27.83<br /> rounded = round(x)<br /> convert_to_string = str(rounded)<br /> before_decimal = convert_to_string.find(&#8216;.&#8217;)<br /> print convert_to_string[0:before_decimal]
  </p>
</blockquote>

<p>
  &#8230; Okay, okay, this probably isn&#8217;t <em>that</em> impressive, given that I&#8217;d already gone through most of Learn Python the Hard Way before I decided to revisit Udacity, and at this point I&#8217;m comfortable enough to google and understand Python documentation when I need to.
</p>

<p>
  However, I *do* remember struggling with this last year when I first went tried out Udacity. So &#8212; yay for being self-aware about how I&#8217;m improving, I guess!
</p>

<p>
  One very simple python function I used that the official Udacity answer didn&#8217;t use (they just manually added 0.5 to x): <a href="https://docs.python.org/2/library/functions.html#round" target="_blank">https://docs.python.org/2/library/functions.html#round</a>
</p>

<p>
  &nbsp;
</p></span>