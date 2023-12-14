---
layout: page
title: Notebook
summary: an old-fashioned (online) notebook
---

{% for post in site.posts limit:10 %}

<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>   
<p class="post-metadata">{{ post.date | date: "%Y.%m.%d" }}</p>

{{ post.content }}

{% endfor %}

To see all posts, see the [archive](archive.html) or search for what you seek:

<div class="gcse-search">
<script async src="https://cse.google.com/cse.js?cx=f09bf157da7f941a0">
</script>
</div>