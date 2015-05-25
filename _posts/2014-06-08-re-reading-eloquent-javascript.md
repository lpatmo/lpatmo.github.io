---
title: '<span data-rel="title">Re-reading Eloquent Javascript</span>'
author: LP
layout: post
permalink: /re-reading-eloquent-javascript/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2748203639
---

<p>
  I am re-reading <a href="http://eloquentjavascript.net/" target="_blank">Eloquent Javascript</a> with Arthur at the moment, and realizing how much of a mistake I made reading it the first time around &#8212; that is, I read it by myself, barely typed out any of the exercises before looking at the solutions, and skimmed past sections when it got confusing.
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2014/06/ejs.png"><img class="alignnone size-full wp-image-866" alt="ejs" src="http://www.thecodingdiaries.com/wp-content/uploads/2014/06/ejs.png" width="250" height="330" /></a>
</p>

<p>
  (Although you can <a href="http://www.amazon.com/gp/product/1593272820?ie=UTF8&tag=marijhaver-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=1593272820" target="_blank">purchase this book</a> online, it&#8217;s free to read online.)
</p>

<p>
  Arthur isn&#8217;t a programmer in the career sense, but he double majored in math along with italian, and apparently having had practice solving mathematical problems helps a lot.
</p>

<p>
  Having a study partner also helps a lot. As we read, we&#8217;ll paraphrase the content out loud, quiz each other about what we just read, google an answer when the answer to a question isn&#8217;t immediately apparent, work on the exercises individually, share our respective solutions to the exercises using JSFiddle, and puzzle out root causes when something we coded renders something surprising.
</p>

<p>
  For example:
</p>

<blockquote>
  <p>
    split and join are not precisely each other&#8217;s inverse. string.split(x).join(x) always produces the original value, but array.join(x).split(x) does not. Can you give an example of an array where .join(&#8221; &#8220;).split(&#8221; &#8220;) produces a different value? &#8211; <strong>Exercise 4.3</strong>
  </p>
</blockquote>

<p>
  <strong>We each approached the solution differently:</strong>
</p>

<pre class="prettyprint">var testo = &#91;&#34;This is a&#34;, &#34;sentence Arthur wrote.&#34;&#93;;
console.log(testo.join(&#34; &#34;));
console.log(testo.join(&#34; &#34;).split(&#34; &#34;));</pre>

<pre class="prettyprint">array = &#91;&#34;this&#34;, &#34;is &#34;, &#34;a&#34;, &#34;sentence&#34;, &#34;Linda&#34;, &#34;wrote&#34;, &#34;with&#34;, &#34;an&#34;, &#34;extra&#34;, &#34;space&#34;, &#34;after&#34;, &#34;is&#34;&#93;;
console.log(array.join(&#34; &#34;));
console.log(array.join(&#34; &#34;).split(&#34; &#34;));</pre>

<p>
  To solve this, we had to truly understand what the .join() and .split() methods did in javascript.
</p>

<p>
  <strong>There&#8217;s good documentation on Mozilla:</strong><br /> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join" target="_blank">https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join<br /> </a>&#8220;The join() method joins all elements of an array into a string.&#8221;
</p>

<p>
  In other words, you start with an array, and you turn it into a string!
</p>

<p>
  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split" target="_blank">https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split<br /> </a>&#8220;The split() method splits a String object into an array of strings by separating the string into substrings.&#8221;
</p>

<p>
  In other words, you split a string up into an array!
</p>

<p>
  The two methods are not exact opposites of each other, though, as we just demonstrated via the book exercise.
</p>