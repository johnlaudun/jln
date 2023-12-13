---
layout: page
title: Notebook
summary: an old-fashioned (online) notebook
---

{% for post in site.posts %}

<p><a href="{{ post.url }}">{{ post.title }}</a>   
{{ post.date | date: "%Y.%m.%d" }}</p>

{% endfor %}