---
title: '<span data-rel="title">SASSConf NYC Reportback (2014)</span>'
author: LP
layout: post
permalink: /sassconf-nyc-reportback-2014/
wiziapp_processed:
  - 1
---
<span data-rel="content">

<p>
  I went to <a href="sassconf.com">SASSConf</a> (my first SASS Conference!) in October 2014 and had a blast. The conference &#8212; organized by <a href="https://twitter.com/itsmisscs">@itsmisscs</a> and <a href="https://twitter.com/Snugug">@Snugug</a> and supported by a team of volunteers &#8212; had probably the most robust agenda in a conference I'd seen for a while.
</p>

<p>
  SASSConf took place at convenient time for me &#8212; right when I was just getting into the meat of refactoring some CSS into SCSS for a larger redesign project at work.
</p>

<p>
  The first day of the conference was set aside for scheduled speaker talks, the second day was set aside for two back-to-back workshops (you could choose from one of two during the morning and afternoon), and the third day was set aside for an un-conference. A lot of care was put into everything from speaker accommodations and food to technical learning opportunities. Oh &#8212; and the after-party on Friday encompassed a karoake and open bar that took place on a boat. A boat.
</p>

<img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-4.jpg" alt="A boat!" /> 

<p>
  Before I get into more beautiful boat pictures, though, let me recap my main three technical takeaways from the conference:
</p>

<p>
  <strong>1. What's the point? Don't Repeat Yourself. (DRY)</strong><br /> Instead of writing straight CSS in a single file for a single component, organize your CSS into different files based on meaning (e.g. the names of your partials can be _buttons.scss, _colors.scss, _layout.scss), and use variables and nesting to keep the CSS organized nicely. Doing this helps get rid of repetitive styles.
</p>

<p>
  I also learned that people were actually using different versions of SASS &#8212; i.e. there was "rubysass" versus "libsass." Libsass is a little behind rubysass in its development, but still comes with some advanced features such as maps and lists. There are also a ton of supplementary tools that some SASS developers use such as Compass, Bourbon (a mixin library), grunt.js, gulp.js, etc.
</p>

<p>
  However, my takeaway was that it wasn't important to go out and use every SASS feature or accompanying tool available. You should use SASS in a way that makes sense for your project, keeping in mind that it's supposed to _help _you write CSS more cleanly and follow the DRY way of thinking.
</p>

<p>
  <strong>2. Mobile first!</strong>
</p>

<p>
  I asked some conference-goers &#8212; including <a href="https://twitter.com/jina">@jina</a>, a co-organizer for one of the workshops &#8212; what their opinion was of using max-width vs. min-width media queries, and basically got a unanimous response in favor of mobile first. <em>Min-width</em> media queries it is, then.
</p>

<p>
  In mobile first, you're developing for mobile devices from the start &#8212; making sure your website looks great on phones and tablets &#8212; before adding CSS styles that change the layout of the page as you stretch the page. Basically, one of the advantages of "mobile first" is that you don't need to specify a breakpoint size to target mobile devices only.
</p>

