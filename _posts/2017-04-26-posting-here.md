---
layout: post
title: Posting Here
author: Rill
excerpt: How to write a post to this blog.
tags: [blogging]
permalink: /blog/posting-here
---

I set up [github pages][github pages] with [Jekyll][jekyll]. It is not
necessary to install Jekyll to blog with this
setup. [Github][github pages] and [Jekyll][jekyll] do all the heavy
lifting to build the blog when you `push` your posts using `git`.

Before You Begin Writing
------------------------

Clone the [F123 blog][f123blog]. You only need to do this once per machine.

    git clone https://github.com/f123/f123.github.io.git    
	
Do a `git pull` before you begin every time before writing and
publishing your post. Make sure you are in the directory containing the web site repository, like this, and then pull:

cd f123.github.io

git pull https://github.com/F123/f123.github.io

How to Write a Post
-------------------

For technical reasons, posts and pages are written in `kramdown`, a
variant of `markdown` which includes tables. The major mode `markdown`
in `emacs` will work very nicely for this.


### Post Conventions ###

[Jekyll][jekyll] expects the post to have the filename
`yyyy-mm-dd-title.md`. Place this file in the `_posts` directory.

Make sure the filename is entirely in lowercase letters and use dashes to avoid spaces between words. For example:

2017-04-28-this-is-an-example.md

Additionally, [Jekyll][jekyll] requires front matter at the top of
your file. The front matter for this post  follows:

    ---
    layout: post
    title: Posting Here
    author: Rill
    excerpt: How to write a post to this blog.
    tags: [blogging]
    permalink: /blog/posting-here
    ---

### Just Write ###

After preparing the front matter, write your post with `markdown`.

How to Publish a Post
---------------------

When you are satisfied with your post, publish it using `git`.

    git add _posts/<your file>
    git commit -m "publishing my post <file name>"
    git push origin master

Your post publishes on the [F123 blog][f123blog]

If an error occurs, [github pages][github pages] emails you.

[github pages]: https://guides.github.com/features/pages/  "github pages"

[jekyll]: http://jekyllrb.com/ "Jekyll"


[f123blog]: https://f123.github.io/ "F123 blog"

---
Updated on April 28, 2017, by Fernando Botelho, to include example of pull command and filename.

