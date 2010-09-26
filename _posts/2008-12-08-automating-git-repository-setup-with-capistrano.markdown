--- 
wordpress_id: 31
title: Automating Git repository setup with Capistrano
wordpress_url: http://www.elaptics.co.uk/?p=31
layout: post
---
Setting up a remote repository for Git is really easy, but who wants to type things unnecessarily? Tonight I knocked up a task for Capistrano which <em>gitify's</em> your current directory then creates a remote git repository and pushes to it.

It's based on a bit of code by <a href="http://peepcode.com" target="_blank">Geoffrey Grosenbach</a> but modified for my needs. I have a VPS which is where I want to host my repositories  — this should also work if you're running on a shared host like Dreamhost where you have ssh access, though I haven't tested it.

Simply cut and paste the following code into <code>~/.caprc</code> then you can run:

<code>cap git:setup scm=t</code>

If it's a Rails app then you can also do

<code>cap git:setup scm=t railsapp=t</code>

which will add .gitignore files to exclude the basics like log and temp files, .DS_Store, *.sqlite3 and the api docs

<script src="http://gist.github.com/33269.js"></script>
 
