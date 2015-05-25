---
title: '<span data-rel="title">Configuring the terminal to open Sublime Text files with the &#8216;subl&#8217; command</span>'
author: LP
layout: post
permalink: /configuring-the-terminal-to-open-sublime-text-files/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 1169546148
---
<span data-rel="content">

<p>
  I&#8217;d noticed a couple of people typing in &#8220;subl file/path&#8221; in their terminal to open up a file after they cd&#8217;ed into the folder, but much to my surprise, the &#8220;subl&#8221; command did not work for me. Turns out I had yet to install it!
</p>

<p>
  Sounds easy, right?
</p>

<p>
  I googled the instructions pretty easily (<a href="http://www.sublimetext.com/docs/2/osx_command_line.html" target="_blank">http://www.sublimetext.com/docs/2/osx_command_line.html)</a>, but predictably, like much of the things I have to install, the attempt failed &#8212; I kept getting back an error that said &#8220;bin/subl&#8221; did not exist. Googled some more, and found <a href="http://stackoverflow.com/questions/10660999/sublime-text-2-cant-create-symlink-to-subl-says-bin-subl-no-such-file-or-di" target="_blank">this stackoverflow post</a> &#8212; which contained an answer suggesting this solution:
</p>

<p>
  ln -s &#8220;/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl&#8221; /usr/local/bin/subl
</p>

<p>
  Another reminder to google the errors you encounter, I suppose &#8212; especially when installing software.
</p>

<p>
  &nbsp;
</p>

<p>
  &nbsp;
</p></span>