---
title: How to create multiple forks of a git repo
author: LP
layout: post
permalink: /how-to-create-multiple-forks-of-a-git-repo/
---

Thanks to [https://adrianshort.org/create-multiple-forks-of-a-github-repo/](https://adrianshort.org/create-multiple-forks-of-a-github-repo/) for the instructions.

In summary (using Telescope, an open-sourced project on Github, as an example):

<pre>
1. git clone https://github.com/TelescopeJS/Telescope.git cb2

2. git remote rename origin upstream

3. git remote add origin https://github.com/lpatmo/cb2.git

4. git push -u origin master

</pre>