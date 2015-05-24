---
title: '<span data-rel="title">Never going back after git</span>'
author: LP
layout: post
permalink: /never-going-back-after-git/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 1452243416
---
<span data-rel="content">

<p>
  <strong>UPDATE: In March 2014, I attended an official git training by <a href="https://twitter.com/peterbell" target="_blank">@PeterBell</a>, hosted at Gilt! Here are my more comprehensive notes from the training: <a href="https://github.com/lpatmo/git-training-notes" target="_blank">https://github.com/lpatmo/git-training-notes</a></strong>
</p>

<p>
  Git was a bit confusing when I first started exploring it, coming from using Subversion for version control. I was used to having everything I committed go <em>live</em>, and the idea that everything I committed would go to some virtual staging area on my computer <em>but not on my github account</em> did not immediately click until&#8230; well, it clicked.
</p>

<p>
  And after that, everything was fine.
</p>

<p>
  (As I heard a tech conference co-attendee explain to a github beginner once, the value in not having every single thing you commit automatically be seen live by your co-workers is that it gives you room to make mistakes. You can think of a &#8220;commit&#8221; as a documented &#8220;save&#8221;/snapshot of your code. But git lets you control which commits you push to your teammates, whereas subversion does not.)
</p>

<p>
  <span style="color: #000000;"><strong>The typical commands I use when starting a new project with git:</strong></span>
</p>

<ul>
  <li>
    <strong style="font-size: 16px;">mkdir </strong>// Creates a directory
  </li>
  <li>
    <strong>git init</strong> // I type this after I cd into the directory to initialize the git directory
  </li>
  <li>
    <strong>[Create a repository on github.com]</strong> // All it takes is a click of a button &#8212; but this, confusingly, has to be done manually
  </li>
  <li>
    <span style="color: #000000;"><span style="color: #000000;"><strong>[Copy/paste the two commands output in the &#8220;repository created&#8221; page into my terminal] </strong>// The first set of instructions does some extra stuff that I don&#8217;t need if I already initialized the repository using git init, I believe. //</span></span> <pre><code>git remote add origin https://github.com/&lt;strong>username&lt;/strong>/&lt;strong>repository-name&lt;/strong>.git </code></pre>
    
    <pre><code>git push -u origin master</code></pre>
  </li>
  
  <li>
    <strong>touch index.html</strong> // This creates a file called index.html in my current directory
  </li>
  <li>
    <strong>pwd</strong> // Optional command that tells me where I am
  </li>
  <li>
    <strong>ls // </strong>This command lists the files that are in the directory. Index.html should be in here now.
  </li>
  <li>
    <strong>subl .</strong> // This command is configured using the sublime text editor, and opens up all the files in the directory in sublime.
  </li>
  <li>
    <strong>git add index.html </strong>//Adds the file so that it can be committed
  </li>
  <li>
    <strong>git commit index.html -m &#8220;first commit&#8221;</strong> //My first commit! If I have a couple of files ready to be committed, I can optionally type git commit . -m &#8220;first commit&#8221;. Be sure that you don&#8217;t forget the &#8220;-m&#8221; or the comment that you must type to explain the change you are documenting.
  </li>
  <li>
    <strong>git status</strong> //Tells me what files I&#8217;ve changed by editing and saving in the editor, and which need to be <em>added</em> or <em>committed</em>. I&#8217;ll type this often to figure out which files I&#8217;ve changed by saving in the text editor.
  </li>
  <li>
    <strong>git log </strong>//Tells me what my most recent commits were. Note that if I push my changes up to github.com, I&#8217;ll also be able to see my commit change logs there in a nicely visually highlighted way (green = additions; red = deletions).
  </li>
  <li>
    <strong>git push </strong>//Pushes up my committed files to my github.com account when I&#8217;m satisfied with my commits. I&#8217;ll do this in bursts.
  </li>
  <li>
    <strong>git pull</strong> // I update my local files with the commits that my teammates pushed up to the shared repository. I&#8217;ll do this before I start the day, and throughout the day.
  </li>
</ul>

<p>
  <span style="color: #000000;"><strong>Bug tracking ease</strong></span>
</p>

<p>
  OH! Did I mention github&#8217;s issues/bug tracker and milestone counters? When I make a commit that resolves an issue number, I can write &#8220;<strong>resolves #87</strong>&#8221; in the commit message, and <em>it&#8217;ll automatically close issue #87 within the repository</em>. I found it amusing that at one point, I was using trello (a project management platform) with some hackathon friends to organize our bugs. We totally could have used github!
</p>

<p>
  <span style="color: #000000;"><strong>Yes, to be sure&#8230;</strong></span>
</p>

<p>
  Of course, merge issues often come up, and your terminal might spit back frustrating messages such as &#8220;You do not have permission&#8230;&#8221; or &#8220;Merge conflict in FILEPATH.&#8221; I&#8217;ll discuss a few of the most common error messages I&#8217;ve encountered in another post.
</p>

<p>
  But anyway&#8230; Version control FTW. I am glad I won&#8217;t be going back to drag-and-drop FTP anytime soon.
</p></span>