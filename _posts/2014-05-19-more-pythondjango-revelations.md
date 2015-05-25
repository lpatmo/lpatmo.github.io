---
title: '<span data-rel="title">More Python/Django Revelations</span>'
author: LP
layout: post
permalink: /more-pythondjango-revelations/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2695931047
---

<p>
  Ok, I&#8217;m still due to write a proper full review of <a href="https://www.udacity.com/course/ud036" target="_blank">Udacity&#8217;s Intro to Object-Oriented Programming</a> course at some point (hopefully soon), but for now, I wanted to take a moment to say: I&#8217;m so glad I made myself go through all the videos there, because a lot of the confusing things from before, from when I was trying to familiarize myself with Django for the first time, aren&#8217;t so confusing anymore.
</p>

<p>
  For example, here in the <a href="https://docs.djangoproject.com/en/dev/topics/db/models/" target="_blank">Django docs about models</a>:
</p>

<pre class="prettyprint">from django.db import models

class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)</pre>

<p>
  Looking at this piece of code for the first time, I HAD NO IDEA THAT <code>models.Model</code> referred to the <code>models</code> module, whose documentation can be found at <a href="https://docs.djangoproject.com/en/dev/topics/db/models/" target="_blank">https://docs.djangoproject.com/en/dev/topics/db/models/</a>!
</p>

<p>
  <code>models.Model</code> simply calls the <code>Model</code> class from he module <code>models</code>. It&#8217;s a standard base class that helps us create representations of data in Django. In the example above, too, class <code>Person</code> inherits properties from class <code>Models.model</code>.
</p>

<p>
  Also, a key line from the docs:<br /> &#8220;Generally, each model maps to a single database table.&#8221;
</p>

<p>
  Makes a lot of sense now. We now have a database table named Person, with two columns for storing 30-character data: one to populate first_name, and another to populate last_name.
</p>

<p>
  By the way, for the record, I&#8217;m still finding <a href="https://www.youtube.com/watch?v=D5VlpgEVVg4&#038;list=TL04EOI77QDS76GOt2LAh57x8tD4JBu7kX" target="_blank">Mike Hibbert&#8217;s Python/Django tutorial on YouTube</a> really helpful. I&#8217;d written previously about his videos in the context of setting up a virtualenv with Django.
</p>

<p>
  If all goes well, perhaps I&#8217;ll stick with it and see how it goes. More soon.
</p>