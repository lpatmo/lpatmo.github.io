---
title: '<span data-rel="title">REVIEW: Getting Started with Django Video Series on Vimeo (Kickstarter-backed), Part I</span>'
author: LP
layout: post
permalink: /review-getting-started-with-django-video-series-on-vimeo-kickstarter-backed-part-i/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2722090931
---

<p>
  W00t, I just deployed my first Django app on Heroku! Only took about a day of debugging, but the tutorial is pretty great.
</p>

<p>
  <strong>Full URL of <em>Getting Started with Django</em>:</strong><br /> <a href="http://gettingstartedwithdjango.com/en/lessons/introduction-and-launch/">http://gettingstartedwithdjango.com/en/lessons/introduction-and-launch/</a>
</p>

<p>
</p>

<p>
  By the way, I&#8217;d recommend watching the video of the tutorial and using the text below it as review or as a summary of what you&#8217;re watching. The text is not fully comprehensive with all the commands, and if you only follow the text you&#8217;ll get confused.
</p>

<p>
  Created by Kenneth Love, this <a href="https://www.kickstarter.com/projects/657368266/getting-started-with-django" target="_blank">Kickstarter-backed</a> Django tutorial was uploaded around January 2013. The first part purports to teach you how to create a small blogging app, and later parts feature larger demonstration projects.
</p>

<p>
  Neither of the Django tutorials I&#8217;d visited so far &#8212; <a href="https://www.youtube.com/watch?v=3DccH9AMwFQ">Coding for Entrepeneurs</a> nor <a href="http://www.tangowithdjango.com/book/">Tango with Django</a> &#8212; had visited deployment (to Heroku, no less!) as part of the setup in the <em>beginning, </em>so it was a nice change. Also nice was that this tutorial:
</p>

<ul>
  <li>
    uses vagrant on top of Virtualbox and virtualenv, which is a best practice setup for running Django apps nowadays
  </li>
  <li>
    uses Postgres for the database instead of sqllite or MySQL (Tango with Django uses sqllite3, which this author recommended against in a production environment)
  </li>
</ul>

<p>
  Note that the first chapter of this tutorial doesn&#8217;t get into creating the full blown-out microblog app yet, but does cover a lot with installation and app file setup.
</p>

<p>
  <strong>The downsides?</strong> I ran into a couple of issues that took me a while to debug, and I&#8217;ll make note of them in more detail below. Also, at the time that this series was made, Django 1.4.3 was the most up-to-date version, so I made sure to install 1.4.3. and not 1.6 or 1.7 &#8212; the <em>most</em> up-to-date version as of May 2014.
</p>

<h2>
  <strong>Issues:</strong>
</h2>

<p>
  <strong>1) When I tried to create a new &#8220;vagrant&#8221; user in postgres, I got:</strong>
</p>

<p>
  ERROR: role &#8220;vagrant&#8221; already exists
</p>

<p>
  The solution was to run
</p>

<ol>
  <li>
    <code>sudo su postgres</code>
  </li>
  <li>
    <code>dropuser vagrant</code>
  </li>
</ol>

<p>
  But then I had to make sure to type <strong>exit</strong> to exit out of <strong>postgres@precise64:/vagrant/projects/microblog$</strong> and get back to <strong>(blog-venv)vagrant@precise64:/vagrant/projects/microblog$</strong>  to continue with the rest of the tutorial.
</p>

<p>
  <strong>2) When I ran &#8216;heroku run python manage.py syncdb&#8217;, I got:</strong>
</p>

<p>
  Error: could not connect to server: No such file or directory Is the server running locally and accepting connections on Unix domain socket &#8220;/var/run/postgresql/.s.PGSQL.5432&#8243;?
</p>

<p>
  Luckily,<a href="http://stackoverflow.com/questions/14574827/gswd-heroku-django-manage-py-issue"> someone on stackoverflow</a> had had the same problem; the solution was to make sure my settings/local.py file was in .gitignore; otherwise, Heroku would be confused by the presence of two DATABASES = { } dictionaries in both base.py and settings.py.
</p>

<p>
  <strong>3) Running multiple Django apps in my local environment created PORT conflicts</strong>
</p>

<p>
  Since I had been in the middle of working on another Django app from the Tango with Django book when I started following this tutorial, I got a conflict in Vagrant with the port numbers. I ended up having to go into <strong>Vagrantfile </strong>to change one of the ports from 8888 to 8889.
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-29-at-3.23.27-PM.png"><img class="alignnone size-full wp-image-814" alt="Screen Shot 2014-05-29 at 3.23.27 PM" src="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-29-at-3.23.27-PM.png" width="209" height="98" /></a><a href="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-29-at-3.23.52-PM.png"><img class="alignnone size-full wp-image-815" alt="Screen Shot 2014-05-29 at 3.23.52 PM" src="http://www.thecodingdiaries.com/wp-content/uploads/2014/05/Screen-Shot-2014-05-29-at-3.23.52-PM.png" width="703" height="130" /></a>
</p>

<p>
  &nbsp;
</p>

<p>
  Instead of being able to see my project in my local browser by just typing <span style="color: #000000;"><b>$ python manage.py runserver</b>, I had to type <strong>$ </strong><b>python </b><span style="text-decoration: underline;"><b>manage.py</b></span><b> runserver 0.0.0.0:8000</b> to see my project in <span style="text-decoration: underline;">http://127.0.0.1:8889/</span>.</span>
</p>

<p>
  Meanwhile, to see my Tango with Django project, I had to run make sure to specify a local port too: <strong>$ python manage.py runserver 0.0.0.0:8887</strong> and http://127.0.0.1:8887/rango.
</p>

<p>
  NOTE: to start working on the project again, follow these steps after getting back into the <strong>gswd-vagrant</strong> folder:<br /> $ vagrant suspend<br /> $ vagrant up #start the vagrant up again<br /> $ vagrant ssh #password is vagrant<br /> $ source ~/blog-venv/bin/activate
</p>

<p>
  NOTE: if there is a vagrant conflict, make sure to vagrant halt on the other instance of vagrant running.
</p>