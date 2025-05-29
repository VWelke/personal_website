---
layout: default
title: Blog
---

# Blog


---

{% for post in site.posts %}
<div class="card">
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <p><em>{{ post.date | date: "%B %d, %Y" }}</em></p>
  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}
