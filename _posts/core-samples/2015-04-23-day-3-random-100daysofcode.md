---
title: '<span data-rel="title">Day 3: Random #100daysofcode</span>'
author: LP
layout: post
permalink: /day-3-random-100daysofcode/
wiziapp_processed:
  - 1
---
<span data-rel="content">

<ul>
  <li>
    <code>white-space: pre-wrap</code> preserves white spaces and breaks lines at newlines. (CSS)
  </li>
</ul>

<p>
  *You can index your models with <code>db_index=True</code> (<a href="https://docs.djangoproject.com/en/1.8/ref/models/fields/#db-index">reference</a>)
</p>

<ul>
  <li>
    You can give your model metadata by adding <code>class Meta</code>. Example from the official docs: <pre><code>from django.db import models
class Ox(models.Model):
  horn_length = models.IntegerField()

  class Meta:
      ordering = ["horn_length"]
      verbose_name_plural = "oxen"
</code></pre>
  </li>
</ul>

<p>
  Metadata options can include db_table, ordering, and verbose_name_plural. (<a href="https://docs.djangoproject.com/en/1.8/ref/models/options/#django.db.models.Options.db_table">reference</a>)
</p>

<ul>
  <li>
    <a href="http://stackoverflow.com/questions/5870537/whats-the-difference-between-django-onetoonefield-and-foreignkey">What is the difference between <code>OneToOneField</code> and <code>ForeignKey</code>?</a>
  </li>
</ul>

<p>
  This post is a part of the <a href="http://www.thecodingdiaries.com/the-100daysofcode-challenge/#sthash.eAFLTbDO.dpbs">#100daysofcode</a> challenge.
</p></span>