<p>
  <em>(Side note: I'm super glad I hopped on the mobile-first train, since I ended up suggesting it to my coworker, and we made a decision to go with it, and it made every part of the redesign project a lot easier.)</em>
</p>

<p>
  A couple of other tips I picked up re: writing CSS for the responsive web:
</p>

<ul>
  <li>
    Use ems instead of pixels (http://blog.cloudfour.com/the-ems-have-it-proportional-media-queries-ftw/). This might give you problems with IE8, but there are great libraries out there that help fix problems. <strong>UPDATE:</strong> Thanks Ana Tudor for pointing out that this issue isn&#8217;t really an issue anymore! The CloudFour blog post was published in 2012.
  </li>
  <li>
    Use <a href="http://modernizr.com/">modernizr</a>, a javascript library that will do a quick check for what things are supported.
  </li>
  <li>
    <a href="https://github.com/jina/refactoring/blob/master/examples/named-media-queries.scss">https://github.com/jina/refactoring/blob/master/examples/named-media-queries.scss</a> has a a great example of a media query mixin.
  </li>
</ul>

<pre><code>$bp-tiny: 300px;
$bp-small: 500px;
$bp-medium: 600px;
$bp-large: 800px;
$bp-larger: 1000px;
$bp-full: 1200px;`

@mixin breakpoint($media) {
@if $media == bp-tiny {
@media only screen and (min-width: $bp-tiny) {
@content;
}
}
@else if $media == bp-small {
// small and medium are 1px smaller than their previous variable
@media only screen and (min-width: $bp-small - 1) {
@content;
}
}
@else if $media == bp-medium {
@media only screen and (min-width: $bp-medium - 1) {
@content;
}
}
@else if $media == bp-large {
@media only screen and (min-width: $bp-large - 1) {
@content;
}
}
@else if $media == bp-larger {
@media only screen and (min-width: $bp-larger - 1) {
@content;
}
}
@else if $media == bp-full {
@media only screen and (min-width: $bp-full - 1) {
@content;
}
}
}
</code></pre>

<p>
  For a quick demo on use cases, this is what the CSS class .sidebar using the breakpoint mixin looks like when compiled: <a href="http://sassmeister.com/gist/ea430284384722b8f850">http://sassmeister.com/gist/ea430284384722b8f850</a>
</p>

<p>
  <strong>3. Your style guides should be "living."</strong><br /> My takeaways:
</p>

<ul>
  <li>
    "Static (un-automated) documentation is a lie waiting to happen. Live style guides are great." &#8211; anonymous.
  </li>
  <li>
    Basically, the argument for "living style guides" (style guides that developers don't manually have to update, because it updates automatically with CSS commits) is that style guides are fluid and will change. The design will change.
  </li>
  <li>
    Meetup.com has an example of a robust style guide: github.com/meetup/meetup-swatches
  </li>
  <li>
    https://github.com/hagenburger/livingstyleguide-workshop is a ruby gem that lets you easily create a style guide from your existing SCSS files using YAML/Markdown-type syntax.
  </li>
  <li>
    KSS is another popular live style guide creation tool.
  </li>
  <li>
    With style guides, adoption can sometimes be hard. You need to convince developers to use it and maintain it.<br /> <span style="text-decoration: underline;"><strong>HELPFUL REFERENCE LINKS</strong></span><br /> <a href="http://www.anthonydispezio.com/sassconf2014">http://www.anthonydispezio.com/sassconf2014</a>
  </li>
  <li>
    Lots of great examples of advanced uses of SASS &#8212; with links to <a href="http://sassmeister.com">SassMeister</a>, the JSFiddle-equivalent for CSS.
  </li>
</ul>

<p>
  <a href="https://github.com/jina/refactoring/">https://github.com/jina/refactoring/</a>
</p>

<ul>
  <li>
    Lots of great examples from this repo. The media query mixin above is inspired by one of the code examples here.
  </li>
</ul>

<p>
  <img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-2.jpg" alt="SASS Stage" />
</p>

<p>
  Only ~100 people attended the conference. Although this was a relatively small conference, it was clear that SASS was getting more and more widely used. According to a javascript developer I talked to, last year at CSSDevConf over half the talks were about SASS.
</p>

<p>
  <span style="text-decoration: underline;"><strong>OTHER NOTES I JOTTED DOWN</strong></span>
</p>

<ul>
  <li>
    Mathematicians have done very cool animations using pure CSS keyframes/SASS.
  </li>
  <li>
    Hampton (<a href="https://twitter.com/hcatlin">@hcatlin</a>) is the creator of SASS and is mostly working on upgrading libsass (<a href="https://github.com/sass/libsass">https://github.com/sass/libsass</a>) to the same level as RubySASS (<a href="https://rubygems.org/gems/sass">https://rubygems.org/gems/sass</a>), which has a few more advanced features.
  </li>
  <li>
    More advanced features include: SASS lets you iterate over numbers, lists, and maps. You can also use @for, @each, and @while.
  </li>
  <li>
    "Pairing between a designer and a developer is awesome because you're learning from each other." &#8211; <a href="http://twitter.com/jina">@jina</a> (I say this from experience: I totally agree!)
  </li>
</ul>

<p>
  <span style="text-decoration: underline;"><strong>MORE PHOTOS FROM SASSConf 2014</strong></span>
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-5.jpg"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-5.jpg" alt="I won a free conference book!" /></a>
</p>

<p>
  I won a book in a random lottery on the third day (unconference-style)!
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-1.jpg"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-1.jpg" alt="SASS Bag" /></a>
</p>

<p>
  Goodie bags for the attendees.
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-1-1.jpg"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-1-1.jpg" alt="photo 1 (1)" /></a>
</p>

<p>
  Speakers on the first day.
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-2-1.jpg"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-2-1.jpg" alt="photo 2 (1)" /></a>
</p>

<p>
  Guess where the conference was hosted &#8212; at Scholastic Inc.! The last time I'd been in the building was 10 years ago, when I'd won a writing award for a short story as a teenager.
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-3-1.jpg"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-3-1.jpg" alt="photo 3 (1)" /></a>
</p>

<p>
  Beautiful SASSMeister projected on a screen.
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-4-1.jpg"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-4-1.jpg" alt="photo 4 (1)" /></a>
</p>

<p>
  Between decks on the boat. Filtered.
</p>

<p>
  <a href="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-5-1.jpg"><img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-5-1.jpg" alt="photo 5 (1)" /></a>
</p>

<p>
  Is that the Manhattan Bridge?
</p>

<p>
  <img src="http://www.thecodingdiaries.com/wp-content/uploads/2015/02/photo-3.jpg" alt="SASS Boat" />
</p>

<p>
  &nbsp;
</p>

<p>
  &nbsp;
</p></span>