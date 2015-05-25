---
title: '<span data-rel="title">Installing Django With Virtualenv</span>'
author: LP
layout: post
permalink: /installing-django-with-virtualenv/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2693068727
---

<p>
  I&#8217;ve been looking at a couple of other Django tutorials lately, and recently &#8212; thanks to David, another Django learner I talked to at a Python meetup &#8212; I started making do with two great resources:
</p>

<p>
  <strong>A) Youtube Series with Mike Hibbert:</strong>
</p>

<p>
</p>

<p>
  <strong>B) <a href="http://www.tangowithdjango.com/book/index.html" target="_blank">Tango with Django</a> by Leif Azzopardi and David Maxwell.</strong>
</p>

<p>
  The Tango with Django book initially looked great, but I was disappointed to find that it doesn&#8217;t start off showing users how to run develop their app using virtualenv. (Some brief notes about using virtualenv doesn&#8217;t come until <a href="http://www.tangowithdjango.com/book/chapters/deploy.html#creating-a-virtual-environment" target="_blank">later in the book</a>.) Mike Hibbert&#8217;s video series, on the other hand, *starts off* walking the user through installation and virtualenv.
</p>

<p>
  For the sake of my own memory and to save myself some time from having to go play/pause through all 17 minutes of the installation video again, I decided to jot down the steps to creating a new Django application using virtualenv:
</p>

<p>
  <strong>1) Create a virtualenv:<br /> </strong>
</p>

<pre class="prettyprint">$ virtualenv --no-site-packages NAME-OF-VIRTUALENV</pre>

<p>
  Replace all capital letters with a name of your choosing.
</p>

<p>
  <strong>2) Activate your virtualenv:</strong>
</p>

<pre class="prettyprint">$ source NAME-OF-VIRTUALENV&#47;bin&#47;activate</pre>

<p>
  This gets you into the virtual environment. You&#8217;ll notice that your command line now has this prefix:
</p>

<pre class="prettyprint">(NAME-OF-VIRTUALENV)Your-MacBook-Air:$</pre>

<p>
  <strong>3) Change directory into your project folder and install Django:</strong>
</p>

<pre class="prettyprint">$ cd NAME-OF-VIRTUALENV
$ easy_install django</pre>

<p>
  You can also run <code> pip install -U django==1.5.4</code> instead of <code> easy_install django</code> if you want to install a specific version of Django instead of the latest version.
</p>

<p>
  <strong>4) Start a new project:</strong>
</p>

<pre class="prettyprint">$ django-admin.py startproject YOURPROJECTNAME</pre>

<p>
  You&#8217;re creating a new project.
</p>

<p>
  <strong>5) Preview your project in the browser:</strong>
</p>

<pre class="prettyprint">$ cd YOURPROJECTNAME
$ python manage.py runserver</pre>

<p>
  After you type the second command, you&#8217;ll be able to preview your app in your local browser.
</p>

<p>
  <span style="color: #000000;"><b>6) Create a new application within your Django project (think of an application as an ice crem tub inside your Django freezer &#8212; thanks for the metaphor, <a href="http://pydanny.com/announcing-two-scoops-of-django-1.6.html" target="_blank">Two Scoops of Django</a>!):</b></span>
</p>

<pre class="prettyprint">$ python manage.py startapp APPNAME</pre>

<hr />

<strong>Update:</strong> I found another good tutorial! The founder behind Coding for Entrepreneurs Youtube series demonstrates the creation of a Django project in virtualenv on his mac:</p> 

<p>
</p>