---
layout: page
title: Blog
---

# Blog Posts

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%b %d, %Y"}}
{% endfor %}
