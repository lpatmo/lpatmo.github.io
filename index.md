---
layout: page
title: The Coding Diaries
tagline: Front-end dev with a non-traditional background (no CS degree). My hope is for this blog to be helpful for others starting out too.
---
{% include JB/setup %}

<div class="container-fluid">
	<div class="row">
	 <div class="col-md-6">
  {% for post in site.posts %}
 <h2> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
    	<p>
    		{{post.content}}

    	</p>

  {% endfor %}
  	</div>

   <div class="col-md-3">
      <ul class="notes">
        <li class="notes" style="padding: 1em; word-wrap: break-word; overflow: hidden;">Hi, I'm Linda! I enjoy going to tech meetups, learning web development, and blogging about the learning path. Follow me on twitter:<a href="http://bit.ly/1epoq9z" target="_blank">@LPnotes</a></li>
      </ul>
          <!-- Begin MailChimp Signup Form -->
            <link href="//cdn-images.mailchimp.com/embedcode/classic-081711.css" rel="stylesheet" type="text/css">
            <style type="text/css">
              #mc_embed_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; }
              /* Add your own MailChimp form style overrides in your site stylesheet or in this style block.
                 We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
            </style>
            <div id="mc_embed_signup">
            <form action="//thecodingdiaries.us4.list-manage.com/subscribe/post?u=3c05880570e60e42c378657f6&amp;id=58b71c85bd" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
                <div id="mc_embed_signup_scroll">
              <h2>Sign up for monthly updates!</h2>
              <p>I draw together a list of the top resources I find every month.</p>
            <div class="mc-field-group">
              
              <input type="email" value="" name="EMAIL" class="required email" id="mce-EMAIL" placeholder="Email">
            </div>
              <div id="mce-responses" class="clear">
                <div class="response" id="mce-error-response" style="display:none"></div>
                <div class="response" id="mce-success-response" style="display:none"></div>
              </div>    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
                <div style="position: absolute; left: -5000px;"><input type="text" name="b_3c05880570e60e42c378657f6_58b71c85bd" tabindex="-1" value=""></div>
                <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
                </div>
            </form>
            </div>

            <!--End mc_embed_signup-->
   </div>
   <div class="col-md-3">

    <ul class="sidebar">
      {% for post in site.posts %}
        <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>

</div>
</div>
</div>



