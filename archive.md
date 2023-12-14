---
layout: page
title: Notebook
summary: an old-fashioned (online) notebook
---

<!-- If you would like to search inside the posts, try:

<div class="gcse-search">
<script async src="https://cse.google.com/cse.js?cx=f09bf157da7f941a0">
</script>
</div> -->

{% for post in site.posts %}

<p><a href="{{ post.url }}">{{ post.title }}</a>   
{{ post.date | date: "%Y.%m.%d" }}</p>

{% endfor %}