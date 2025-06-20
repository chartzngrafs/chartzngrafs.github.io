---
layout: default
title: Home
---

# Welcome to ChartzNGrafs Blog

Sharing insights, charts, and more! A cyberpunk-inspired blog featuring data visualizations, analytics, and digital creativity in a synthwave aesthetic.

## Latest Posts

{% for post in site.posts limit:5 %}
- **[{{ post.title }}]({{ post.url }})** - {{ post.date | date: "%B %d, %Y" }}
  
  {{ post.excerpt | strip_html | truncatewords: 20 }}

{% endfor %}
