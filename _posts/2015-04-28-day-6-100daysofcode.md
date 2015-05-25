---
title: '<span data-rel="title">Day 6: #100daysofcode</span>'
author: LP
layout: post
permalink: /day-6-100daysofcode/
wiziapp_processed:
  - 1
---

<ul>
  <li>
    It's common to use adjectives as the names for decorator functions.
  </li>
</ul>

<p>
  Decorator functions can pass in more than just simple value properties. They can also pass in functions.
</p>

<ul>
  <li>
    "Functions in Python cannot be anonymous, and function declarations are not expressions, so they cannot be defined and used on the same line." (<a href="https://blog.glyphobet.net/essay/2557">Helpful article: difference between javascript and python</a>)
  </li>
  <li>
    Tip: move functions outside of constructor function so that the function is not invoked every time an object is instantiated. For example:
  </li>
</ul>

<pre><code>var Car = function(obj, loc) { 
var obj = {loc: loc };
obj.move = move;
return obj;
}

var move = function() { 
    obj.loc++;
}
</code></pre>

<ul>
  <li>
    Decorators take in another function or a class as an argument and return a modified function or class.
  </li>
  <li>
    The reason why most JS libraries are wrapped in an anonymous function: it protects the contents of the library from interference by other .js files.
  </li>
  <li>
    In javascript, variable hoisting happens. That is, a variable is defined ("hoisted") to the top of its scope (e.g. if <code>var a = 5</code> on line 5 inside a function, it would be as if <code>var a;</code> on line 2).
  </li>
</ul>

<p>
  In python, there is no variable hosting, so an identifier would not exist until the interpreter reached the line of code where it was defined. (<a href="https://blog.glyphobet.net/essay/2557">Source</a>)
</p>

<p>
  &#8211;<br /> Q: How do I simply the following?
</p>

<pre><code>var amy = {loc: 1}
amy.loc++;
var ben = {loc: 1}
ben.loc++;
</code></pre>

<p>
  A:
</p>

<pre><code>var move = function(car) { 
   person.loc++;
}

var carlike = function(obj, loc) {
   obj.loc = loc;
   return obj;
}

var amy = carlike({}, 1);
var ben = carlike({}, 2);
move(amy);
move(ben);
</code></pre>

<p>
  ==============
</p>

<p>
  This post is a part of the <a href="http://www.thecodingdiaries.com/the-100daysofcode-challenge/#sthash.eAFLTbDO.dpbs">#100daysofcode</a> challenge.
</p>