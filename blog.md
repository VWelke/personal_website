---
layout: default
title: Blog
---

# 📝 Blog

Welcome to my blog! Here I share reflections on research, interesting tools, and notes from my astrophysics journey.

---

{% for post in site.posts %}
<div class="card">
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <p><em>{{ post.date | date: "%B %d, %Y" }}</em></p>
  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}
