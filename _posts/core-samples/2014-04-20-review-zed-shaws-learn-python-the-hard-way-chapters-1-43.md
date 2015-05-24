---
title: '<span data-rel="title">REVIEW: Zed Shaw&#8217;s &#8216;Learn Python The Hard Way&#8217; (Chapters 1-43)</span>'
author: LP
layout: post
permalink: /review-zed-shaws-learn-python-the-hard-way-chapters-1-43/
wiziapp_processed:
  - 1
dsq_thread_id:
  - 2662851520
---
<span data-rel="content">

<p>
  Learning Python was a lot easier after being familiar with Javascript.
</p>

<p>
  I was warned about Python&#8217;s spacing and indentation issues, which I took in stride. I also really enjoyed the lack of extra () and {}. Also, coming from javascript, I felt that the language was pretty intuitive. <em>For loops</em> and <em>while loops</em> were similar. There was even an equivalent between the <strong>console.log() </strong>in javascript and <strong>print</strong> in Python; I remember asking, several months ago, the difference between <strong>console.log</strong> and <strong>return</strong> in javascript, and I can only now belatedly appreciate just how elementary that question was.
</p>

<p>
  For beginners completely new to web development, I&#8217;d still recommend learning html/css/javascript first, along with a simple introduction to github, just so they can get over the hurdles of understanding functions for the first time, why they need to use the terminal, and how file paths work, etc.
</p>

<p>
  Anyway. I should probably preface that before I started <a href="http://learnpythonthehardway.org/book/">Learn Python The Hard Way (LPTHW)</a> this time, I went through about 43% of <a href="http://www.codecademy.com/tracks/python" target="_blank">Codecademy&#8217;s Python track</a>. It was helpful insofar as getting me used to Python syntax (its unique way of writing functions!) and some simple exercises, but LPTHW is definitely the meatier of the two tutorials. Here&#8217;s my brief review of the first 43 chapters:
</p>

<p>
  <span style="text-decoration: underline;"><strong>Chapters 1-10</strong></span>
</p>

<p>
  Breezed though these chapters, mainly because there are only so many differences between javascript and python re: comments, variables, and strings. I think I&#8217;d previously written about beginners possibly getting <a title="Teaching a beginner Lessons 0 and 1 of Zed Shaw’s Learn Python The Hard Way" href="http://www.thecodingdiaries.com/teaching-a-beginner-lessons-0-and-1-of-zed-shaws-learn-python-the-hard-way/" target="_blank">tripped up by having to use the terminal</a>. The other thing that must&#8217;ve tripped up true programming beginners would probably be typos, but I didn&#8217;t have as much a problem with that. The thing I did have to re-familiarize myself with was the concept of substitution:
</p>

<pre class="prettyprint">my_eyes = &#39;brown&#39;
my_hair = &#39;black&#39;
print &#34;He&#39;s got %s eyes and %s hair.&#34; % (my_eyes, my_hair)</pre>

<p>
  <span style="text-decoration: underline;"><strong>Chapters 11-20</strong></span>
</p>

<p>
  Some notes for review:
</p>

