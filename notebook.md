---
layout: page
title: Notebook
header: notebook
summary: an old-fashioned (online) notebook
link: /notebook/
---

{% for post in site.posts %}

<p><a href="{{ post.url }}">{{ post.title }}</a> <br> {{ post.description }}<br> {{ post.date \| date_to_string }}</p>

{% endfor %}