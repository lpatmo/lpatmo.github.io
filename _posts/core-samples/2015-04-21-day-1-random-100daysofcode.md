---
title: '<span data-rel="title">Day 1 Random: #100daysofcode</span>'
author: LP
layout: post
permalink: /day-1-random-100daysofcode/
wiziapp_processed:
  - 1
---
<span data-rel="content">

<ul>
  <li>
    Note to self: if a div inside a div isn't recognizing the parent div as a parent when it's set to <code>position: absolute</code>, it's because the closest parent needs to be set to <code>position: relative.</code> Otherwise, it'll default to <code>position: static</code>. (CSS)
  </li>
  <li>
    <code>Meteor.startup() { }</code> is sort of like <code>$(function() {});</code> except we use it with meteor. (MeteorJS)
  </li>
  <li>
    Adjust the height of a textarea with its content: <pre><code>$(&#39;textarea&#39;).css(&#39;height&#39;, &#39;auto&#39;); 
$(&#39;textarea&#39;).height(this.scrollHeight);
</code></pre>
  </li>
  
  <li>
    If you want the ability to write markdown inside your WordPress posts, see:<br /> <a href="http://www.elegantthemes.com/blog/tips-tricks/using-markdown-in-wordpress">http://www.elegantthemes.com/blog/tips-tricks/using-markdown-in-wordpress</a>. (I decided on using the PrettyPress Editor.)
  </li>
  <li>
    Note: to pull from a <em>branch</em> inside an upstream repo&#8230; <code>git fetch upstream branchname</code> and <code>git merge upstream branchname</code>
  </li>
  <li>
    If I notice that there are elements inside <code>view:source</code> but can't find it inside the browser <code>elements</code> tab, chances are it's because there was a <code>.remove()</code> put on the elements. (JS)
  </li>
  <li>
    <code>localStorage</code> is nice and lighter weight than cookies.
  </li>
  <li>
    <code>Intl.DateTimeFormat().resolvedOptions().timeZone ? Intl.DateTimeFormat().resolvedOptions().timeZone</code> returns the users's timezone! However, this is currently supported on only very limited modern browsers. (JS)
  </li>
</ul>

<p>
  This post is a part of the <a href="http://www.thecodingdiaries.com/the-100daysofcode-challenge/#sthash.eAFLTbDO.dpbs">#100daysofcode</a> challenge.
</p></span>