<ul>
  <li>
    Put a comma at the end of each <strong>print</strong> line so that <strong>print </strong>doesn&#8217;t end with a newline character and go to the next line (Chapter 11)
  </li>
  <li>
    <strong>variable = raw_input(&#8220;> &#8220;) </strong> (Chapter 11)
  </li>
  <li>
    <strong>txt = open(filename)</strong> creates a variable named &#8216;txt&#8217; and opens up the file. <strong>print txt.read() </strong>opens up the file and spews out the contents of the file. Commenting each line of code helped me understand it a lot better. (Chapter 15)
  </li>
  <li>
    <strong>from sys import argv</strong>, typically seen at the top of a file, means that sys is a <em>package</em>, and the <em>argv</em> feature is retrieved from that package. (Chapter 15)
  </li>
  <li>
    Googled why I had to do <strong>output.close(): </strong>https://mail.python.org/pipermail/tutor/2012-January/088031.html (Chapter 17)
  </li>
</ul>

<p>
  <span style="text-decoration: underline;"><span style="color: #000000; text-decoration: underline;"><b>Chapters 21-3</b><strong></strong></span></span>
</p>

<ul>
  <li>
    <strong>int(raw_input()) </strong>vs. <strong>float(raw_input())</strong>
  </li>
  <li>
    control-d exits you out of the python shell
  </li>
  <li>
    If you have a file named example.py, you can type <strong>python </strong>to get into the python shell, type <strong>from example import * </strong>to import all the features from the example.py package, type <strong>help(example)</strong> to see the contents of that file, and run commands against that file.
  </li>
  <li>
    Make sure to change a piece of string into a list using <strong>.split(&#8216; &#8216;) </strong>first if you want to use something like <strong>.pop(0)</strong> to break off the first word in the list.
  </li>
  <li>
    <pre class="prettyprint">def break_words(stuff):
&#34;&#34;&#34;This function will break up words for us.&#34;&#34;&#34;
words = stuff.split(&#39; &#39;)
return words</pre>
  </li>
  
  <li>
    Exercise 26: more practice with functions.
  </li>
  <li>
    Exercise 27: <pre class="prettyprint">TRUE or FALSE -&gt; if has true in it, true.
TRUE AND FALSE -&gt; if has false in it, false.</pre>
  </li>
  
  <li>
    Exercise 30: Story with a bear.
  </li>
</ul>

<p>
  <span style="text-decoration: underline;"><strong>Chapters 31-43</strong></span>
</p>

<ul>
  <li>
    Start with an empty list<br /> <code class="prettyprint">elements = &#91;&#93;</code><br /> , then use the range function to count from 0 to 5</p> <pre class="prettyprint">for i in range(0,6):
     print &#34;Adding %d to the list.&#34; % i
     #append is a function that lists understand
     elements.append(i)</pre>
  </li>
  
  <li>
    There a bunch of methods you can use on lists, like <strong>list.append(), list.extend(), list.pop(), list.sort(), list.reverse()</strong>, etc.: <a href="https://docs.python.org/2/tutorial/datastructures.html" target="_blank">https://docs.python.org/2/tutorial/datastructures.html</a>
  </li>
  <li>
    My solution for printing out a 2D list like [[1,2,3][4,5,6]]: <pre class="prettyprint">#starting with an empty list
elements = &#91;&#93;
#then use the range function to do 0 to 5 counts
for i in range(0,2):
     new = &#91;&#93;
     #append is a function that lists understand
     for j in range(1,4):
         if i == 1:
            new.append(j+3)
         else:
            new.append(j)
     elements.append(new)
# now we can print them out too
print elements</pre>
  </li>
  
  <li>
    Use <strong>while</strong> loops sparingly in python. Usually a <strong>for </strong>loop is better.
  </li>
  <li>
    Review your while statements and make sure that the thing you are testing will become False at some point.
  </li>
  <li>
    When in doubt, print out your test variable at the top and bottom of the while-loop to see what it&#8217;s doing.
  </li>
  <li>
    Think of using <strong>print</strong> like using your console.log() in javascript.
  </li>
  <li>
    Every <strong>if </strong>statement must also have an <span style="color: #000000;"><b>else</b>.</span>
  </li>
  <li>
    Using try/except: <pre class="prettyprint">def start():
    print &#34;You are in a dark room.&#34;
    print &#34;There is a door to your right and left.&#34;
    print &#34;Which one do you take?&#34;

    next = raw_input(&#34;&gt; &#34;)
    #print (how_much)

    if next == &#34;left&#34;:
        bear_room()
    elif next == &#34;right&#34;:
        cthulhu_room()
    else:
        try:
            how_much = int(next)
            print &#34;yay number!&#34;
        except ValueError:
            print &#34;Not a number or left or right. You stumble around the room until you starve.&#34;
start()</pre>
  </li>
  
  <li>
    <strong>Q:</strong> What&#8217;s the relationship between dir(something) and the &#8220;class&#8221; of something?<br /> <strong>A:</strong> dir(something) gives you all the attributes of the object. The class is like the blueprint for the house.
  </li>
  <li>
    You can only use numbers to retrieve items from a list. You can use any type to retrieve items from a dictionary. For example: list[1] versus dictionary[&#8216;word&#8217;].
  </li>
  <li>
    <pre class="prettyprint">for a, b in states.items():
    print &#34;%s is abbreviated %s&#34; % (a, b)</pre>
  </li>
  
  <li>
    In Exercise 40 we finally start talking about classes!<br /> <blockquote>
      <p>
        &#8220;Here&#8217;s why classes are used instead of modules: You can take the above class and use it to craft many of them, millions at a time if you want, and they won&#8217;t interfere with each other. With modules, when you import there is only one for the entire program unless you do some monster hacks.&#8221;
      </p>
    </blockquote>
  </li>
  
  <li>
    When you instantiate a class, you get an object. Example: <pre class="prettyprint">thing = MyStuff()
thing.apple()
print thing.tangerine</pre>
  </li>
  
  <li>
    Exercise 41 is pretty fun: you run a script that helps you memorize how to read each of the components in a module. For example, in English, <strong>class apple(object): def sky(self, horse)</strong> translates to &#8220;class apple has-a function named sky that takes self and horse parameters.&#8221;
  </li>
</ul>

<p>
  One day I&#8217;m going to look back on these notes and think: &#8220;Did I really have to take notes on that?&#8221; But in the meantime&#8230;
</p>

<p>
  Update: This already happened for some bullet points, hah!
</p></span>