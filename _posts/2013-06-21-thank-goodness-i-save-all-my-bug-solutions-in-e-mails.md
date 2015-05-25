---
title: '<span data-rel="title">Thank goodness I save all my bug solutions in e-mails</span>'
author: LP
layout: post
permalink: /thank-goodness-i-save-all-my-bug-solutions-in-e-mails/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 1553181016
---
<span data-rel="content">

<p>
  <a href="http://incident57.com/codekit/">Codekit</a> (software which web developers use for lots of cool things, but which I mainly use for compiling LESS) started acting up after a reboot of my computer recently, showing me an error starting with the following words:
</p>

<blockquote>
  <p>
    Error: EACCES, permission denied &#8216;[FILEPATH]&#8217;&#8230;
  </p>
</blockquote>

<p>
  I remember googling around and landing upon <a href="https://help.ubuntu.com/community/FilePermissions">linux file permissions documentation</a>, and eventually realizing that if I went into the root (<strong>sudo -s</strong> &#8212; a command I learned from a hackathon teammate just the week before, thanks A.!) and did <strong>chmod a+rw style.css</strong>, the compilation error was magically solved.
</p>

<p>
  Now, I am about 80% certain that my fix isn&#8217;t a 100% true fix, but I am *so glad* I recorded the method I used to solve it in e-mail because&#8230; yeah, the problem just popped up again. And I went crazy for a few minutes doing git revert and trying to figure out what went wrong (I was only editing a .less file!) before I realized that the codekit error looked kind of familiar, and&#8230; hmm. Searching &#8220;EACCES&#8221; pulled up the solution I had documented in my own e-mail archives.
</p>

<p>
  Moral to the story: document your bug fix methods (even if temporary), especially if the fixes are obscure.
</p></span>