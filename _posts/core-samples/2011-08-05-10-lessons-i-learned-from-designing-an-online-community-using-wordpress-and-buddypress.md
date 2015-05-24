---
title: '<span data-rel="title">10 Lessons I Learned From Designing An Online Community Using WordPress and Buddypress</span>'
author: LP
layout: post
categories: lessons-learned, wordpress
tags: [buddypress, wordpress]
permalink: /10-lessons-i-learned-from-designing-an-online-community-using-wordpress-and-buddypress/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 1306673432
---
<span data-rel="content">

<p>
  I re-discovered my fascination with online community building around the same time I subscribed to a shared hosting service, installed WordPress, discovered the Buddypress plugin, and stumbled upon some awesome code discussion forums online. This was December 2010. The discovery turned into an independent study I dubbed &#8220;Volunteerism in a Web 2.0 World,&#8221; which turned into the development of a website and lots of meetings and several pages of an annotated bibliography &#8212; all of which I submitted to my Research in Practice Program (RIPP) advisor at the end of the semester.
</p>

<p>
  <center>
    <img src="http://farm7.staticflickr.com/6033/6345644811_a30ed70b2d.jpg" width="560" />
  </center>
</p>

<p>
  Over the course of my meetings with &#8220;stakeholders&#8221; (Duke students and administrators) to asses the value of the &#8220;website&#8221; (<a href="http://dukeimpact.org" target="_blank">an online social network for Duke civic engagement</a>), I learned a few things about designing an online community using WordPress and Buddypress.
</p>

<h3>
  1) Your site needs an FAQ.
</h3>

<p>
  No, really. It does. Although you personally might think that the activity feeds and groups and profile editing links are in the most obvious locations in the world, your users will not. They&#8217;re used to their own oft-frequented social networks (cough, Facebook), and  they&#8217;ll ask you why clicking on their avatar doesn&#8217;t automatically bring them to a &#8220;change your profile picture&#8221; page or if logging into your site using Facebook Connect will mean that everything they post will automatically get cross-posted to their Facebook wall. In addition, users want to know about your site features. How does your specific network make project management or content sharing easier than expected, for example?
</p>

<h3>
  2) Speaking of Facebook Connect&#8230;
</h3>

<p>
  Do it. People hate creating new passwords for new sites they&#8217;re not certain they&#8217;ll visit twice. The only caveat I have is that some people are suspicious of entering their account information into any third-party site. Therefore I recommend giving people single sign-on options using Twitter, Linkedin, OpenID, Livejournal, etc. as well as Facebook.
</p>

<h3>
  3) Learn HTML and CSS. Understanding PHP wouldn&#8217;t hurt either.
</h3>

<p>
  Trust me &#8212; it helps a lot to know HTML and at least some basic CSS. (If you don&#8217;t know how to start, Google is your friend! There are <a href="http://www.htmldog.com/guides/cssbeginner/" target="_blank">so</a> <a href="http://www.w3schools.com/html/default.asp" target="_blank">many</a> free tutorials out there.) Understanding the style.css file is all you need to start changing the color, style, and positioning of the components of your theme. Along the way you&#8217;ll probably start staring at all the PHP… and be forced to understand it as well. :)
</p>

<h3>
  4) Excited volunteers =/= a successful community.
</h3>

<p>
  I approached a lot of people for feedback about my project, and a surprisingly high number were interested in getting involved. After happily accepting their support, nothing happened. Turns out there are two lessons to gleam here: 1) Figuring out how to manage volunteers in a way that also respects their time and their interests is difficult. 2) The people excited enough to volunteer are already sold on your product, so it&#8217;s important not to take their excitement <em>too </em> seriously. The rest of your target market still needs to be convinced to care about your community enough to join.
</p>

<h3>
  5) Make your homepage interesting enough to visit twice.
</h3>

<p>
  My landing page was static for the first few weeks. Then I tried to spice it up by embedding a dynamic Wix banner with pretty photographs and an inline menu that walked the user through all the features on the site. Then I realized <em>hey, that&#8217;s still static</em> and eventually figured out how to tweak the activity.php file (which contained the sitewide newstream, basically) and move it to the home page.
</p>

<p>
  The point is, you want users to instantaneously be able to see new content that&#8217;s relevant to them every time they load up your page. There&#8217;s probably a reason <a href="http://quora.com" target="_blank">Quora</a>, <a href="http://stackoverflow.com" target="_blank">Stackoverflow</a> and most Ning networks<a href="http://thehpalliance.org/" target="_blank"> </a>all have news feeds on their front pages.
</p>

<h3>
  6) Clearly define your niche<strong>. </strong>
</h3>

<p>
  Even if your network shared some of the highest quality content on the internet, users aren&#8217;t going to come back to it when they can visit Google News or The New York Times for their daily news intake. It&#8217;s important to clearly define your site&#8217;s niche so that users will have an easier time understanding how your site adds value to their lives. For example, <a href="http://quora.com" target="_blank">Quora</a> is the social network where one gets their questions answered; <a href="http://stackoverflow.com" target="_blank">Stackoverflow</a> is a Q&A network for programmers; <a href="http://linkedin.com" target="_blank">Linkedin</a> is a specific network for jobhunting professionals. What specific need does your social network cater to?
</p>

<h3>
  7) Don&#8217;t be afraid to ask for e-mail addresses.
</h3>

<p>
  I initially suffered from a fear of spamming people. Then I realized that <em>every site I&#8217;ve registered an account with</em> has sent me a welcome e-mail. And then they keep on sending me monthly, if not weekly  newsletters. Why? To make sure I remember that they exist. Even Facebook, which has become an automatic &#8220;second window&#8221; for many users (the first, obviously, is e-mail) still e-mails out tons of annoying notifications and friendship search reminders to new registrants.
</p>

<p>
  Moral of the story: as long as you give the user a clear &#8220;unsubscribe&#8221; or &#8220;manage preferences&#8221; link, you shouldn&#8217;t feel too bad.
</p>

<h3>
  8) Beware of outdated plugins and themes.
</h3>

<p>
  Look at the description closely and check to see if it&#8217;s been tested up to the WordPress version you&#8217;ve installed. If you&#8217;re unsure, search for the plugin forums (every WordPress plugin should have one) and see the latest praises or issues people are discussing on the threads.
</p>

<h3>
  9) If a new theme or plugin crashes your site, rename or delete it.
</h3>

<p>
  The first time I got a PHP error from a rogue plugin, I called tech support at my hosting company &#8212; who helpfully fixed the problem for me by asking me about the last thing I did (&#8220;Install a plugin,&#8221; I said) and going into my files to rename the plugin.
</p>

<p>
  Eventually I learned how to use my hosting account properly by finding the files myself. -_-
</p>

<h3>
  10) Cook a stew, not a souffle.
</h3>

<p>
  Tony Brown, an entrepreneur and co-director of the Hart Leadership Program at Duke, gave me this valuable piece of advice when I cold-emailed him to request a meeting.  I had originally intended to obtain advice about how a social network that engaged Duke students could potentially also support non-profits in Durham (Duke-Durham relations were part of his domain). He told me to stop worrying about the details and to treat the project as a stew, not a souffle.
</p>

<p>
  In other words: Focus first on gaining traction (Does the product add value? Will the targeted really use it?), and <em>then</em> worry about adding all the cool features, target market expansion, and awesome partnerships.
</p></span>