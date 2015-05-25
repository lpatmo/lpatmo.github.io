---
title: '<span data-rel="title">Teaching a beginner Lessons 0 and 1 of Zed Shaw&#8217;s Learn Python The Hard Way</span>'
author: LP
layout: post
permalink: /teaching-a-beginner-lessons-0-and-1-of-zed-shaws-learn-python-the-hard-way/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 1122919137
---
<span data-rel="content">

<p>
  Walking J. (a complete beginner) through lessons 0 and 1 of <a href="http://learnpythonthehardway.org/book/">Learn Python The Hard Way</a> by Zed Shaw, it occurred to me that LPTHW is probably best learned as a beginner when there&#8217;s someone experienced to help you through the setup, and to answer the larger-picture questions of why you are doing what you are doing.
</p>

<p>
  J. uses a PC, is fairly computer literate (he knows general keyboard shortcuts and how to create/delete files and folders), and had actually taken AP Computer Science in high school &#8212; so had some familiarity with Java. But the questions he asked me made me realize how discouraging it can be to try to run through LPTHW when you have no idea about how to set up the development environment, and why the dev environment is set up the way it is.
</p>

<p>
  Some issues that we encountered:
</p>

<p>
  <strong>1) Python wouldn&#8217;t download.</strong> Ha. He had Python already installed, or so he thought &#8212; but then it turned out that he had Python 3 installed of Python 2 (if you read Zed Shaw&#8217;s directions carefully, Python 2 was necessary)&#8230; and <em>then </em>for some reason it took a few minutes longer for his machine to recognize that Python 2 was actually installed. So we waited and waited before he was able to get a successful message upon typing &#8220;python&#8221; in the powershell.
</p>

<p>
  <strong>2) The powershell looks intimidating!</strong> J. was running Windows 7, I believe &#8212; and the powershell came out with this bright blue background. For non-programmers (I remember this too from before I started using the terminal every day), <strong>it looks intimidating as heck</strong>. You don&#8217;t want to type an accidental command that&#8217;ll delete or destroy all your files.
</p>

<p>
  I know, I know &#8212; this fear seems absurd to those who are familiar with the command line. I had to convince him to trust me that A) I wouldn&#8217;t make him type anything that would ruin his computer; B) that it was perfectly okay and normal to use the powershell all the time; all programmers do, especially when they&#8217;re using version control, and that typing &#8220;mkdir new-directory-name&#8221; to create a folder was BETTER than going to the start menu and creating a new folder through the user interface.
</p>

<p>
  Argh. This latter point was definitely something that needed convincing on. Luckily, once he learned the &#8220;mkdir&#8221; command along with the &#8220;cd&#8221; command, I think the uses of the powershell became clearer. And then I referred him to Zed Shaw&#8217;s <a href="http://cli.learncodethehardway.org/book/" target="_blank">Command Line Crash Course</a> . :-P
</p>

<p>
  <strong>3) Understanding how the text editor works in combination with the powershell</strong>. Zed Shaw recommends Notepad++ for Windows users, which is perfectly fine, but I recommended Sublime Text to J. just for the heck of it (and maybe because Sublime is v. pretty). Anyway, from the start there was some slight confusing of Sublime Text <em>with</em> the Powershell &#8212; which made me realize that the clarity of Lesson 0 could have been improved with just a few screenshots. J., from his one high school CS course in the early 2000s, also expected that Sublime would act as a compiler &#8212; which didn&#8217;t happen, of course. I had to tell him to think of Sublime like a Microsoft Word document &#8212; it&#8217;s just the text editor. But you can run it in the command line with &#8220;python filename.py&#8221;, or even preview it in the browser if it&#8217;s a .html file. But by itself, there&#8217;s no built-in &#8220;compile&#8221; or &#8220;preview&#8221; tab.
</p>

<p>
  Setup took longer than I&#8217;d expected, but it was worth it in the end to see the spark of delight in someone&#8217;s eyes, saving a file called ex01.py and running &#8220;python ex01.py&#8221; successfully in their powershell for the first time.
</p>

<p>
  I told J. that he&#8217;d probably be able to catch up with me pretty soon; I&#8217;m only Lesson 11!
</p>

<p>
  &nbsp;
</p>

<p>
  &nbsp;
</p></span>