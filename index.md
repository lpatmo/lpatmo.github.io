---
layout: page
title: The Coding Diaries
tagline: Supporting tagline
---
{% include JB/setup %}

<div class="posts">
  {% for post in site.posts %}
 <h2> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
    	<p>
    		{{post.content}}

    	</p>

  {% endfor %}
</div>

