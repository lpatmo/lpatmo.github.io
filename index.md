---
layout: page
title: The Coding Diaries
tagline: Front-end dev with a non-traditional background (no CS degree). My hope is for this blog to be helpful for others starting out too.
---
{% include JB/setup %}
  <link href='http://fonts.googleapis.com/css?family=Unkempt' rel='stylesheet' type='text/css'>

<div class="container">
	<div class="row">
	 <div class="col-xs-8">
  {% for post in site.posts %}
 <h2> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
    	<p>
    		{{post.content}}

    	</p>

  {% endfor %}
  	</div>

    <div class="col-xs-4">
    	<ul class="notes">
			<li class="notes" style="padding: 1em; word-wrap: break-word; overflow: hidden;">Hi, I'm Linda! I enjoy going to tech meetups, learning web development, and blogging about the learning path. Follow me on twitter:<a href="http://bit.ly/1epoq9z" target="_blank">@LPnotes</a></li>
		</ul>


    <ul class="sidebar">
      {% for post in site.posts %}
        <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>


  </div>
</div>
</div>




