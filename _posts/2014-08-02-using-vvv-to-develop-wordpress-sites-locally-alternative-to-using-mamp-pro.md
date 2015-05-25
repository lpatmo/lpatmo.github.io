---
title: '<span data-rel="title">Using VVV to develop multiple WordPress sites locally (alternative to using MAMP Pro!)</span>'
author: LP
layout: post
permalink: /using-vvv-to-develop-wordpress-sites-locally-alternative-to-using-mamp-pro/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2895693645
---

<p>
  Went to my first <a href="https://twitter.com/hashtag/wcnyc?src=hash" target="_blank">Wordcamp in NYC</a> this weekend! Funny enough, one of the first people I met upon entering the conference was <a href="https://twitter.com/karmatosed" target="_blank">@karmatosed</a>, whose <a href="http://www.packtpub.com/buddypress-theme-development/book?utm_source=social+media&utm_medium=email&utm_campaign=social+media" target="_blank">Buddypress Theme Development book</a> I had just downloaded for offline reading on my Safari Books Online mobile app. (I had *literally* been reading it on the subway just a few minutes before I met her. :D) So many accomplished WordPress developers at this conference.
</p>

<p>
  Anyway, this post is about how I learned to set up multiple local instances of WordPress on my macbook air WITHOUT using MAMP Pro (go Vagrant!), thanks much to <a href="http://twitter.com/drewapicture" target="_blank">@DrewAPicture</a>, a web engineer at <a href="10up.com" target="_blank">10Up</a> and contributor to WordPress and to VVV. He helped me figure out &#8220;what&#8217;s next?&#8221; after the  setup instructions in <a href="https://github.com/Varying-Vagrant-Vagrants/VVV" target="_blank">https://github.com/Varying-Vagrant-Vagrants/VVV</a> left me hanging.
</p>

<p>
  I thought the instructions in the initial README were great for getting my first http://local.wordpress.dev site set up. But what if I wanted to set up another instance? Below are my notes.
</p>

<p>
  <strong>STEPS FOR CREATING ANOTHER LOCAL WP INSTANCE:</strong><br /> 0. Create a new folder in vagrant-local/www. For example: <strong>vagrant-local/www/name-of-your-project/</strong>
</p>

<p>
  1. In your <strong>VVV/database</strong> folder, change the file name of <strong>init-custom-sample.sql</strong> to <strong>init-custom.sql</strong>.
</p>

<p>
  2. Inside <strong>vagrant-local/database/init-custom.sql</strong>, create the databases. For example:
</p>

<pre class="prettyprint">CREATE DATABASE IF NOT EXISTS `name-of-project`;
GRANT ALL PRIVILEGES ON `name-of-project`.* TO &#39;wp&#39;@&#39;localhost&#39; IDENTIFIED BY &#39;wp&#39;;CREATE DATABASE IF NOT EXISTS `name-of-project2`;
GRANT ALL PRIVILEGES ON `name-or-project2`.* TO &#39;wp&#39;@&#39;localhost&#39; IDENTIFIED BY &#39;wp&#39;;</pre>

<p>
  4. In <strong>vagrant-local/config/nginx-config/sites/</strong>, create <strong>servers</strong><b>.conf</b>. This is where you&#8217;ll configure your nginx. If you have multiple dev instances, you&#8217;ll have multiple <strong>server{ }</strong> blocks. For example:
</p>

<pre class="prettyprint">server {
listen       80;
listen       443 ssl;
server_name  name-of-project.dev;
root         &#47;srv&#47;www&#47;name-of-project;
include &#47;etc&#47;nginx&#47;nginx-wp-common.conf;
}</pre>

<pre class="prettyprint">server {
listen       80;
listen       443 ssl;
server_name  name-of-project2.dev;
root         &#47;srv&#47;www&#47;name-of-project2;
include &#47;etc&#47;nginx&#47;nginx-wp-common.conf;
}</pre>

<p>
  5. <strong>In your terminal, make sure the vagrant IPs are added to the bottom of your ~/etc/hosts file.</strong>
</p>

<pre class="prettyprint">$ sudo -s
$ cd ~&#47;
$ cd ..&#47;..&#47;
$ cd etc
$ vim hosts</pre>

<p>
  Make sure:
</p>

<pre class="prettyprint">192.168.50.4 name-of-project.dev
192.168.50.4 name-of-project2.dev</pre>

<p>
  … is added to the bottom of the hosts file.
</p>

<p>
  Type <b>exit</b> to get out.
</p>

<p>
  6. Run<strong> vagrant provision </strong>in your terminal so that the databases changes are registered.
</p>

<p>
  7. Download wordpress in vagrant using the command line.
</p>

<pre class="prettyprint">$ vagrant ssh
$ cd ..&#47;..&#47;
$ cd srv&#47;www&#47;name-of-project
$ wp core download</pre>

<p>
  <b>exit</b> to get out of vagrant.
</p>

<p>
  8. Navigate to http://name-of-project.dev in the browser to create a new wp-config.php file, and follow the steps.
</p>

<p>
  Your database host should be <strong>localhost</strong>, and the user and password should be associated with what you input in step #2. In this example, the user and password are &#8216;wp&#8217; and &#8216;wp.&#8217;
</p>

<p>
  9. You should now be able to see your local wordpress installation at <strong>http://name-of-project.dev/</strong>!
</p>

<p>
  10. In practice, it&#8217;s better not to use version control on the core WordPress docs. You can <strong>git init</strong> inside <strong>vagrant-local/www/name-of-your-project/wp-content/themes/your-own-wordpress-theme</strong> to use version control specifically on your theme.
</p>

<p>
  &nbsp;
</p>