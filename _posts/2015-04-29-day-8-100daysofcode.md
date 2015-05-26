---
title: '<span data-rel="title">Day 8: #100daysofcode</span>'
author: LP
layout: post
permalink: /day-8-100daysofcode/
wiziapp_processed:
  - 1
---


I did not know rewriting <code>{{form.as_p}} </code> so that I could have more control over each of the form elements was as easy as transforming it into:


<code>
{% for field in form %}
	...
 {%endfor%}
</code>

  with <code>{{ field }}</code> and <code>{{ field.help_text }}</code> and code>{{ field.label }}</code> as variables.
  :D

This post is a part of the <a href="/the-100daysofcode-challenge/#sthash.eAFLTbDO.dpbs">#100daysofcode</a> challenge.
