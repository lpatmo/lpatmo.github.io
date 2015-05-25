---
title: '<span data-rel="title">Day 2 Random: #100daysofcode</span>'
author: LP
layout: post
permalink: /day-2-random-100daysofcode/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 
---
<span data-rel="content">

<ul>
  <li>
    In a tuple such as: <pre><code>  GENDER_CHOICES = (
    ("M", "Male"),
    ("F", "Female"),
    ("?", "Unknown")
  )
</code></pre>
    
    <p>
      &#8230; within <code>models.py</code>, the first value is written into the database. The second value is the value that is displayed for the user.</li> 
      
      <li>
        After writing up models.py, you need to run these two migrations to sync the database: <pre><code>python manage.py makemigrations academy
python manage.py migrate academy
</code></pre>
      </li>
      
      <li>
        Adding the <code>-p</code> flag can make TWO directories! For example: <pre><code>mkdir -p project/subdirectory1/subdirectory2
</code></pre>
      </li>
      
      <li>
        By default, <code>BASE_DIR</code> is set to the root of your project file &#8212; the same spot where you can find <code>manage.py</code>.
      </li>
      <li>
        open(): <a href="https://docs.python.org/2/library/functions.html#open">https://docs.python.org/2/library/functions.html#open</a>
      </li></ul> 
      
      <p>
        *<code>csv.DictReader(open(csv_file))</code> will return a list with each row in the file as a dictionary.
      </p>
      
      <ul>
        <li>
          OMG THIS INSIDE admin.py IS MAGIC:
        </li>
      </ul>
      
      <pre><code>from django.contrib import admin
from academy.models import Invite

class InviteAdmin(admin.ModelAdmin):
    list_display = ("name", "branch", "gender", "date_of_birth", "race")
    list_filter = ("branch", "gender", "race")
    search_fields = ("name",)

admin.site.register(Invite, InviteAdmin)
</code></pre>
      
      <p>
        *If you just want to &#8216;deploy&#8217; a site so that it&#8217;s available to other users in your intranet network (e.g. other people in your office), try this: 1) Find your IP address by typing <code>ifconfig</code> into your command line. 2) Run <code>$ python manage.py runserver 0.0.0.0:8000</code> in your terminal. 3) Paste in http://[IP ADDRESS]:8000/admin/ into your browser. Theoretically, this should work, but it did not work for me just now. :(
      </p>
      
      <ul>
        <li>
          Every time you change your models, in newer versions of Django, run something like: <code>python manage.py makemigrations appname</code>. Every time a migration is run, a file will be added to <code>/appname/migrations</code>. Next, you have to actually run the migration: <code>python manage.py migrate academy</code>.
        </li>
        <li>
          <code>list_display</code> is awesome. So is <code>list_editable</code>.
        </li>
      </ul>
      
      <p>
        Thanks much to <a href="http://first-django-admin.readthedocs.org/en/latest/">http://first-django-admin.readthedocs.org/en/latest/</a> for the surprisingly straightforward and short django tutorial.
      </p>
      
      <p>
        This post is a part of the <a href="http://www.thecodingdiaries.com/the-100daysofcode-challenge/#sthash.eAFLTbDO.dpbs">#100daysofcode</a> challenge.
      </p></span>