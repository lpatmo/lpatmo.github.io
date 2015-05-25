---
title: '<span data-rel="title">Day 7: #100daysofcode</span>'
author: LP
layout: post
permalink: /day-7-100daysofcode/
wiziapp_processed:
  - 1
---

<ul>
  <li>
    Python uses "classical inheritance. JS uses "prototypal" inheritance.
  </li>
  <li>
    In python, you have an <strong>init</strong> constructor which generally contains some methods. In javascript, any function can be constructor by putting <code>new</code> in front of the function call. Make a method available to every instance of this javascript constructor by adding it to the <code>prototype</code> property of the constructor.
  </li>
</ul>

<pre><code>class Example(object):
    def __init__(self, args):
         self.args = args

     def example_function(self):
         #something to self.args

f = Example(data)
f.example_function()
</code></pre>

<p>
  //python
</p>

<pre><code>function Example(args){
this.args = args;
}

Example.prototype.example_function = function() {
 //do something to this.args
}

f = new Example();
f.example_function();
</code></pre>

<p>
  //javascript
</p>

<ul>
  <li>
    In python, functions and methods are different <em>types</em>.
  </li>
  <li>
    How to make an object inherit from another in javascript:
  </li>
</ul>

<pre><code>function Base() {
   console.log(&#39;something&#39;);
}

function Derived() {
   console.log(&#39;something2&#39;);
}

Derived.prototype = new Base();
</code></pre>

<ul>
  <li>
    How to make a class inherit from another in python:
  </li>
</ul>

<pre><code>class Base(object):
   pass

class Derived(Base):
pass
</code></pre>

<p>
  Source: Matt Chisholm (<a href="https://blog.glyphobet.net/essay/2557">https://blog.glyphobet.net/essay/2557</a>)
</p>

<p>
  This post is a part of the <a href="http://www.thecodingdiaries.com/the-100daysofcode-challenge/#sthash.eAFLTbDO.dpbs">#100daysofcode</a> challenge.
</p>